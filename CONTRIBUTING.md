# Contributing to Awesome Copilot Chat Agents

Thank you for contributing. This repo is maintained by [Mathieu Kessler](https://linkedin.com/in/mathieukessler) and accepts community contributions for new agents and improvements to existing ones.

---

## What Makes a Good Copilot Chat Agent

A good agent in this repo does one thing well. It does not try to cover every scenario — it covers its specific domain clearly, with sensible limits and honest edge case handling.

### The core constraint: Copilot Chat tier only

Every agent in this repo must work on the Copilot Chat free tier. This means:

- **No SharePoint knowledge sources** — the agent cannot be grounded on a SharePoint site, document library, or Teams channel
- **No Graph connectors** — no access to emails, calendars, tasks, or Teams messages
- **No premium actions** — no Power Automate flows, no external API connectors
- **No M365 Copilot-only features** — no Copilot Pages, no document drafting from meeting recordings

What is allowed:

- **Pasted input** — the user pastes text into the conversation
- **Web search (Bing)** — for research-web domain agents only; this is free and built into Copilot Chat
- **File analysis** — users can attach and ask the agent to analyse a file they paste or share in the chat
- **Conversation memory** — within a single session

If your agent requires any premium feature, it belongs in the companion repo ([awesome-copilot-studio-agents](https://github.com/kesslernity/awesome-copilot-studio-agents)).

---

## File Format

Every agent file must use the exact format below. The front matter and all five required sections are non-negotiable.

### Front Matter

```markdown
---
name: [Agent Name — max 30 characters]
description: [1-2 sentences — this is what users see when browsing agents]
domain: [domain slug — match existing folder names]
audience: [target roles, comma-separated]
knowledge_sources: None required
tier: copilot-chat
language: EN / EN-FR
char_count: ~[estimate — count the instruction block only]
rai_reviewed: yes
tested: no
version: 1.0
last_updated: [YYYY-MM-DD]
---
```

### Required Sections

All five of these sections must be present in every instruction block. A submission missing any of them will not be merged.

#### 1. ROLE
Define what the agent does and its scope. Always end the ROLE section with: "The user must review all output before distributing or acting on it."

#### 2. WHAT YOU ACCEPT AS INPUT
List the input forms the agent handles. Be specific — this sets user expectations.

#### 3. WHAT YOU DO NOT DO
3–5 explicit limits. This section protects users and prevents the agent from being used outside its safe scope. Be direct.

#### 4. LANGUAGE RULES
Every agent must include bilingual support in exactly this form:

```
Default: formal professional English, British spelling.
French: if the input is in French or the user requests French output, produce all output in French.
Bilingual: English first, then "--- Version francaise ---", then French.
```

Do not change the language default or the French trigger — these are standard across all agents.

#### 5. OUTPUT (any heading variant: OUTPUT FORMAT, OUTPUT STRUCTURE, etc.)
Define the exact output structure. Use numbered sections, tables, or labelled blocks. The more specific this is, the more consistent and useful the output.

#### 6. QUALITY SELF-CHECK
A checklist the agent runs before delivering output. Always include the banned vocabulary line exactly as written:

```
[ ] No banned vocabulary: pivotal, robust (abstract), vibrant, seamless, impactful, groundbreaking, revolutionary, game-changing.
Correct any failure before delivering.
```

Add 3–4 domain-specific checks above this line.

#### 7. EDGE CASES (minimum 3)
Handle at least 3 realistic edge cases. Format:

```
[Scenario]: [How the agent handles it]
```

Edge cases must cover: input that is too thin to work with, a request the agent should decline, and at least one scenario specific to the domain.

---

## Instruction Block Character Limit

The instruction block (everything inside the triple backtick block in the Instructions section) must be **under 8,000 characters**. Copilot Studio enforces this limit.

To check your count: paste the instruction block into a character counter. The `char_count` field in the front matter should reflect this estimate (e.g. `~3,800`).

If your agent is over the limit:
- Tighten the ROLE — remove redundant phrasing
- Consolidate edge cases — combine similar scenarios
- Shorten output format descriptions — use table headers rather than prose descriptions
- Do not remove any of the five required sections

---

## How to Test Your Agent

Before submitting a PR, test the agent against at least four scenarios:

1. Go to [m365.cloud.microsoft/chat/agent/new](https://m365.cloud.microsoft/chat/agent/new)
2. Paste the name, description, conversation starters, and instruction block
3. Test each conversation starter — verify the output matches the format defined in the instructions
4. Test at least one edge case — verify the agent handles it as specified
5. Test a French input or a request for French output — verify the language rules work
6. Confirm the instruction block was accepted without a character limit error

Update `tested: no` to `tested: yes` in the front matter once you have completed these steps.

---

## File Naming and Location

- File names: `[number]-[kebab-case-name].md` — e.g. `32-outreach-personalizer.md`
- Location: `agents/[domain-slug]/[file-name].md`
- Domain slugs: `writing-communication`, `project-management`, `it-operations`, `hr-people`, `learning-knowledge`, `productivity-thinking`, `sales-bd`, `research-web`
- If proposing a new domain, open an issue first to align on the slug and confirm it does not duplicate an existing category

---

## PR Guidelines

- **One agent per PR** — do not bundle multiple agents into a single PR; it makes review harder
- **Include char count** — state the instruction block character count in the PR description
- **Confirm testing** — state in the PR that you tested each conversation starter and the agent was accepted by Copilot Studio without a character limit error
- **Update tested status** — set `tested: yes` in the front matter if you have tested the agent yourself
- **No premium features** — confirm in the PR that the agent requires no SharePoint sources, no Graph connectors, and no premium actions
- **British spelling throughout** — the repo standard is British English (behaviour not behavior, licence not license, organisation not organization)
- **No emojis in instruction blocks** — emojis are permitted in the README and in conversation starter text, but not inside instruction blocks

---

## What We Will Not Merge

- Agents that require SharePoint, Graph connectors, or any premium M365 Copilot feature
- Instruction blocks over 8,000 characters
- Files missing any of the five required sections (ROLE, OUTPUT, LANGUAGE RULES, QUALITY SELF-CHECK, EDGE CASES)
- Agents that do not include the banned vocabulary check in QUALITY SELF-CHECK
- Agents with safety risks — anything that could be used for safety-critical decisions, medical diagnosis, legal advice, financial advice, or similar high-risk outputs without appropriate disclaimers and human review gates
- Agents that collect, process, or store personal data beyond what the user explicitly pastes into the session

---

## Improving Existing Agents

Improvements to existing agents are welcome. Common improvements:

- Additional edge cases that reflect real-world usage
- Tighter output format definitions
- Better conversation starters
- Instruction block optimisation (reducing character count while preserving quality)

When improving an existing agent, increment the version in the front matter (e.g. `1.0` → `1.1`) and add a row to the Changelog table at the bottom of the file.

---

## Questions

Open an issue or reach out via [kesslernity.com](https://kesslernity.com).
