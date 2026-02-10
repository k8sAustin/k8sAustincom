# Kubernetes Austin: Technical Sessions Selection - Standards & Governance

**Document Version:** 1.0  
**Owner:** Program Committee & Technical Steering  
**Objective:** To ensure all presentations meet the "Tier 1" quality and architectural standards required by the Silicon Hills engineering ecosystem.

---

## 1. Session Categorization (Track Metadata)

Before scoring, the Program Committee classifies each proposal into one of the following tracks to ensure a balanced, high-value agenda for our members.

* **Track A: The Onboarding (Introductory & Tutorial)**
  * *Target Audience:* Junior to Mid-level practitioners.
  * *Focus:* "Zero to One" implementation, helping new engineers grasp core Cloud Native concepts.
* **Track B: The Deep Dive (Level: Intermediate to Advanced)**
  * *Target Audience:* Senior Engineers, Site Reliability Engineers (SREs), and Architects.
  * *Focus:* Internals, advanced debugging, complex networking, cluster security and observability.
* **Track C: The Visionary (Novel Contributions)**
  * *Target Audience:* Technical Leads, CTOs, and Ecosystem Innovators.
  * *Focus:* Bold new patterns, highly creative problem-solving, and advanced "Day 2" operations insights.

---

## 2. The Assessment Rubric (1-5 Scale)

All proposals are evaluated against four core criteria. This rigorous peer-review process protects our members' time and ensures regional technical excellence.

### 📐 Criterion A: Content Quality & Structure
*Does the proposal demonstrate engineering rigor and coherent storytelling?*

* **1 Star:** Unclear, incoherent, incomplete, or lacks a discernible thesis.
* **2 Stars:** Somewhat relevant but poorly written; unrealistic scope (e.g., trying to cover "All of K8s" in 20 minutes) or unclear takeaways.
* **3 Stars:** Clear and structured, but predictable. A standard "How-to" format lacking unique insight or depth.
* **4 Stars:** Well-written and coherent. Strong fit for the session format with a clear, engaging narrative arc.
* **5 Stars:** **Highly Engaging.** Polished, high-impact audience takeaways. Demonstrates absolute mastery of the subject matter and exceptional presentation structure.

### 🎯 Criterion B: Community Relevance
*Does this topic matter to the Kubernetes Austin audience right now?*

* **1 Star:** Not relevant to the K8s Meetup. Little to no audience value.
* **2 Stars:** Tangential topic or possesses very limited, isolated appeal.
* **3 Stars:** Relevant, but addresses a narrow niche or highly specific edge case.
* **4 Stars:** Strongly aligned with CNCF goals. Broad, immediate value to the local engineering community.
* **5 Stars:** **Community Critical.** Addresses timely and significant Cloud Native challenges (e.g., breaking version changes, critical CVEs, major ecosystem shifts) with wide-scale impact.

### 🛡️ Criterion C: Vendor Neutrality (The Integrity Gate)
*Does this session serve the community or a corporate sales pitch?*

* **1 Star (The "Sales Pitch"):** **HARD REJECT.**
  * *Definition:* Clear focus on proprietary software without wider ecosystem value.
* **3 Stars (The "Borderline"):** **CONDITIONAL ACCEPTANCE.**
  * *Definition:* A valid technical problem is discussed, but the solution leans heavily toward a specific commercial tool without acknowledging Open Source alternatives.
  * *Action:* Reviewer must request the speaker add a "Comparative Architecture" slides contextualizing the tool within the broader CNCF landscape before final acceptance.
* **5 Stars (The "Community Standard"):** **TIER 1 QUALITY.**
  * *Definition:* Pure architectural patterns, unbiased "War Stories" (failures and successes), or deep-dives into CNCF Graduated/Incubating projects.
  * *Indicator:* The knowledge is universally transferable regardless of which vendor or cloud provider the audience utilizes.

### 🏗️ Criterion D: Architectural Impact & Scalability
*Does this session address the complex, high-stakes challenges faced by the Silicon Hills enterprise ecosystem?*

* **1 Star (Hobbyist):** Homelab or sandbox scale only. Excellent for personal learning, but lacks relevance to enterprise production environments.
* **3 Stars (Mid-Market):** Applicable to startups or mid-sized clusters. Standard, out-of-the-box implementation patterns.
* **5 Stars (Hyperscale / Enterprise Ready):** * *Definition:* Explicitly addresses high-stakes architectural challenges relevant to massive-scale, Fortune 500 environments. 
  * *Topics:* Multi-region federation, Zero-Trust security at scale, fleet-wide cost-optimization, or highly complex legacy migration strategies.

---

## 3. The Selection Protocol (Decision Matrix)

To maintain our status as a premier hub for the CNCF community, the Program Committee adheres to the following decision thresholds:

| Decision | Criteria Threshold | Committee Action |
| :--- | :--- | :--- |
| **Auto-Reject** | Score < 2 in any category, OR a 1 Star in Vendor Neutrality. | Issue standard decline notification detailing the missed criteria. |
| **Mentorship Track** | High Potential (4-5 stars in Impact/Relevance) but Low Structure (2-3 stars in Content Quality). | **"Yes, if..."** The Program Chair offers direct coaching/feedback to help the speaker refine their technical narrative. |
| **Standard Accept** | Average > 3.5 Stars across all categories. | Schedule for an upcoming monthly session. |
| **Premier Slot** | 5 Stars in both "Architectural Impact" & "Vendor Neutrality". | Fast-tracked and reserved for the **"Headliner"** slot to attract Senior/Lead engineering attendance. |

---

## 4. Reviewer Guidelines & Mentorship Philosophy

Kubernetes Austin believes in building speakers, not just hosting them. When applying this rubric, reviewers must adhere to the following principles:

1. **Constructive Rejection:** If a proposal is declined, the reviewer must cite the specific criterion (e.g., "Currently scoring a 2 on Vendor Neutrality") to provide the speaker with an actionable path to improve and resubmit.
2. **Cultivating "Hidden Gems":** Actively look for local engineers with immense technical depth (scoring high on Criterion D) who may simply lack public speaking experience. Route them to the Mentorship Track to help polish their delivery.
