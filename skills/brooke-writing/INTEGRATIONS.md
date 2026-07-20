# Integration Guide

Use `SYSTEM_PROMPT.md` as the persistent highest-priority style instruction supported by each platform.

## ChatGPT

- Save the concise identity of the framework in Memory.
- Place the full prompt in Custom Instructions, a Project instruction, or a Custom GPT instruction.
- For API applications, send it as a developer or system message.

## OpenAI API

Load `SYSTEM_PROMPT.md` into the application’s developer instruction. Keep task-specific user requests separate so they can override tone when necessary.

Conceptual message order:

```text
1. System or developer: Brooke Writing Skills
2. Developer: application-specific constraints
3. User: current writing task and source material
```

## Claude

Use the prompt in Project Instructions, a Claude Code `CLAUDE.md`, or the system prompt field of an API request.

Suggested repository placement:

```text
CLAUDE.md
.ai/styles/brooke-writing.md
```

## Gemini and NotebookLM

- Gemini: place the prompt in a Gem’s instructions or at the beginning of a dedicated writing conversation.
- NotebookLM: add the prompt as a source document and explicitly instruct the notebook to apply it when generating prose.
- NotebookLM summaries are source analysis, not a guaranteed persistent system style.

## Ollama

Embed the prompt in a Modelfile:

```text
FROM your-model
SYSTEM """
Paste the contents of SYSTEM_PROMPT.md here.
"""
```

Then create a named preset model:

```powershell
ollama create brooke-writer -f Modelfile
ollama run brooke-writer
```

## Open WebUI

Create a model preset or system-prompt preset named `Brooke Writer` and paste `SYSTEM_PROMPT.md` into the system prompt field.

## LM Studio

Create a preset with the system prompt loaded. Keep temperature moderate so rhythm remains alive without weakening factual discipline.

## VS Code, Codex, and coding agents

Store a copy in the repository as one of the agent instruction files supported by the tool:

```text
AGENTS.md
CLAUDE.md
.github/copilot-instructions.md
.ai/styles/brooke-writing.md
```

For code tasks, apply the Brooke Tone only to explanatory prose, documentation, narrative copy, and user-facing text. Do not fragment source code or sacrifice technical clarity.

## Generic LLM configuration

When a platform has only one prompt field, place this order in the prompt:

1. factual and safety requirements
2. Brooke Writing Skills
3. task instructions
4. source material
5. requested output format

## Retrieval-based deployment

For larger systems, index all files in this directory and retrieve the style prompt whenever the task involves:

- reflective essay
- memoir or personal narrative
- philosophy
- literary analysis
- artist statement
- editorial writing
- serious personal prose

Do not automatically retrieve it for troubleshooting, code, calculations, legal forms, medical summaries, or procedural instructions unless Brooke explicitly requests the style.

## Version control

Treat this directory as the canonical portable copy. Updates should be committed here and then synchronized into each provider’s persistent prompt or project instruction.
