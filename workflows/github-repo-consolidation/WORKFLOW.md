# GitHub Repo Consolidation Workflow

Purpose: consolidate Brooke's AI, prompt, MCP, memory, and skill materials into `structured-intelligence` without deleting source repositories or mixing incompatible licenses.

## Safety posture

This workflow is non-destructive.

- Do not delete source repositories.
- Do not remove files from source repositories during discovery.
- Do not import third-party source code before license review.
- Do not merge generated tools into active skills without testing.
- Do not publish private memory, session logs, API keys, credentials, school documents, or private book assets.

## Phase 1 — Inventory

For each candidate repo, record:

```text
repo:
default branch:
size:
visibility:
primary purpose:
language/runtime:
license:
contains skills:
contains prompts:
contains workflows:
contains MCP/server code:
contains private/local material:
recommended action:
```

## Phase 2 — Classify

Use these categories:

| Category | Meaning | Action |
|---|---|---|
| `canonical` | Belongs natively in `structured-intelligence` | Build here |
| `wrapper` | Useful tool but source should stay separate | Write skill wrapper here |
| `reference` | Useful knowledge source | Add summary and link |
| `vendor` | External package or app | Keep separate, document install/use |
| `hold` | Not enough information yet | Do not move |
| `archive-candidate` | Old or redundant, but not deleted | Mark only after backup |

## Phase 3 — License review

Before copying anything, check:

- license file
- README license badge
- package metadata
- third-party authorship notes
- whether assets are included
- whether prompts are externally authored
- whether terms are commercial, noncommercial, copyleft, or permissive

If license is unclear, summarize and link only.

## Phase 4 — Build wrappers first

Preferred first consolidation is original wrapper skills, not source imports:

```text
skills/github-safe-recovery/
skills/book-preflight/
skills/indesign-mcp-control/
skills/repo-quality-scan/
skills/license-review/
skills/prompt-library-cleanup/
```

Each skill should include:

```text
SKILL.md
config.yaml or metadata.yaml when needed
examples/
scripts/ only if original and tested
```

## Phase 5 — Create repo map

Update:

- `docs/repo-quality-report.md`
- `docs/ai-skills-map.md`
- `knowledge/license-notes/third-party-ai-repos.md`

## Phase 6 — Validate

Run repo validation before merge:

```bash
./scripts/validate_structure.sh
```

If validation is unavailable locally, manually check:

- each new directory has a clear README or SKILL file
- no empty placeholder folders were committed
- no binary/private files were added accidentally
- license notes are present for third-party references
- paths follow lowercase hyphen naming

## Phase 7 — Merge discipline

Use a pull request for each consolidation wave:

1. Inventory and docs only
2. Wrapper skills
3. Install scripts
4. Prompt cleanup
5. Optional vendor/reference updates

Do not combine repo cleanup, source imports, and new skills in one PR.

## Current branch plan

Branch: `ai-skills-consolidation`

First PR should include documentation only:

- repo quality report
- AI skills map
- third-party license notes
- this workflow

After that PR is reviewed, create a second branch for the first wrapper skill set.
