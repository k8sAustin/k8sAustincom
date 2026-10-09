# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Not an application — there is no build, test, or lint step. It backs https://k8saustin.com (Cloud Native Austin, formerly Kubernetes Austin — a CNCF community chapter) as a Netlify site made of a static landing page (`index.html`, `404.html`) and the `_redirects` file. The rest is governance/community markdown. Netlify auto-deploys from `main` (status badge in `README.md`), so a merged change to `index.html` or `_redirects` is live immediately.

Naming: Cloud Native Austin is the new name for Kubernetes Austin (same group, broader scope beyond Kubernetes). Keep the `k8saustin.com` domain and existing short links working.

## Files that matter

- **`index.html`** / **`404.html`** — self-contained static pages (inline CSS, system fonts, white background, light theme only (no dark mode), no build step). `index.html` is the landing page served at `/` and explains the Kubernetes Austin → Cloud Native Austin rename; `404.html` is served by Netlify for unknown paths. Keep them prettier-clean and free of external assets.
- **`_redirects`** — Netlify redirect rules. Maps short paths (`/meetup`, `/present`, `/slack`, `/youtube`, per-event slugs like `/autoscaling`, `/talos`) to external targets (ocgroups.dev event pages, Sessionize, Meetup, social profiles, Google/Typeform forms).
- **`Sessions-Selection-Guidelines.md`** — Program Committee governance doc: track categorization (A–D), 1–5 assessment rubric, triage protocol, reviewer guidelines. Carries a `Document Version: YYYY.MM.DD` header.
- **`README.md`** — the single source for the chapter overview/values/CoC/CFP text (a duplicate `Kubernetes-Austin.md` was removed; don't reintroduce a second copy).
- **`package.json`** — only dependency is `netlify-shortener`, exposed as `npm run shorten` (`netlify-shortener`) to add short links to `_redirects`. Run `npm install` first (`node_modules` is not committed).

## `_redirects` conventions

- Format is `/<slug>  <target-url>` with column-aligned whitespace; one rule per line.
- There is intentionally **no `/*` catch-all**: `/` serves `index.html` and unknown paths get `404.html`. Don't re-add a catch-all without also deciding what happens to `/`. If a wildcard is ever added, it must be last — Netlify evaluates top-to-bottom and first match wins.
- Every short path linked from `index.html` (`/present`, `/host`, `/slack`, `/feedback`, `/meetup`, social links) must exist here; removing one breaks the page.
- Event slugs point at specific ocgroups.dev event IDs; new events get a new slug rather than repointing an old one (old links are in circulation on slides/social).
- `/managed-oss` and `/monitoring-oss` currently point at the same event URL (`ttf4zrq`) — likely a copy/paste error; verify before touching either.
- Slugs are case-sensitive in Netlify's default matching; `/kuberTENes` is intentionally mixed-case.
- Test a changed redirect against the deploy preview (or `curl -sI https://k8saustin.com/<slug>`) rather than assuming it works.

## Git workflow

Changes land via PRs from `feature/<name>` branches into `main` (see merged PRs #2, #3 in history). Conventional commits.

**Never commit directly to `main`.** Always create a new branch first (`git switch -c feature/<change-name>`). This is enforced by a `PreToolUse` hook in `.claude/settings.json` that denies `git commit` from Bash while on `main`/`master`. Create the branch in its own step — a chained `git switch -c x && git commit` is still denied because the branch is checked before the command runs.
