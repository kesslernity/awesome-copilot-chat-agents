# Awesome Copilot Chat Agents

> **82 ready-to-deploy agents for Microsoft Copilot Chat — no Copilot Premium required.**
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

### Domain 11: Legal & Contracts
`agents/legal/`

*These agents draft and organize only. Every output requires review by a qualified lawyer before use, and law is jurisdiction-specific — they do not provide legal advice.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 53 | [Contract Clause Reviewer](agents/legal/contract-clause-reviewer.md) | Reviews a pasted clause against your standard position — lists deviations and points to raise | In-house counsel / Contracts / Legal ops | `@Contract Clause Reviewer` |
| 54 | [NDA First-Draft Assistant](agents/legal/nda-first-draft-assistant.md) | Drafts a first-draft NDA from a brief, marked for legal review, with a reviewer checklist | In-house counsel / Contracts / Paralegals | `@NDA First-Draft Assistant` |
| 55 | [Legal Research Summarizer](agents/legal/legal-research-summarizer.md) | Summarizes pasted memos, case notes, or statute excerpts into a structured brief | In-house counsel / Paralegals / Compliance | `@Legal Research Summarizer` |
| 56 | [Matter Status Reporter](agents/legal/matter-status-reporter.md) | Turns matter notes into a structured legal status report | In-house counsel / Legal ops / Paralegals | `@Matter Status Reporter` |
| 57 | [Regulatory & Policy Tracker](agents/legal/regulatory-policy-tracker.md) | Turns regulatory updates or policy text into an impact summary for compliance review | Compliance / In-house counsel / Regulatory | `@Regulatory & Policy Tracker` |

### Domain 12: Procurement & Vendor Management
`agents/procurement/`

*These agents prepare and organize only — they never score, select, award, or commit. Evaluation and award decisions stay with procurement under your governance.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 58 | [RFP Requirements Builder](agents/procurement/rfp-requirements-builder.md) | Turns a need into structured RFP/RFQ requirements (criteria only, no scores) | Procurement / Category / Sourcing | `@RFP Requirements Builder` |
| 59 | [Supplier Response Comparator](agents/procurement/supplier-response-comparator.md) | Lays bid responses side by side vs requirements with gaps and questions | Procurement / Sourcing / Panels | `@Supplier Response Comparator` |
| 60 | [Vendor Scorecard Builder](agents/procurement/vendor-scorecard-builder.md) | Structures performance evidence into a scorecard (reviewer sets the ratings) | Procurement / Vendor managers | `@Vendor Scorecard Builder` |
| 61 | [Negotiation Prep Brief](agents/procurement/negotiation-prep-brief.md) | Turns history and context into a negotiation prep brief (no price targets) | Procurement / Category / Buyers | `@Negotiation Prep Brief` |
| 62 | [Supplier Comms Drafter](agents/procurement/supplier-comms-drafter.md) | Drafts RFI invites, clarifications, declines, onboarding requests (no commitments) | Procurement / Buyers / Ops | `@Supplier Comms Drafter` |

### Domain 13: Data & Analytics
`agents/data-analytics/`

*These agents explore, document, and draft — never the source of truth. Verify every figure in your data/BI platform; correlation is not causation.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 63 | [Data Story Writer](agents/data-analytics/data-story-writer.md) | Turns validated findings into a stakeholder narrative (no recompute, no overclaim) | Data / BI / Analytics | `@Data Story Writer` |
| 64 | [Report Requirements Builder](agents/data-analytics/report-requirements-builder.md) | Turns a stakeholder ask into a BI requirements spec with gaps flagged | BI / Business analysts | `@Report Requirements Builder` |
| 65 | [KPI Definition Helper](agents/data-analytics/kpi-definition-helper.md) | Drafts precise KPI/metric definitions for governance review | Analytics / BI / Data | `@KPI Definition Helper` |
| 66 | [Chart Advisor](agents/data-analytics/chart-advisor.md) | Recommends chart types and encodings for a message and data shape | Analysts / anyone building a chart | `@Chart Advisor` |
| 67 | [Data Dictionary Builder](agents/data-analytics/data-dictionary-builder.md) | Turns a column list/schema into a data dictionary draft, [TBC] where unknown | Data / Analytics engineers | `@Data Dictionary Builder` |

### Domain 14: Data Privacy
`agents/data-privacy/`

