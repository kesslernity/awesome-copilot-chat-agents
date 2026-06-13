# Awesome Copilot Chat Agents

> **52 ready-to-deploy agents for Microsoft Copilot Chat — no Copilot Premium required.**
> Paste each instruction block into the Copilot Studio agent builder. No coding. Works on any commercial M365 licence.

[![GitHub stars](https://img.shields.io/github/stars/kesslernity/awesome-copilot-chat-agents?style=flat-square)](https://github.com/kesslernity/awesome-copilot-chat-agents/stargazers)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

---

## Who This Is For

Most enterprise M365 deployments have a small cohort of users on M365 Copilot (the premium licence) and a much larger group on Copilot Chat — the version included with any commercial M365 licence at no extra cost. That larger group does not get email or calendar grounding, SharePoint search, or Teams integration. What they do get is a capable AI assistant with a custom agent builder, web search, and file analysis.

This repo serves the majority. Every agent here is designed for Copilot Chat's constraints:

- **Instruction-only** — no SharePoint knowledge sources required
- **No M365 data grounding** — everything works from pasted input or web search
- **No extra cost** — deploys on any commercial M365 licence
- **No coding** — paste the instruction block into the Copilot Studio builder and you are done

If your organisation is evaluating which users need premium Copilot licences, this repo demonstrates how much is possible without them.

---

## Deploying Copilot for your org?

The **[M365 Copilot Practitioner Kit](https://kesslermathieu.gumroad.com/l/kpfpi)** covers the full picture: IT prerequisites, governance before you publish, a 90-day rollout roadmap, 26 field guides, and 10 agent templates with practitioner notes on when to build each and what breaks in week one.

**[Get the kit →](https://kesslermathieu.gumroad.com/l/kpfpi)**

---

### 📕 Governing the estate, not just building it

If you are running AI in an enterprise and the question "who owns the model's mistake?" does not yet have a name against it, **Critical Density** is the responsibility-and-audit playbook: how dependency builds invisibly, why attribution has to be installed before an incident, and a five-artifact toolkit (the Density Register, the Attribution-Readiness Checklist, the RACI-for-AI, the Audit Question Bank, and the Governance-Cadence Control Spec). Audit-grade, EU AI Act-aware, sector-neutral.

Start free with the [Licence-Plate Test](https://store.kesslernity.com/l/licence-plate-test) (a 12-question attribution self-test), or get the full book + toolkit: [Critical Density, $59](https://store.kesslernity.com/l/critical-density).

---

## AI at Work Newsletter + Free Course

**AI at Work** — a biweekly GenAI briefing with verified news, tested prompts, and one practical insight for your whole team.

[Subscribe at newsletter.kesslernity.com](https://newsletter.kesslernity.com)

Free 35-minute course: **AI Quick Start Essentials** — practical responsible AI use, no prior experience needed.

[Start free at trainings.kesslernity.com](https://trainings.kesslernity.com)

---

## What This Is

These are **declarative agents** built in Microsoft Copilot Studio — the same builder available at [m365.cloud.microsoft](https://m365.cloud.microsoft). Each agent has:

- A name and description users see when they @mention it
- Conversation starters that guide first use
- An instruction block that defines the agent's role, output format, language rules, quality checks, and edge case handling

**How this differs from the companion premium repo:**

| | This repo (Copilot Chat) | [awesome-copilot-studio-agents](https://github.com/kesslernity/awesome-copilot-studio-agents) (M365 Copilot) |
|--|--------------------------|----------------------------------------------|
| Licence required | Any commercial M365 | M365 Copilot (premium) |
| SharePoint grounding | No | Yes |
| Email & calendar access | No | Yes |
| Teams integration | No | Yes |
| Web search | Yes (Bing, built-in) | Yes |
| File analysis | Yes (pasted) | Yes |
| Custom agents | Yes | Yes |
| Extra cost | None | Copilot licence |

---

## Copilot Chat vs M365 Copilot — What Works Here

| Feature | Copilot Chat (free tier) | M365 Copilot (premium) |
|---------|:----------------------:|:--------------------:|
| Custom declarative agents | ✓ | ✓ |
| Web search (Bing) | ✓ | ✓ |
| File analysis (pasted content) | ✓ | ✓ |
| @mention agents in Teams/Chat | ✓ | ✓ |
| Email and calendar grounding | ✗ | ✓ |
| Teams message search | ✗ | ✓ |
| SharePoint knowledge grounding | ✗ | ✓ |
| Word / Excel / PowerPoint integration | ✗ | ✓ |
| Graph-connected agents | ✗ | ✓ |

---

## How to Deploy Any Agent

1. Go to [m365.cloud.microsoft/chat/agent/new](https://m365.cloud.microsoft/chat/agent/new) (or search for "Copilot" in your M365 app launcher and select "Create an agent")
2. Paste the **Name** and **Description** from the agent file's front matter
3. Paste the **Conversation Starters** (up to 4)
4. Copy the full instruction block from the **Instructions** section and paste it into the Instructions field
5. Save and publish — the agent is immediately available via @mention in Copilot Chat

**For research-web agents (marked 🌐):** Enable web search in the agent's settings when creating it. This is free and uses Bing — no additional licence required.

No SharePoint connections, no Actions, no Graph connectors needed for any agent in this repo.

---

## Agent Directory

### Domain 1: Writing & Communication
`agents/writing-communication/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 1 | [Meeting Minutes Writer](agents/writing-communication/meeting-minutes-writer.md) | Converts pasted notes or transcripts into structured minutes | All staff / EAs / PMs | `@Meeting Minutes Writer` |
| 2 | [Email Tone Coach](agents/writing-communication/email-tone-coach.md) | Adjusts tone of email drafts without changing meaning | All staff | `@Email Tone Coach` |
| 3 | [Executive Summary Maker](agents/writing-communication/executive-summary-maker.md) | Converts long documents into structured executive summaries | All staff / Managers / EAs | `@Executive Summary Maker` |
| 4 | [Comms Clarity Coach](agents/writing-communication/comms-clarity-coach.md) | Improves clarity and readability of any business communication | All staff | `@Comms Clarity Coach` |
| 5 | [Report Narrative Builder](agents/writing-communication/report-narrative-builder.md) | Converts data tables or raw findings into narrative paragraphs | Analysts / Finance / PMs | `@Report Narrative Builder` |
| 6 | [Business Case Builder](agents/writing-communication/business-case-builder.md) | Structures a business case document from pasted notes | Managers / BAs / Project leads | `@Business Case Builder` |
| 7 | [Language Translator](agents/writing-communication/language-translator.md) | Translates text between languages with tone and register preservation | Global teams / All staff | `@Language Translator` |
| 8 | [AI Text Humanizer](agents/writing-communication/ai-text-humanizer.md) | Removes AI writing patterns — restores direct, varied, human-sounding prose | All staff / Writers / Comms / Marketing | `@AI Text Humanizer` |

### Domain 2: Project Management
`agents/project-management/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 9 | [Status Report Writer](agents/project-management/status-report-writer.md) | Generates structured project status reports from pasted notes | PMs / PMO / Team leads | `@Status Report Writer` |
| 10 | [Risk Register Assistant](agents/project-management/risk-register-assistant.md) | Builds project risk registers from pasted notes | PMs / PMO / Risk managers | `@Risk Register Assistant` |
| 11 | [RAID Log Helper](agents/project-management/raid-log-helper.md) | Builds RAID logs from pasted project notes or workshop outputs | PMs / PMO / BAs | `@RAID Log Helper` |
| 12 | [Project Brief Builder](agents/project-management/project-brief-builder.md) | Builds structured project briefs from problem descriptions or email threads | PMs / BAs / Sponsors | `@Project Brief Builder` |
| 13 | [Lessons Learned Facilitator](agents/project-management/lessons-learned-facilitator.md) | Structures lessons learned documents from retrospective notes | PMs / PMO / Agile coaches | `@Lessons Learned Facilitator` |

### Domain 3: IT Operations
`agents/it-operations/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 14 | [Incident Post-Mortem Writer](agents/it-operations/incident-post-mortem-writer.md) | Converts incident notes into structured blameless post-mortems | IT / DevOps / SRE | `@Incident Post-Mortem Writer` |
| 15 | [Change Request Drafter](agents/it-operations/change-request-drafter.md) | Drafts structured IT change requests from pasted descriptions | IT / DevOps / Change Managers | `@Change Request Drafter` |
| 16 | [Runbook Creator](agents/it-operations/runbook-creator.md) | Converts operational procedures into structured runbooks | IT / SRE / DevOps | `@Runbook Creator` |
| 17 | [SLA Report Writer](agents/it-operations/sla-report-writer.md) | Converts SLA metrics into structured performance reports | IT Managers / Service Delivery | `@SLA Report Writer` |
| 18 | [IT Comms Translator](agents/it-operations/it-comms-translator.md) | Translates technical IT communications into plain business language | IT Comms / Service Desk | `@IT Comms Translator` |

### Domain 4: HR & People
`agents/hr-people/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 19 | [Job Description Writer](agents/hr-people/job-description-writer.md) | Drafts inclusive job descriptions from role briefs | HR / Hiring managers / TA | `@Job Description Writer` |
| 20 | [Interview Question Generator](agents/hr-people/interview-question-generator.md) | Generates competency-based interview question sets from a JD | HR / Hiring managers | `@Interview Question Generator` |
| 21 | [Performance Feedback Coach](agents/hr-people/performance-feedback-coach.md) | Helps write balanced SBI-model performance feedback from notes | Managers / HR / All staff | `@Performance Feedback Coach` |
| 22 | [Onboarding Checklist Builder](agents/hr-people/onboarding-checklist-builder.md) | Builds structured onboarding checklists from pre-arrival to day 30 | HR / Managers / Team leads | `@Onboarding Checklist Builder` |
| 23 | [Team Announcement Writer](agents/hr-people/team-announcement-writer.md) | Drafts team announcements — hires, departures, restructures, launches | Managers / HR / Comms | `@Team Announcement Writer` |

### Domain 5: Learning & Knowledge
`agents/learning-knowledge/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 24 | [Concept Explainer](agents/learning-knowledge/concept-explainer.md) | Explains any concept at the complexity level the user specifies | All staff / L&D / Managers | `@Concept Explainer` |
| 25 | [FAQ Generator](agents/learning-knowledge/faq-generator.md) | Generates structured FAQs from any pasted content | All staff / Comms / IT / HR | `@FAQ Generator` |
| 26 | [Knowledge Article Writer](agents/learning-knowledge/knowledge-article-writer.md) | Converts process notes into structured knowledge base articles | IT / Operations / HR / Support | `@Knowledge Article Writer` |
| 27 | [Training Content Builder](agents/learning-knowledge/training-content-builder.md) | Converts SME notes into structured training materials | L&D / Managers / SMEs | `@Training Content Builder` |
| 28 | [Onboarding Guide Writer](agents/learning-knowledge/onboarding-guide-writer.md) | Builds structured onboarding guides from role notes | HR / Managers / Team leads / L&D | `@Onboarding Guide Writer` |

### Domain 6: Productivity & Thinking
`agents/productivity-thinking/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 29 | [Decision Clarity Coach](agents/productivity-thinking/decision-clarity-coach.md) | Structures a decision frame with options, criteria, and tradeoffs | All staff / Managers | `@Decision Clarity Coach` |
| 30 | [Brainstorm Facilitator](agents/productivity-thinking/brainstorm-facilitator.md) | Runs structured brainstorming from a challenge statement | All staff / Teams / Managers | `@Brainstorm Facilitator` |
| 31 | [Action Item Extractor](agents/productivity-thinking/action-item-extractor.md) | Extracts action items and commitments from meeting notes or email chains | All staff / PMs / EAs | `@Action Item Extractor` |
| 32 | [Meeting Agenda Builder](agents/productivity-thinking/meeting-agenda-builder.md) | Builds structured meeting agendas with time allocations from a topic list | All staff / Managers / EAs | `@Meeting Agenda Builder` |
| 33 | [Structured Problem Solver](agents/productivity-thinking/structured-problem-solver.md) | Applies 5 Whys, Fishbone, or Problem-Cause-Solution to a described problem | All staff / Managers / Ops / IT | `@Structured Problem Solver` |

### Domain 7: Finance
`agents/finance/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 34 | [Financial Narrative Writer](agents/finance/financial-narrative-writer.md) | Converts financial data and tables into plain-language management commentary | Finance managers / FP&A / CFOs / Controllers | `@Financial Narrative Writer` |
| 35 | [Budget Justification Writer](agents/finance/budget-justification-writer.md) | Converts budget line items into structured approval-ready justification text | Finance managers / Budget owners / Dept heads | `@Budget Justification Writer` |
| 36 | [Variance Analysis Coach](agents/finance/variance-analysis-coach.md) | Structures root-cause variance explanations that hold up under scrutiny | FP&A / Finance business partners / Controllers | `@Variance Analysis Coach` |
| 37 | [Audit Prep Assistant](agents/finance/audit-prep-assistant.md) | Drafts audit query responses, evidence lists, and process narratives | Finance managers / Controllers / Internal audit | `@Audit Prep Assistant` |
| 38 | [Investor Update Writer](agents/finance/investor-update-writer.md) | Converts financial results and milestones into structured investor updates | CFOs / IR teams / Founders / Finance directors | `@Investor Update Writer` |

### Domain 8: Engineering
`agents/engineering/`

*These agents include explicit safety boundaries — all outputs must be reviewed by the responsible engineer before issue.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 39 | [Technical Specification Writer](agents/engineering/technical-spec-writer.md) | Converts engineering requirements and design notes into structured technical specs | Mechanical / Electrical / Civil / Process / HVAC engineers | `@Technical Specification Writer` |
| 40 | [Engineering Report Writer](agents/engineering/engineering-report-writer.md) | Structures field notes, design review outputs, and technical findings into formal reports | Engineers across disciplines / Project engineers / Site supervisors | `@Engineering Report Writer` |
| 41 | [Electrical Load List Helper](agents/engineering/electrical-load-list-helper.md) | Checks electrical load lists for completeness, totals installed/operating loads, flags gaps | Electrical engineers / Project engineers | `@Electrical Load List Helper` |
| 42 | [HVAC Design Documenter](agents/engineering/hvac-design-documenter.md) | Converts HVAC design notes into design basis statements, system descriptions, and equipment schedules | HVAC / Building services / MEP engineers | `@HVAC Design Documenter` |
| 43 | [RFI Response Drafter](agents/engineering/rfi-response-drafter.md) | Drafts structured RFIs and RFI responses for engineering and construction projects | Project engineers / Site engineers / Contract engineers | `@RFI Response Drafter` |

### Domain 9: Sales & BD
`agents/sales-bd/`

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 44 | [Outreach Personalizer](agents/sales-bd/outreach-personalizer.md) | Drafts personalised outreach from pasted prospect context | Sales / BD / AEs / SDRs | `@Outreach Personalizer` |
| 45 | [Objection Handler Coach](agents/sales-bd/objection-handler-coach.md) | Structures objection responses and offers role-play practice | Sales / BD / AEs / CS | `@Objection Handler Coach` |
| 46 | [Proposal Reviewer](agents/sales-bd/proposal-reviewer.md) | Reviews proposal drafts for clarity, structure, and disqualification risk | Sales / BD / Bid Managers | `@Proposal Reviewer` |
| 47 | [Competitive Brief Builder](agents/sales-bd/competitive-brief-builder.md) | Builds competitive intelligence briefs from pasted input (no web search) | Sales / BD / Marketing / Strategy | `@Competitive Brief Builder` |
| 48 | [Win/Loss Analyst](agents/sales-bd/win-loss-analyst.md) | Structures win/loss analysis from pasted debrief notes | Sales / BD / Sales Leadership | `@Win/Loss Analyst` |

### Domain 10: Research & Web Intelligence 🌐
`agents/research-web/`

*These agents use Bing web search — free and built into Copilot Chat. Enable web search when creating the agent.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 49 | [Topic Research Summarizer](agents/research-web/topic-research-summarizer.md) 🌐 | Researches any topic via web search and returns a cited summary | All staff / Analysts / Managers | `@Topic Research Summarizer` |
| 50 | [News Digest Builder](agents/research-web/news-digest-builder.md) 🌐 | Builds a ready-to-share news digest on any topic or keyword | All staff / Managers / Comms | `@News Digest Builder` |
| 51 | [Competitor Monitor](agents/research-web/competitor-monitor.md) 🌐 | Summarises recent public activity for a named competitor | Sales / Marketing / Strategy | `@Competitor Monitor` |
| 52 | [Market Brief Builder](agents/research-web/market-brief-builder.md) 🌐 | Builds a market intelligence brief on any sector using web search | Strategy / BD / Sales / Leadership | `@Market Brief Builder` |

🌐 = Requires web search enabled in Copilot Chat settings. Free — uses Bing, no additional licence required.

---

## The Reasoning Behind These 52 Agents

Every agent in this repo follows the same hidden discipline. The instruction blocks that work in production aren't better at telling the agent what to do — they're explicit about what it must **never** do, they survive the 8,000-character limit without losing structure, and they fail in predictable, recoverable ways.

That discipline is a craft. After writing and rewriting these 52 blocks, the patterns that separate an agent that holds up from one that drifts became repeatable — so I wrote them down.

**[Agent Instruction Block Design Guide](https://kesslermathieu.gumroad.com/l/eyeauo)** — $19 — is the craft behind this repo:

- **12 design patterns**, each with a before/after rewrite
- **8 named failure modes** — the specific ways instruction blocks break, and how to close each one
- **The 8,000-character constraint**, treated as a design problem instead of a wall you hit
- A **reusable agent scaffold** you can start every new agent from
- **5 full worked rewrites** of real instruction blocks, broken/fixed side by side
- A **10-question deployment test** to run before you publish
- **Agent Builder vs Copilot Studio** — every field limit, plus model-stability and reasoning/response-mode guidance

These 52 agents are free and always will be — and they're already in production. This is the reasoning layer underneath them, for when you're mid-build in Agent Builder or Copilot Studio and your own block isn't behaving.

**[Read the reasoning → $19](https://kesslermathieu.gumroad.com/l/eyeauo)**

> Building the judgment side too — *when* an agent is the wrong tool? See **[When Not to Use AI — A Decision Framework for Teams](https://kesslermathieu.gumroad.com/l/nusvz)** ($29), or **[get both for $39](https://kesslermathieu.gumroad.com/l/oocxx)** (saves $9).

---

## Companion Repo: M365 Copilot Premium Agents

If your organisation upgrades to M365 Copilot, the premium repo unlocks SharePoint grounding, email and calendar access, and Teams integration.

**[awesome-copilot-studio-agents](https://github.com/kesslernity/awesome-copilot-studio-agents)** — 78 agents across 14 domains, built for M365 Copilot premium licences.

Several agents in this repo have premium counterparts there that add M365 data grounding — for example, a Status Report Writer that reads from your actual project SharePoint site instead of requiring pasted input. If you are running both licence tiers in your organisation, the two repos complement each other: deploy the chat agents for your broad user base, and the premium agents for your Copilot-licensed cohort.

---

## Contributing

Contributions welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the quality bar, file format requirements, and PR guidelines.

The two key constraints for this repo:
- **Copilot Chat tier only** — no SharePoint knowledge sources, no Graph connectors, no premium features
- Instruction blocks must be under 8,000 characters

---

## Licence

[Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/)

You are free to use, adapt, and redistribute these agents — including commercially — as long as you credit the source and share derivatives under the same licence.

---

*Built by [Mathieu Kessler](https://linkedin.com/in/mathieukessler) · [NerdyChefs.ai](https://nerdychefs.ai) · [kesslernity.com](https://kesslernity.com)*
