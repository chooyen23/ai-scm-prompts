---
name: ai-scm-prompts
description: >
  Provides structured, role-specific AI prompt templates and use cases for Supply Chain Management (SCM)
  professionals. Use this skill whenever the user asks for help with prompts, use cases, or AI applications
  across any of these four SCM domains: Freight Forwarding, Distribution Centre Management, Procurement,
  or Operations Management. Trigger this skill when the user mentions shipping, logistics, warehousing,
  buying, sourcing, operations, customs, carriers, suppliers, DC, 3PL, MHE, or any related
  supply chain topic — even if they don't use the word "prompt". Also trigger when the user asks
  "how do I use AI for [SCM topic]" or "give me a prompt for [SCM task]".
---

# AI SCM Prompts Skill

This skill helps supply chain professionals apply AI across four core operational domains. It provides
ready-to-use prompt templates, structured use cases, and an 8-level progression framework — from
basic document drafting to advanced stress-testing and technology scouting.

---

## Domain Reference Files

All domain content lives in `.doc/`. Load **only the file relevant to the user's domain** — do not
load all four at once.

| Domain | When to load | File |
|---|---|---|
| Freight Forwarding | Shipping, BOL, customs, carrier quotes, route planning, port disruptions | `.doc/AI_for_Freight_Forwarding.md` |
| Distribution Centre | Warehousing, slotting, picking, MHE, safety audits, throughput, conveyor | `.doc/AI_for_Distribution.md` |
| Procurement | Sourcing, RFP/RFQ, contracts, negotiation, supplier analysis, spend | `.doc/AI_for_Procurement.md` |
| Operations Management | SOPs, capacity planning, process audits, production, downtime, Industry 4.0 | `.doc/AI_for_Operations_Management.md` |

---

## How to Use This Skill

### Step 1 — Identify the domain
Determine which of the four domains the user's question belongs to. If ambiguous, ask:
> "Are you working on freight/logistics, warehouse operations, procurement/sourcing, or general operations management?"

### Cross-Domain Routing Exceptions

Some scenarios seem to belong to one domain but need content from another. Always check these before loading a single file:

| User's scenario | Primary file | Also load |
|---|---|---|
| "Supplier can't deliver / failed / disrupted" | `.doc/AI_for_Procurement.md` | `.doc/AI_for_Operations_Management.md` (L7: Disruption Simulation) — this has the contingency/mitigation prompt |
| "Carrier performance / KPI / scorecard" | `.doc/AI_for_Freight_Forwarding.md` | `.doc/AI_for_Operations_Management.md` (L4: Logistics Optimization) — carrier performance analysis lives here |
| "DC staffing / headcount" | `.doc/AI_for_Distribution.md` | `.doc/AI_for_Operations_Management.md` (L2: Capacity Planning) — if the ask includes machine/equipment alongside people |
| "Last-mile / delivery routing" | `.doc/AI_for_Operations_Management.md` | `.doc/AI_for_Freight_Forwarding.md` (L4: Route & Modal Optimization) — for multi-modal or carrier-specific angles |
| "Sustainability / carbon / emissions / green logistics / Scope 3" | `.doc/AI_for_Freight_Forwarding.md` (L4: Route & Modal Optimization — CO2 calculations) | `.doc/AI_for_Operations_Management.md` (L3: Process Audit — waste/Muda identification) — together they cover transport emissions + operational waste reduction |

**Synthesized prompt for sustainability / carbon footprint analysis** (spans Freight L4 + Ops L3):
```
"Analyze our supply chain operations for carbon reduction opportunities. For transport,
evaluate modal shift options (e.g., sea vs. air vs. road) and estimate the CO2 saving
per route change. For operations, identify the top 3 process waste areas (Muda) that
also carry a carbon cost. Summarize findings as a Scope 3 emissions reduction roadmap:
[paste transport lanes + process data]."
```

