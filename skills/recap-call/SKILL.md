---
name: recap-call
description: Recap a specific customer call from TODAY. Use when the advisor asks what was discussed on a call, wants a meeting recap, or asks for attendees, decisions, or action items from a call.
---

# Recap a call

Recap one call from the signed-in advisor's TODAY data. Stay read-only and do
not add details the call record does not contain.

1. Find the call with `search` using the calls index, a past time range, and the
   advisor's own scope. Match on customer, date, or topic.
2. If several calls match, list them with customer and date and ask which one to
   open.
3. Call `get_call` for the selected call.
4. Summarize:
   - Purpose and context
   - Attendees
   - Key discussion points
   - Decisions made
   - Action items only when the record states them
   - Extracted CRM fields
5. Separate what was said from what you infer. Do not invent action items,
   owners, or due dates. State which sections are missing.
6. Offer next steps, such as reading the customer's cumulative facts or preparing
   for the next meeting.
