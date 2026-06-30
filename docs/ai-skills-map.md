# AI Skills Map

This map defines where AI, prompt, MCP, memory, publishing, and automation materials belong inside `structured-intelligence`.

## Canonical organization

```text
structured-intelligence/
  agents/
  skills/
  workflows/
  knowledge/
  prompts/
  scripts/
  docs/
```

## Agent candidates

| Agent | Purpose | Default skills |
|---|---|---|
| `book-production-editor` | Protect editorial layout, source registers, bibliography, and print proof quality. | `book-preflight`, `indesign-production`, `github-safe-recovery` |
| `github-repo-auditor` | Scan repositories for structure, license risk, duplicated purpose, secrets, and build quality. | `repo-quality-scan`, `license-review`, `github-safe-recovery` |
| `indesign-production-specialist` | Support InDesign automation, JSX handoff, preflight, image-link checking, and print export. | `indesign-mcp-control`, `book-preflight` |
| `ai-skills-curator` | Organize prompts, skills, memory tools, MCP references, and install paths. | `prompt-library-cleanup`, `license-review`, `repo-quality-scan` |

## Skill candidates

| Skill | Purpose | Notes |
|---|---|---|
| `github-safe-recovery` | Branch, PR, and recovery workflow that avoids data-loss operations. | Based on the book repo recovery workflow. |
| `repo-quality-scan` | Audit repo structure, docs, license, package files, tests, and obvious risk terms. | Should produce Markdown and CSV outputs. |
| `license-review` | Sort third-party code into copy-safe, reference-only, and avoid categories. | Must run before consolidation. |
| `book-preflight` | PDF/book production checklist for trim, page count, photo-only checks, TOC, bibliography, and final proof review. | Reusable for Booklab/publication work. |
| `indesign-mcp-control` | Wrapper skill for InDesign MCP server usage and safe publishing tasks. | Should stay separate from the MCP server source. |
| `prompt-library-cleanup` | Clean prompt collections, preserve attribution, remove unsafe or low-quality prompt patterns. | Useful for `promptoftheyear`. |
| `token-budget-audit` | Measure and reduce AI context/tool overhead. | Should be original wrapper logic or notes, not copied noncommercial code. |
| `connector-catalog-review` | Maintain connector notes and use-case mapping. | Good fit for MCP connector database notes. |

## Workflow candidates

| Workflow | Purpose |
|---|---|
| `github-repo-consolidation` | Decide what to consolidate, what to archive, what to keep separate, and what needs license review. |
| `ai-skills-installation` | Install chosen skills into Codex, Claude Code, or custom skill directories. |
| `book-finalization` | Final proof sequence for editorial book PDFs and InDesign packages. |
| `mcp-tool-evaluation` | Evaluate MCP servers for safety, local requirements, maturity, and fit. |
| `prompt-corpus-cleanup` | Turn prompt collections into attributed, reusable prompt templates. |

## Knowledge areas

```text
knowledge/
  connectors/
  license-notes/
  prompt-references/
  vendor-notes/
  book-production/
  local-ai-tools/
```

## Consolidation lanes

### Lane A: Safe to build here

Original materials created for Brooke's workflows:

- Book production checklists
- GitHub recovery process notes
- InDesign workflow wrappers
- Repo audit workflows
- Skill installation scripts
- Prompt cleanup notes

### Lane B: Reference only first

Third-party projects that are useful but should not be copied yet:

- `everything-claude-code`
- `claude-code-system-prompts`
- `claude-mem`
- `token-optimizer`
- `ai-flow`
- `indesign-mcp-server`

### Lane C: Keep separate apps

Full applications and servers should stay as standalone repositories:

- AI workflow apps
- MCP servers
- memory service apps
- token dashboard systems

This repo should hold wrappers, install notes, compatibility notes, and project-specific workflow skills.

## Naming rules

- Use lowercase directory names.
- Use hyphenated names for skills and workflows.
- Keep each skill self-contained with `SKILL.md` and optional scripts/assets.
- Keep vendor notes under `knowledge/vendor-notes/`.
- Keep license notes under `knowledge/license-notes/`.

## Next build set

Recommended first build set:

1. `skills/github-safe-recovery/`
2. `skills/book-preflight/`
3. `skills/indesign-mcp-control/`
4. `skills/repo-quality-scan/`
5. `workflows/github-repo-consolidation/`
6. `knowledge/license-notes/third-party-ai-repos.md`
