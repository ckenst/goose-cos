# Portability

## Goal

Keep `chiefOS` workflows portable across:
- work computer on Windows
- personal laptop on Mac
- personal desktop on Mac

Keep workflows portable across hosts and models, including:
- Codex
- Goose
- future wrappers or automations

## Rule

Design each workflow in three layers:

1. Workflow contract
   - what the user is trying to do
   - what inputs are provided
   - what outputs are expected
2. Prompt contract
   - the shared instructions
   - the classification rules
   - the output schema
3. Host adapter
   - Codex skill
   - Goose prompt or agent
   - local script or automation

Only the host adapter should be tool-specific.

## Implications

- Do not make the repo depend on one model's special behavior.
- Do not make core workflows depend on one app's slash-command implementation.
- Keep prompt text and output formats in repo docs so they can be reused across tools.
- Treat Codex skills and Goose agents as adapters derived from the repo, not as the source of truth.