*These agents prepare privacy paperwork only — they never determine lawfulness, breach notifiability, DPIA risk, or what to disclose, and they work from descriptions, never personal data. The DPO decides.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 68 | [DPIA Scaffold Builder](agents/data-privacy/dpia-scaffold-builder.md) | Turns a processing description into a DPIA scaffold (ratings left to the DPO) | DPO / Privacy counsel / Privacy | `@DPIA Scaffold Builder` |
| 69 | [ROPA Entry Drafter](agents/data-privacy/ropa-entry-drafter.md) | Drafts a Record of Processing Activities entry (lawful basis left to confirm) | Privacy managers / DPO | `@ROPA Entry Drafter` |
| 70 | [DSAR Intake Assistant](agents/data-privacy/dsar-intake-assistant.md) | Structures a data subject request into intake, scope, and statutory clock | Privacy / DPO | `@DSAR Intake Assistant` |
| 71 | [Breach Triage Organizer](agents/data-privacy/breach-triage-organizer.md) | Organizes suspected-breach facts for the DPO's assessment (no notifiability call) | DPO / Privacy / Incident leads | `@Breach Triage Organizer` |
| 72 | [Privacy Notice Drafter](agents/data-privacy/privacy-notice-drafter.md) | Drafts a privacy notice/section for legal/DPO review and jurisdiction check | Privacy counsel / DPO | `@Privacy Notice Drafter` |

### Domain 15: Trade Compliance
`agents/trade-compliance/`

*These agents prepare the export-control file only — they never assign a classification, determine a screening match, clear a party, or decide a licence. Screening runs in your screening tool; trade compliance decides. Export/sanctions errors carry civil and criminal liability.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 73 | [Export Classification Prep](agents/trade-compliance/export-classification-prep.md) | Builds a classification worksheet from a product/tech description (no ECCN/USML assigned) | Export control / Trade compliance | `@Export Classification Prep` |
| 74 | [Restricted Party Screening Prep](agents/trade-compliance/restricted-party-screening-prep.md) | Extracts all parties to screen + a checklist (screening runs in the tool) | Trade compliance / Trade ops | `@Restricted Party Screening Prep` |
| 75 | [Export Red Flag Checker](agents/trade-compliance/red-flag-checker.md) | Applies standard export red-flag indicators to a transaction (flags, not a finding) | Trade compliance / Export liaisons | `@Export Red Flag Checker` |
| 76 | [End-Use Statement Drafter](agents/trade-compliance/end-use-statement-drafter.md) | Drafts an end-use/end-user statement scaffold + due-diligence questions | Trade compliance / Sales | `@End-Use Statement Drafter` |
| 77 | [Trade Compliance Comms Drafter](agents/trade-compliance/trade-comms-drafter.md) | Drafts end-use requests, hold notices, escalations (no clearance/determination) | Trade compliance / Trade ops | `@Trade Compliance Comms Drafter` |

### Domain 16: Risk, Ethics & Compliance
`agents/risk-ethics-compliance/`

*These agents prepare GRC paperwork only — they never make a compliance determination, an ethics ruling, an investigation finding, or a risk acceptance. Investigations and speak-up matters are confidential and may be privileged.*

| # | Agent | Description | Audience | Invoke |
|---|-------|-------------|----------|--------|
| 78 | [Compliance Policy Drafter](agents/risk-ethics-compliance/policy-drafter.md) | Drafts a compliance/ethics policy (code, ABAC, COI) for compliance/legal review | Compliance / Ethics counsel | `@Compliance Policy Drafter` |
| 79 | [COI Disclosure Triage](agents/risk-ethics-compliance/coi-disclosure-triage.md) | Structures a conflict-of-interest disclosure into an assessment intake | Ethics & compliance | `@COI Disclosure Triage` |
| 80 | [Third-Party DD Questionnaire Builder](agents/risk-ethics-compliance/third-party-dd-questionnaire.md) | Builds an ABAC/third-party due-diligence questionnaire + red flags (no clearance) | Compliance / ABAC | `@Third-Party DD Questionnaire Builder` |
| 81 | [Controls Mapping Helper](agents/risk-ethics-compliance/controls-mapping-helper.md) | Maps a requirement to controls and flags gaps (no compliance conclusion) | Compliance / Risk / Audit | `@Controls Mapping Helper` |
| 82 | [Investigation Chronology Organizer](agents/risk-ethics-compliance/investigation-chronology-organizer.md) | Organizes investigation facts into a confidential chronology (never a finding) | Investigations / Compliance counsel | `@Investigation Chronology Organizer` |

---

## More from Kesslernity

This repo is free and stays free. If it's useful, here's the rest of the toolkit.

**Free**
- 📄 **Copilot on One Page** — the one-page cheat sheet for getting real answers out of Copilot. [Free download](https://store.kesslernity.com/l/copilot-on-one-page)

**The rest of the free Copilot repos**
- [awesome-microsoft-copilot-prompts](https://github.com/kesslernity/awesome-microsoft-copilot-prompts) — 400+ tested Copilot prompts
- [awesome-copilot-studio-agents](https://github.com/kesslernity/awesome-copilot-studio-agents) — ready-to-deploy Copilot Studio agents
- [awesome-copilot-cowork-skills](https://github.com/kesslernity/awesome-copilot-cowork-skills) — Cowork skills

**Deploying Copilot for a team?**
- 🛒 Deployment kits, governance playbooks, and the honest "when not to use it" guides, built so you can deploy Copilot without a consultant: **[kesslernity.com/store](https://kesslernity.com/store)**

Independent and vendor-neutral. Not affiliated with Microsoft.

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
