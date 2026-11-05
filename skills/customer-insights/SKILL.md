---
name: customer-insights
description: Summarize what TODAY knows about a customer, including cumulative facts and extracted CRM data. Use when the advisor asks what facts, needs, requirements, or CRM details were captured about a customer.
---

# Customer insights

Summarize the advisor's captured knowledge about one customer. Use only TODAY
data the signed-in advisor can see, and keep the plugin read-only.

1. Find the customer with `search`. If the name is ambiguous, ask which customer
   before continuing.
2. Call `get_customer_cumulative_facts` for the customer.
3. Call `get_customer_extracted_data` for the per-meeting CRM fields.
4. Return:
   - Confirmed facts grouped by theme such as needs, goals, constraints,
     preferences, and key people
   - Per-meeting extracted CRM fields with the meeting date
   - Conflicts or items that may be stale
   - Gaps worth asking about next time
5. Attribute each fact to its meeting or date when the record provides one.
   Never present an inference as a customer statement.
6. If the customer has no captured facts or extracted data, say so plainly and
   suggest searching their calls.
