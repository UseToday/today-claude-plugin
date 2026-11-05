---
name: prepare-customer-meeting
description: Prepare a briefing for a customer meeting using TODAY. Use when the advisor asks to prepare for a meeting, wants a customer brief, or asks what to know before talking to a customer.
---

# Prepare a customer meeting

Build a concise, source-grounded brief from the signed-in advisor's TODAY data.
Never invent facts, and never include records the advisor cannot see.

1. Identify the customer with `search`. If the name is ambiguous, ask which
   customer before continuing.
2. Optionally call `get_profile` for the advisor's name and context.
3. Call `get_customer_cumulative_facts` for the customer. This is the merged set
   of facts stated across the advisor's meetings with that customer.
4. Call `get_customer_extracted_data` for the per-meeting CRM fields.
5. Use `search` with the calls index, a past time range, and the advisor's own
   scope to find the most recent calls. Open the most relevant one with
   `get_call`.
6. Return a brief with these sections:
   - Customer snapshot
   - What TODAY knows, with the source meeting date when available
   - Recent conversations with date, attendees, and a short summary
   - Extracted CRM details
   - Suggested talking points and open questions
7. Mark missing or conflicting information instead of filling the gap. Close by
   offering to open a specific call or refresh the brief.
