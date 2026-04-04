# Chief of Staff v1 - Shutdown Command Spec Starter

## Summary
We'll create a first-pass shutdown workflow centered on a `/shutdown` command.
The command should help capture everything still in your head or scattered in temporary places at the end of the day, then sort that raw dump into structured buckets.

## Desired User Flow
1. You type `/shutdown`.
2. The CoS prompts you to paste everything still on your mind and in temporary storage.
3. You paste one large brain dump.
4. The CoS classifies each item into one of three buckets:
   - TODOs / action items
   - Knowledgebase items
   - Calendar items
5. The CoS returns a structured summary for review.

## Key Product Decisions
1. Capture format
   - Should the prompt expect one freeform dump, or guide you through categories?
   - Should the command support multiple pasted chunks before processing?
2. Classification rules
   - Define the exact difference between an action item, a knowledgebase item, and a calendar item.
   - Decide what happens to ambiguous items that fit multiple buckets.
3. Output behavior
   - Decide whether v1 only returns a structured summary, or also writes into downstream systems.
   - Decide whether the output should be review-only first, with approval before any writes.

## Proposed v1 Scope
- Input: a single pasted brain dump
- Processing: parse and classify items
- Output: structured review grouped by bucket
- Safety: no automatic external writes until classification quality is trusted

## Open Integration Paths
- TODOs / action items -> Notion tasks or another task system
- Knowledgebase items -> notes store / knowledgebase destination
- Calendar items -> Google Calendar or calendar review queue

## Test Plan
1. Paste a mixed dump containing tasks, reference notes, and scheduling items.
2. Verify every line is either classified or explicitly marked ambiguous.
3. Check that calendar-worthy items keep enough detail for later scheduling.
4. Check that knowledgebase items preserve useful context rather than turning into tasks.

## Assumptions
- `/shutdown` is the first CoS command we implement.
- v1 should prioritize good capture and sorting over automation depth.
- Human review should happen before any task/calendar/knowledgebase writes.
- The shutdown workflow should be portable across Windows and Mac environments.
- The command behavior should remain tool-agnostic so it can run in Codex, Goose, or another host later.
