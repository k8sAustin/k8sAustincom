
# Kubernetes Austin: Technical Sessions Selection - Standards & Governance

**Document Version:** 2026.02.10  
**Owner:** Program Committee & Technical Steering  
**Objective:** To ensure all presentations meet the "Tier 1" quality and architectural standards required by the Silicon Hills engineering ecosystem.

---

## 💡 The Philosophy: Protecting Our Community's Time
As Central Texas grows into a major hub for enterprise cloud infrastructure, our meetup must evolve to serve everyone from junior developers to Fortune 500 Lead Architects. 

In the past, community events have occasionally struggled with "Trojan Horse" sales pitches or mismatched technical depths. This framework is designed to:
1. **Protect our stage** from disguised marketing and proprietary product pitches.
2. **Ensure a balanced agenda** that caters to both newcomers and highly advanced practitioners.
3. **Provide objective, constructive feedback** to local speakers to help them improve.

---

## 📂 1. Session Categorization (Track Metadata)

Before scoring, the Program Committee classifies each proposal into one of the following tracks to ensure a balanced, high-value agenda for our members.

* **Track A: The Onboarding (Introductory & Tutorial)**
  * *Target Audience:* Junior to Mid-level practitioners.
  * *Focus:* "Zero to One" implementation, helping new engineers grasp core Kubernetes and Cloud Native concepts.
* **Track B: The Deep Dive (Level: Intermediate to Advanced)**
  * *Target Audience:* Senior Engineers, Site Reliability Engineers (SREs), and Architects.
  * *Focus:* Internals, advanced debugging, leveraging eBPF, complex networking, cluster security and observability.
* **Track C: The Visionary (Novel Contributions)**
  * *Target Audience:* Technical Leads, CTOs, and Ecosystem Innovators.
  * *Focus:* Bold new architectural patterns, highly creative problem-solving, and advanced "Day 2" operations insights.

---

## ⚖️ 2. The Assessment Rubric (1-5 Scale)

All proposals are evaluated against four core criteria. This rigorous peer-review process protects our members' time and ensures regional technical excellence.

### 📐 Criterion A: Content Quality & Structure

*Does the proposal demonstrate engineering rigor and coherent storytelling?*

* **1 Star:** Unclear, incoherent, incomplete, or lacks a discernible thesis.
* **2 Stars:** Somewhat relevant but poorly written; unrealistic scope (e.g. "Everything about K8s in 15 mins") or unclear takeaways.
* **3 Stars:** Clear and structured, but predictable. A standard format lacking unique insight or depth.
* **4 Stars:** Well-written and coherent. Strong fit for the session format with a clear, engaging narrative arc.
* **5 Stars:** **Highly Engaging.** Polished, high-impact audience takeaways. Demonstrates absolute mastery of the subject matter and exceptional presentation structure.

### 🎯 Criterion B: Community Relevance

*Does this topic matter to the Kubernetes Austin audience right now?*

* **1 Star:** Not relevant to the K8s Austin Meetup and Cloud Native. Little to no audience value.
* **2 Stars:** Tangential topic or possesses very limited, isolated appeal.
* **3 Stars:** Relevant, but addresses a narrow niche or highly specific edge case.
* **4 Stars:** Strongly aligned with CNCF goals. Broad, immediate value to the community.
* **5 Stars:** **Community Critical.** Addresses timely and significant Cloud Native challenges (e.g., breaking version changes, major ecosystem shifts) with wide-scale impact.


### 🛡️ Criterion C: [Vendor Neutrality](https://contribute.cncf.io/projects/best-practices/community/vendor-neutrality/) (The Integrity Gate)

*Does this session serve the community or is a product pitch?*

* **1 Star (The "Product Pitch"):** **HARD REJECT.**
  * *Definition:* Clear focus on proprietary software without wider ecosystem value.
* **3 Stars (The "Borderline"):** **CONDITIONAL ACCEPTANCE.**
  * *Definition:* A valid technical problem is discussed, but the solution leans heavily toward a specific commercial tool without acknowledging Open Source alternatives.
  * *Action:* Reviewer must request the speaker add a "Comparative Architecture" slides contextualizing the tool within the broader CNCF landscape before final acceptance.
* **5 Stars (The "Community Standard"):** **TIER 1 QUALITY.**
  * *Definition:* Pure architectural patterns, unbiased "War Stories" (failures and successes), or deep-dives into CNCF projects. Knowledge is universally transferable.
  * *Indicator:* The knowledge is universally transferable regardless of which vendor or cloud provider the audience utilizes.

### 🏗️ Criterion D: Architectural Impact & Scalability
*Does this session address the complex, high-stakes challenges faced by the Silicon Hills enterprise ecosystem?*

* **1 Star (Hobbyist):** Homelab or sandbox scale only. Excellent for personal learning, but lacks relevance to enterprise production environments.
* **3 Stars (Mid-Market):** Applicable to startups or mid-sized clusters. Standard, out-of-the-box implementation patterns.
* **5 Stars (Hyperscale / Enterprise Ready):** * *Definition:* Explicitly addresses high-stakes architectural challenges relevant to massive-scale, Fortune 500 environments.
  * *Topics:* Multi-region federation, Zero-Trust security at scale, fleet-wide cost-optimization, or highly complex legacy migration strategies.

---

## 🔄 3. The Selection & Triage Protocol

To maintain our status as a premier hub for the CNCF community, the Program Committee will utilize the following workflow:

### Phase 1: The Workflow
1. **Initial Triage:** The designated **Program Chair** conducts a first-pass review of all incoming Sessionize submissions, scoring them against the Technical Rubric.
2. **The Filter:** The Program Chair applies the Decision Matrix (below) to automatically filter out proprietary sales pitches and route high-potential proposals to the Mentorship track.
3. **Committee Selection:** The Program Chair presents the curated "Shortlist" (sessions averaging > 3.0 Stars) to the full Co-Organizer team during our monthly sync for final slotting, ensuring the committee only spends time reviewing high-value proposals.

### Phase 2: The Decision Matrix
*The Program Chair applies the following thresholds during the Initial Triage phase:*

| Decision Stage | Criteria Threshold (Rubric Score) | Committee / Program Chair Action |
| :--- | :--- | :--- |
| **Auto-Reject** | Score of < 2 in *any* category, OR a strict 1 Star in *Vendor Neutrality*. | **Program Chair** issues a standard decline notification detailing the specific missed criteria. |
| **Mentorship Track** | High Potential (4-5 Stars in *Impact/Relevance*) but Low Structure (2-3 Stars in *Content Quality*). | **"Yes, if..."** Program Chair opens a dialogue offering direct architectural feedback to help the speaker refine their technical narrative. |
| **Standard Accept** | Average > 3.0 Stars across all categories. | Added to the **Shortlist** for the full committee to review and schedule for an upcoming monthly session. |
| **Premier Slot** | 5 Stars in both *Architectural Impact* AND *Vendor Neutrality*. | Fast-tracked and reserved for the **"Headliner"** slot to attract Senior/Lead engineering attendance. |

---

## 🤝 4. Reviewer Guidelines & Mentorship Philosophy

Kubernetes Austin believes in building speakers, not just hosting them. When applying this rubric, reviewers must adhere to the following principles:

1. **Cultivating "Hidden Gems":** Actively look for local engineers with immense technical depth (scoring high on Criterion D) who may simply lack public speaking experience or have poor structure (Low Content Quality). Route them to the Mentorship Track to help polish their delivery.
2. **Constructive Rejection:**  The Program Chair will initiate a "Mentorship" response, offering the speaker specific, constructive feedback to help them refine their narrative for a re-submission.
