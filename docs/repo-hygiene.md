# Repository Hygiene

Purpose: keep `structured-intelligence` organized as the central AI-skills workspace without turning it into a dumping ground.

## Cleanup principles

1. Keep source repositories intact until reviewed.
2. Prefer wrapper skills and workflow notes before source imports.
3. Keep third-party source out of this repo until license review is complete.
4. Keep private/session/local files out of public Git history.
5. Keep generated outputs separate from source materials.
6. Every new skill, agent, workflow, or knowledge area must have a clear purpose file.

## Required top-level roles

| Path | Role |
|---|---|
| `agents/` | Task-specific agents with prompts, config, and smoke tests. |
| `skills/` | Reusable capability bundles with `SKILL.md`, config, scripts, references, and assets. |
| `workflows/` | End-to-end operating playbooks. |
| `knowledge/` | Reusable source notes, vendor notes, license notes, connector notes, and generated summaries. |
| `prompts/` | Reusable prompt templates and prompt-analysis notes. |
| `scripts/` | Validation, installation, scaffolding, and audit automation. |
| `docs/` | Architecture, reports, repo maps, and public documentation. |

## What belongs here

- Original Brooke workflows
- Original AI skills and agents
- Original repo-cleanup maps
- Original InDesign/book production wrappers
- Original GitHub safety workflows
- Original prompt cleanup and attribution notes
- License summaries and vendor reference notes

## What does not belong here

- API keys or `.env` files
- private memory databases
- local session transcripts
- personal medical, school, or family records
- raw book source packages unless intentionally public
- unreviewed third-party source code
- full cloned app repositories pasted inside this repo
- generated cache folders
- build artifacts without a clear reason

## File naming rules

- Directory names: lowercase hyphen case.
- Skill directories: `skills/example-skill/`.
- Workflow directories: `workflows/example-workflow/`.
- Knowledge notes: grouped by topic, for example `knowledge/license-notes/`.
- Avoid spaces in file and directory names.
- Avoid vague names such as `misc`, `stuff`, `new`, `old`, or `backup`.

## Skill checklist

Each skill should include:

```text
skills/<skill-name>/
  SKILL.md
  config.yaml or metadata.yaml if needed
  examples/ if useful
  scripts/ only when original, safe, and tested
  references/ when source notes are needed
```

Before committing a skill:

- Confirm it has a clear trigger/use case.
- Confirm it does not copy third-party code without license review.
- Confirm any scripts are read-only or clearly labeled if they modify files.
- Confirm no local absolute paths are required unless documented as examples.

## Workflow checklist

Each workflow should include:

```text
workflows/<workflow-name>/
  WORKFLOW.md
  checklist.md if needed
  examples/ if useful
```

Before committing a workflow:

- Confirm it has a safety section.
- Confirm destructive commands are absent or explicitly blocked.
- Confirm expected outputs are listed.
- Confirm the workflow can be followed on Windows, macOS, or phone-mode where relevant.

## Knowledge checklist

Knowledge files should be summaries, maps, or notes. They should not become a private dumping area.

Before committing knowledge files:

- Check that the material is safe to make public.
- Include attribution when referencing an upstream repo or author.
- Prefer summaries and links over copied source text.
- Keep license notes with the knowledge item when possible.

## Cleanup pass order

Use this order for future cleanup branches:

1. Scan for secrets and local files.
2. Update `.gitignore` for generated/private artifacts.
3. Add or update repo maps.
4. Add missing purpose files.
5. Normalize names only after confirming references will not break.
6. Move files only on a dedicated branch.
7. Delete nothing unless a backup branch exists and Brooke explicitly approves.

## Current no-delete rule

This repo should not be cleaned by deleting content first. The first cleanup pass is documentation, ignore rules, maps, and structure protection. Removal/archive decisions should happen only after a separate inventory PR.
