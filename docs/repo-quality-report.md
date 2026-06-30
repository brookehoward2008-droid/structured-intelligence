# AI / Skills Repository Quality Report

Branch: `ai-skills-consolidation`

Purpose: identify which AI, prompt, MCP, memory, token, and skill repositories should be consolidated into this repository and which should remain separate as references.

## Executive decision

Use `structured-intelligence` as the canonical AI-skills command center.

Do not combine every source repo directly into this repository. Consolidate original skills, wrapper skills, workflows, documentation, and source maps here. Keep third-party or differently licensed projects as references unless their license and project purpose clearly allow direct reuse.

## Recommended consolidation model

| Category | Action |
|---|---|
| Original Brooke skills, agents, workflows | Move or rewrite into this repo |
| Prompt maps and personal workflow notes | Consolidate into `prompts/`, `workflows/`, and `knowledge/` |
| Third-party tools with permissive license | Reference first, copy only after license review |
| AGPL or noncommercial code | Do not copy source into this MIT-oriented repo |
| Large app repositories | Keep separate; add integration notes and wrappers here |
| Book / InDesign automation | Keep book repos separate; create reusable InDesign skills and workflows here |

## Candidate repo scan

| Repository | Role | Quality notes | Recommendation |
|---|---|---|---|
| `structured-intelligence` | Canonical AI-skills workspace | Already has top-level locations for agents, skills, workflows, knowledge, prompts, scripts, and docs. | Make this the main repo. |
| `everything-claude-code` | Large Claude/Codex/OpenCode skills and harness ecosystem | Strong reference, but too broad to merge wholesale. | Vendor/reference only. Extract patterns carefully. |
| `claude-code-system-prompts` | Prompt reference and system-prompt archive | Useful as a reference corpus. Not an active skill workspace. | Keep separate; add notes and links only. |
| `claude-mem` | Persistent memory system | Valuable, but licensed differently from this repo. | Do not copy source into this repo. Create conceptual notes only. |
| `token-optimizer` | Token/cost/session optimization system | Useful, but licensed for noncommercial terms. | Keep separate; use as reference only unless license is reviewed. |
| `ai-flow` | AI workflow app | Full app with UI/backend/runtime assumptions. | Keep separate app. Add integration notes only. |
| `promptoftheyear` | Prompt collection | Contains external prompts and authorship/backlink context. | Curate and attribute. Do not import wholesale. |
| `Maintained-Database-for-Claude-connectors` | MCP/connector catalog | Good knowledge source for connector mapping. | Mirror as a knowledge index only if license/attribution is clear. |
| `indesign-mcp-server` | InDesign MCP automation server | Highly relevant to Booklab and publishing workflows. | Keep as tool repo; add wrapper skill/workflow here. |
| `evolver` | Possible AI/dev tool repo | Needs deeper scan before consolidation. | Hold for later review. |

## Quality risks found

1. **License mixture.** The candidate repos do not all share the same license. This prevents a simple copy-everything consolidation.
2. **Different purposes.** Some repos are full applications, some are prompts, some are skill packs, and some are reference databases.
3. **Public visibility.** Several repos are public. Do not place personal memory, private keys, API keys, medical details, school credentials, or private book source assets here.
4. **Overlapping AI concepts.** Memory, prompts, skills, MCP connectors, and token optimization overlap but are not the same thing. They need clean categories.
5. **Tool-specific installation paths.** Claude Code, Codex, OpenClaw, and other harnesses use different install conventions. This repo should provide wrappers and install scripts rather than assume one tool.

## Preferred repo taxonomy

```text
agents/        persona/task agents
skills/        reusable capability bundles
workflows/     step-by-step operating procedures
knowledge/     source maps, vendor notes, connector notes, license notes
prompts/       reusable prompt templates and prompt analyses
scripts/       validation, install, inventory, and audit scripts
docs/          architecture, reports, and public documentation
```

## Immediate next actions

1. Keep `structured-intelligence` as the master AI-skills repo.
2. Add a repo map before moving any code.
3. Add license notes before copying any third-party source.
4. Add wrapper skills for InDesign, GitHub recovery, book production, and repo auditing.
5. Add validation checks so the repo stays organized as it grows.

## Safe consolidation rule

When in doubt, link and summarize first. Copy source only after license, authorship, and maintenance purpose are confirmed.