**Synthesized prompt for carrier performance analysis** (gap not covered in source files):
```
"Analyze this carrier performance dataset. Score each carrier on [On-Time Delivery %, Damage Rate,
Cost per Shipment]. Identify the bottom performer and draft a supplier performance review summary
with recommended actions: [paste data]."
```

---

### Step 2 — Load the relevant reference file
Read the appropriate `.doc/` file. Each file contains 8 levels of AI application, each with:
- A **Goal** (the business outcome)
- **USE IT FOR** (specific tasks)
- A **PROMPT TEMPLATE** (ready to adapt)

### Step 3 — Match to the right level
Map the user's task to the appropriate level using this guide:

| Level | Theme | Typical Ask |
|---|---|---|
| 1 | Drafting & Documentation | "Help me write a BOL / SOP / RFP" |
| 2 | Planning & Calculation | "How many staff do I need? What's the spot rate?" |
| 3 | Audit & Review | "Check this contract / workflow / layout for issues" |
| 4 | Optimization | "Find me a better route / sourcing strategy" |
| 5 | Synthesis & Analysis | "Summarize these logs / proposals / reports" |
| 6 | Executive Communication | "Turn this into a CEO summary / business case" |
| 7 | Stress-Testing | "What if the port strikes / supplier fails?" |
| 8 | Technology Scouting | "Compare these tools / evaluate this tech" |

### Step 4 — Deliver the response
Provide:
1. The **matching prompt template**, adapted to the user's specifics if they've shared them
2. A brief note on **what to fill in** (placeholders like `[Origin]`, `[Volume]`, etc.)
3. Optionally, a tip on how to **chain** this with an adjacent level for more impact

---

## Response Format Guidelines

- **For a single task**: Give the prompt template directly, with a 1-sentence explanation of what it does.
- **For a broad "how do I use AI for X" question**: Present 3–4 of the most relevant levels as a short menu, then ask which one to go deeper on.
- **For educators/teaching contexts**: Frame the levels as a learning progression — "Start with Level 1 to build confidence, then move to Level 4 once the basics click."
- **For cross-domain questions** (e.g., procurement + operations): Load both relevant files and synthesize.

---

## Quick-Load Summary (without opening files)

If the user's ask is simple and clearly matches a known level, you can respond from this condensed
summary before loading the full file. For anything nuanced, load the file.

**Freight Forwarding quick reference:**
- L1 BOL/invoice drafting · L2 Spot-rate quoting · L3 HS Code / customs audit · L4 Route optimization (incl. CO2 calculations)
- L5 Email/delay synthesis · L6 Client visibility reports · L7 Contingency planning · L8 Carrier scouting
- ⚠️ *Carrier performance/KPIs* → also load Ops L4
- ⚠️ *Sustainability / carbon / green logistics / Scope 3* → also load Ops L3

**Distribution Centre quick reference:**
- L1 Re-slotting plans · L2 Headcount / shift scheduling · L3 Layout & racking audit · L4 Safety / MHE analysis
- L5 Throughput bottleneck · L6 Cycle count reconciliation · L7 Equipment failure contingency · L8 Automation scouting
- ⚠️ *Headcount + machine planning together* → also load Ops L2

**Procurement quick reference:**
- L1 RFP/SOW drafting · L2 Spec writing · L3 Contract risk review · L4 Negotiation prep
- L5 Supplier analysis · L6 Stakeholder influence · L7 Pressure-testing (own sourcing decisions) · L8 Market research
- ⚠️ *Supplier failure / delivery disruption* → Procurement L7 is NOT the right prompt — load Ops L7 instead

**Operations Management quick reference:**
- L1 SOP drafting · L2 Capacity planning · L3 Process / waste audit — Lean/Muda (incl. carbon cost of waste) · L4 Logistics optimization (incl. carrier performance)
- L5 Data synthesis · L6 Executive reporting · L7 Disruption simulation (supplier failure, strikes, demand spikes) · L8 Technology scouting
- ⚠️ *Sustainability / carbon / Scope 3 emissions* → also load Freight L4 for transport modal shift analysis
