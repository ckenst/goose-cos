# Shutdown Command - Questionnaire Checklist

## Command UX
- Where will `/shutdown` live first? (Codex chat command, script, slash-command wrapper, other)
- Which hosts need to support the same shutdown behavior later? (Codex, Goose, both)
- Should the command always begin with the same capture prompt?
- Should it allow multiple pastes before processing?
- Should it ask follow-up questions, or classify immediately from the pasted dump?

## Input Scope
- What counts as "temporary storage"? (scratchpad, sticky notes, tabs, text files, emails to self, etc.)
- Will the input be one freeform paste, or can you include headings and rough categories?
- Should the CoS preserve the original raw dump somewhere?

## Classification Rules
- What makes something a TODO / action item?
- What makes something a knowledgebase item?
- What makes something a calendar item?
- Can one item belong to more than one bucket?
- What should happen to ambiguous or incomplete items?

## TODO / Action Item Output
- What fields should be extracted when possible? (title, due date, priority, project, duration, notes)
- Should TODOs be phrased as verb-first tasks?
- Should the CoS infer priority, or leave it blank in v1?

## Knowledgebase Output
- Where should knowledgebase items go in v1?
- Should they be summarized, cleaned up, or stored mostly as-is?
- Should source/context be preserved verbatim?

## Calendar Output
- What counts as a calendar item versus a normal task?
- Should calendar items be events, reminders, or a review list in v1?
- What date/time details should be extracted?
- What should happen when date/time information is missing?

## Review Workflow
- Should `/shutdown` end with a single grouped summary or separate sections with confirmation?
- Do you want an approval step before anything is saved anywhere?
- How should uncategorized items be shown back to you?

## Safety & Boundaries
- Confirm: no silent dropping of items
- Confirm: preserve enough context to reconstruct intent
- Confirm: no external writes in v1 unless explicitly approved
- Confirm: core behavior should stay tool-agnostic and model-agnostic
- Any explicit "never do" rules?

## Future Integrations
- TODO destination:
- Knowledgebase destination:
- Calendar destination:
- State/history location, if any:
