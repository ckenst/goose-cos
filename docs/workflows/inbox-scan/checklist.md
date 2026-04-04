# Inbox Scan Spec — Questionnaire Checklist

## Email Scope
- Which email account(s) are in scope?
    - ckenst@gmail.com, chris@kenst.com
- What is the exact search window? (timezone + start/end)
    - Inbox
- Which Gmail categories are excluded? (promotions/social/updates/forums)
    - Anything archived, not in the inbox
- Should specific senders or domains be always included/excluded?
    - No

## Actionability Rules
- What counts as “actionable” for your work?
    - Bills
    - Social media comments
    - Invoices
    - Personal emails from Cliff, Sally or Emmalin or other friends
- What types of emails should always be skipped?
    - Newsletters
    - Most notifications, but not bills
- Should follow‐ups be created for unanswered threads?
    - Yes

## Priority Framework (P1–P4)
- Define P1 with a concrete test:
- Define P2 with a concrete test:
- Define P3 with a concrete test:
- Define P4 with a concrete test:
- When uncertain, which priority should be the default?

## Due Date Heuristics
- If a deadline is mentioned explicitly, how should it be parsed?
    - It will go on my Google Calendar
- If no deadline, what default due date should be used?
    - Skip
- Should weekends be avoided for due dates?
    - No

## Duration Heuristics
- Default duration when unknown:
    - Skip
- Common task types and typical durations:

## Notion Tasks DB (New)
- Database name:
- Required fields:
- Optional fields:
- Status options:
- Priority options:
- Project/Area taxonomy:
- Link back to source email (URL field? rich text? relation?):

## De‑duplication
- What constitutes a duplicate task?
- Should completed duplicates be ignored or resurrected?
- Should a new email update an existing task’s context?

## Safety & Boundaries
- Confirm: read‑only email access
- Confirm: no email drafts/sends
- Confirm: no calendar access
- Any other explicit “never do” rules?

## State Tracking
- Where should the last‑run timestamp be stored?
- What should happen if the state file is missing or corrupted?

## Daily Review Workflow
- How should the daily summary be delivered? (console, file, email, Notion page)
    - Email
- Do you want a manual approval step before tasks are created?
    - Yes
