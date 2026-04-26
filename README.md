# AI SCM Prompts — Claude Skill
A Claude skill that gives supply chain professionals ready-to-use AI prompt templates across four operational domains. Stop starting from scratch — just describe your task and get a prompt built for your context.

## What This Skill Does
When installed, this skill teaches Claude to recognise supply chain tasks and respond with structured, role-specific prompt templates. It covers 32 use cases across 4 domains, organised into an 8-level progression framework from everyday documentation all the way to strategic stress-testing.
Just talk to Claude naturally — "I need to write an RFP for a new 3PL" or "our main supplier just failed, what do I do?" — and the skill routes your question to the right template automatically.

## The Four Domains
DomainWhat it covers🚢 Freight ForwardingBOL drafting, spot-rate quoting, HS Code compliance, route optimisation, port disruption contingencies, carrier scouting🏭 Distribution CentreSlot planning, labour scheduling, safety audits, throughput analysis, cycle counts, automation evaluation📋 ProcurementRFP/RFQ drafting, spec writing, contract review, negotiation prep, supplier analysis, stakeholder communication⚙️ Operations ManagementSOP writing, capacity planning, process audits (Lean/Six Sigma), executive reporting, disruption simulation, Industry 4.0 scouting

## The 8-Level Framework
Each domain follows the same progression — start at Level 1 for quick wins, work up as confidence grows:
LevelThemeExample task1Drafting & DocumentationWrite a BOL, SOP, or RFP2Planning & CalculationStaffing headcount, spot-rate comparison3Audit & ReviewContract risk check, warehouse layout review4OptimisationRoute planning, sourcing strategy5Synthesis & AnalysisSummarise logs, proposals, or reports6Executive CommunicationTurn data into a CEO-ready business case7Stress-Testing"What if the port strikes / supplier fails?"8Technology ScoutingCompare tools, evaluate automation ROI

## Installation
### Requirements

A Claude.ai account (Free, Pro, or Team)
Code Execution enabled: Settings → Capabilities → Code Execution

### Install the skill

Download ai-scm-prompts.skill from the Releases page
In Claude.ai, go to Customize → Skills
Click Upload Skill and select the downloaded file
Toggle the skill on

That's it. The skill is now active in your Claude sessions.

### How to Use It
Once installed, just talk to Claude normally using supply chain language. The skill triggers automatically — no slash commands needed.

#### Example prompts that activate the skill:

- "Help me draft a Bill of Lading for a CIF shipment to Rotterdam"
- "I need to calculate headcount for a peak season volume of 50,000 orders"
- "Our sortation conveyor is down for 6 hours — what's the contingency plan?"
- "Write a prompt to stress-test our single-source supplier risk"
- "How do I use AI to reduce our Scope 3 emissions?"

Claude will identify your domain, match it to the right level, and return an adapted prompt template with guidance on what to fill in.

### Cross-Domain Scenarios
Some real-world situations span more than one domain. The skill handles these automatically:
ScenarioDomains combinedSupplier failure / delivery disruptionProcurement + Operations (L7)Carrier performance / KPI scorecardFreight + Operations (L4)Sustainability / carbon / Scope 3Freight (L4) + Operations (L3)DC headcount + machine planningDistribution + Operations (L2)Last-mile routing with modal shiftOperations + Freight (L4)

Repository Structure
ai-scm-prompts/
├── README.md               ← You are here
├── SKILL.md                ← Skill routing logic and framework
└── .doc/
    ├── AI_for_Freight_Forwarding.md
    ├── AI_for_Distribution.md
    ├── AI_for_Procurement.md
    └── AI_for_Operations_Management.md
The .doc/ folder contains the full reference content for each domain — 8 levels each, with goals, use cases, and prompt templates. Claude loads only the relevant file per session, keeping responses focused.
