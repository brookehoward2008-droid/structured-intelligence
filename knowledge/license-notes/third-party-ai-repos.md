# Third-Party AI Repository License Notes

Purpose: prevent accidental license contamination while consolidating AI skills, prompts, workflows, and tool notes into `structured-intelligence`.

## Core rule

Do not copy third-party source code, prompts, assets, or docs into this repository until the license and attribution requirements are confirmed.

Use this repository for original wrappers, workflow notes, installation notes, summaries, and compatibility maps.

## Initial license/risk table

| Repository | Observed license/status | Consolidation status | Notes |
|---|---|---|---|
| `structured-intelligence` | MIT according to its README | Native home | Canonical repo for original AI skills and workflows. |
| `ai-flow` | MIT according to README | Reference or selective integration | Full app. Keep source separate unless importing small permitted pieces with attribution. |
| `claude-mem` | AGPL 3.0 badge in README | Reference only | Do not copy source into an MIT-oriented repo unless deliberately accepting AGPL obligations. |
| `token-optimizer` | PolyForm Noncommercial badge in README | Reference only | Do not copy source into a general public skills repo. Build original notes/wrappers instead. |
| `everything-claude-code` | MIT badge in README | Reference/vendor only first | Large ecosystem. Importing wholesale would create maintenance complexity. |
| `claude-code-system-prompts` | Prompt reference repo | Reference only first | System prompt text changes over time and may have upstream terms. Link/summarize rather than copying wholesale. |
| `promptoftheyear` | Prompt collection with backlinks/authorship notes | Curate only | Preserve attribution and avoid importing unsafe or low-quality prompts. |
| `Maintained-Database-for-Claude-connectors` | Connector directory | Knowledge index only | Good source for connector mapping; verify license/attribution before mirroring content. |
| `indesign-mcp-server` | Tool/server repo | Wrapper only | Keep MCP server source separate; create a local skill that explains safe usage. |
| `evolver` | Not fully reviewed | Hold | Needs deeper scan before action. |

## Approved consolidation types

These are safe starting points:

- original README notes written for this repo
- original `SKILL.md` files
- original workflow checklists
- repo maps and summaries
- install instructions that link to upstream instead of copying code
- compatibility matrices
- local usage notes
- attribution-preserving prompt indexes

## Not approved until reviewed

- source files from third-party repos
- full prompt corpora copied from external collections
- logos, screenshots, and assets from upstream repos
- license files changed or omitted from imported code
- minified compiled code
- memory databases, logs, session transcripts, or private local config

## Suggested source-note format

For every third-party reference, create a short note:

```text
Project:
Upstream:
Purpose:
License observed:
Copied source: no / yes
Copied assets: no / yes
Attribution required:
Local wrapper path:
Review date:
Decision:
```

## First safe action

Create wrapper skills from scratch:

- `skills/github-safe-recovery/`
- `skills/book-preflight/`
- `skills/indesign-mcp-control/`
- `skills/repo-quality-scan/`

Do not import source code yet.
