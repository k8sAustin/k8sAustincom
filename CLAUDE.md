# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Not an application — there is no build, test, or lint step. It backs https://k8saustin.com (Kubernetes Austin, a CNCF community chapter) as a Netlify site whose only functional artifact is the `_redirects` file. The rest is governance/community markdown. Netlify auto-deploys from `main` (status badge in `README.md`), so a merged change to `_redirects` is live immediately.

## Files that matter

- **`_redirects`** — Netlify redirect rules; this is the whole "site". Maps short paths (`/meetup`, `/present`, `/slack`, `/youtube`, per-event slugs like `/autoscaling`, `/talos`) to external targets (ocgroups.dev event pages, Sessionize, Meetup, social profiles, Google/Typeform forms).
- **`Sessions-Selection-Guidelines.md`** — Program Committee governance doc: track categorization (A–D), 1–5 assessment rubric, triage protocol, reviewer guidelines. Carries a `Document Version: YYYY.MM.DD` header.
- **`README.md`** and **`Kubernetes-Austin.md`** — the chapter overview/values/CoC/CFP text. `Kubernetes-Austin.md` is currently a byte-identical copy of `README.md` minus the title/Netlify badge header. Keep them in sync or consolidate; don't edit one silently.
- **`package.json`** — only dependency is `netlify-shortener`, exposed as `npm run shorten` (`netlify-shortener`) to add short links to `_redirects`. Run `npm install` first (`node_modules` is not committed).

## `_redirects` conventions

- Format is `/<slug>  <target-url>` with column-aligned whitespace; one rule per line.
- The catch-all `/*  https://ocgroups.dev/cncf/group/3up7rjk` **must stay last** — Netlify evaluates top-to-bottom and first match wins, so any rule added below it is dead.
- Event slugs point at specific ocgroups.dev event IDs; new events get a new slug rather than repointing an old one (old links are in circulation on slides/social).
- `/managed-oss` and `/monitoring-oss` currently point at the same event URL (`ttf4zrq`) — likely a copy/paste error; verify before touching either.
- Slugs are case-sensitive in Netlify's default matching; `/kuberTENes` is intentionally mixed-case.
- Test a changed redirect against the deploy preview (or `curl -sI https://k8saustin.com/<slug>`) rather than assuming it works.

## Git workflow

Changes land via PRs from `feature/<name>` branches into `main` (see merged PRs #2, #3 in history). Conventional commits.

**Never commit directly to `main`.** Always create a new branch first (`git switch -c feature/<change-name>`). This is enforced by a `PreToolUse` hook in `.claude/settings.json` that denies `git commit` from Bash while on `main`/`master`. Create the branch in its own step — a chained `git switch -c x && git commit` is still denied because the branch is checked before the command runs.
