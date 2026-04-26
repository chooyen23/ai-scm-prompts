# AI SCM Prompts — Claude Skill

A Claude skill that gives supply chain professionals ready-to-use AI prompt templates across four operational domains. Stop starting from scratch — just describe your task and get a prompt built for your context.

---

## What This Skill Does

When installed, this skill teaches Claude to recognise supply chain tasks and respond with structured, role-specific prompt templates. It covers **32 use cases across 4 domains**, organised into an 8-level progression framework from everyday documentation all the way to strategic stress-testing.

Just talk to Claude naturally — *"I need to write an RFP for a new 3PL"* or *"our main supplier just failed, what do I do?"* — and the skill routes your question to the right template automatically.

---

## The Four Domains

| Domain | What it covers |
|---|---|
| 🚢 **Freight Forwarding** | BOL drafting, spot-rate quoting, HS Code compliance, route optimisation, port disruption contingencies, carrier scouting |
| 🏭 **Distribution Centre** | Slot planning, labour scheduling, safety audits, throughput analysis, cycle counts, automation evaluation |
| 📋 **Procurement** | RFP/RFQ drafting, spec writing, contract review, negotiation prep, supplier analysis, stakeholder communication |
| ⚙️ **Operations Management** | SOP writing, capacity planning, process audits (Lean/Six Sigma), executive reporting, disruption simulation, Industry 4.0 scouting |

---

## The 8-Level Framework

Each domain follows the same progression — start at Level 1 for quick wins, work up as confidence grows:

| Level | Theme | Example task |
|---|---|---|
| 1 | Drafting & Documentation | Write a BOL, SOP, or RFP |
| 2 | Planning & Calculation | Staffing headcount, spot-rate comparison |
| 3 | Audit & Review | Contract risk check, warehouse layout review |
| 4 | Optimisation | Route planning, sourcing strategy |
| 5 | Synthesis & Analysis | Summarise logs, proposals, or reports |
| 6 | Executive Communication | Turn data into a CEO-ready business case |
| 7 | Stress-Testing | "What if the port strikes / supplier fails?" |
| 8 | Technology Scouting | Compare tools, evaluate automation ROI |

---

## Installation

### Requirements
- A [Claude.ai](https://claude.ai) account (Free, Pro, or Team)
- Code Execution enabled: **Settings → Capabilities → Code Execution**

### Install the skill

1. Download **`ai-scm-prompts.skill`** from the [Releases](../../releases) page
2. In Claude.ai, go to **Customize → Skills**
3. Click **Upload Skill** and select the downloaded file
4. Toggle the skill **on**

That's it. The skill is now active in your Claude sessions.

---

## How to Use It

Once installed, just talk to Claude normally using supply chain language. The skill triggers automatically — no slash commands needed.

**Example prompts that activate the skill:**

- *"Help me draft a Bill of Lading for a CIF shipment to Rotterdam"*
- *"I need to calculate headcount for a peak season volume of 50,000 orders"*
- *"Our sortation conveyor is down for 6 hours — what's the contingency plan?"*
- *"Write a prompt to stress-test our single-source supplier risk"*
- *"How do I use AI to reduce our Scope 3 emissions?"*

Claude will identify your domain, match it to the right level, and return an adapted prompt template with guidance on what to fill in.

---

## Cross-Domain Scenarios

Some real-world situations span more than one domain. The skill handles these automatically:

| Scenario | Domains combined |
|---|---|
| Supplier failure / delivery disruption | Procurement + Operations (L7) |
| Carrier performance / KPI scorecard | Freight + Operations (L4) |
| Sustainability / carbon / Scope 3 | Freight (L4) + Operations (L3) |
| DC headcount + machine planning | Distribution + Operations (L2) |
| Last-mile routing with modal shift | Operations + Freight (L4) |

---

## Repository Structure

```
ai-scm-prompts/
├── README.md               ← You are here
├── SKILL.md                ← Skill routing logic and framework
└── .doc/
    ├── AI_for_Freight_Forwarding.md
    ├── AI_for_Distribution.md
    ├── AI_for_Procurement.md
    └── AI_for_Operations_Management.md
```

The `.doc/` folder contains the full reference content for each domain — 8 levels each, with goals, use cases, and prompt templates. Claude loads only the relevant file per session, keeping responses focused.

---

## For Educators

This skill is designed to work as a teaching tool, not just a practitioner tool. The 8-level framework maps naturally to a learning progression:

- **L1–L2** — Build confidence with low-risk, high-frequency tasks
- **L3–L5** — Apply analytical thinking to real operational data
- **L6–L7** — Develop strategic communication and resilience planning
- **L8** — Evaluate technology critically, not just enthusiastically

Suggested classroom exercise progression:

1. **Starter (L1):** Give students a packing list and ask them to prompt Claude to generate a BOL or SOP
2. **Applied (L4):** Provide a scenario with cost and time constraints — ask them to prompt Claude for a route or sourcing optimisation
3. **Capstone (L7):** Run a disruption simulation — *"your key supplier just failed for 2 weeks"* — and have students prompt Claude to build a mitigation plan, then critique the output

---

## Contributing / Feedback

Found a gap, a wrong domain routing, or a use case that's missing? Open an issue or submit a pull request. The skill is built to be iterated on.

---

*Built for SCM professionals and educators. Covers Freight Forwarding · Distribution Centre · Procurement · Operations Management.*
