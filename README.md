# TODAY

Read-only access to your TODAY customers, calls, and meeting intelligence
inside Claude.

![TODAY](assets/logo.svg)

Search your customers and calls, open a specific call for attendees, summaries,
and CRM fields, and read the facts TODAY has captured across your meetings with
a customer. Every result is limited to records the signed-in advisor can already
see in TODAY. Use it to prepare for a meeting, recap what was discussed, or check
what is known about a customer. TODAY is read-only in Claude: it does not create,
edit, or delete anything.

## Use it

- "Search my customers for Bianca Sozzi."
- "Summarize my most recent calls."
- "What facts do we know about Bianca Sozzi?"
- "Help me prepare for my next meeting with Bianca Sozzi."
- "Recap my last call with Bianca and list the action items."

## Skills

| Skill | What it does |
| --- | --- |
| `prepare-customer-meeting` | Builds a pre-meeting brief from the customer's facts, recent calls, and extracted CRM data. |
| `recap-call` | Summarizes one call: attendees, discussion, decisions, action items, and CRM fields. |
| `customer-insights` | Summarizes cumulative facts and per-meeting CRM data, with gaps and conflicts called out. |

## Connect

Add the plugin, then open its **Connectors** tab and connect **TODAY**. Sign in
with your TODAY account. Claude uses OAuth 2.1 (DCR + PKCE), and the connection
receives only the `connector:read` scope. In Claude Code, `/mcp` shows the
connection state.

## Data

The plugin contains no credentials. Claude sends your request and tool arguments
to `https://mcp.usetoday.io/mcp`; TODAY returns only records the signed-in
advisor can already see. The plugin itself stores nothing. The MCP server is
operated by TODAY.

- Privacy policy: https://www.usetoday.io/legal/privacy-policy
- Terms: https://www.usetoday.io/legal/terms-and-conditions
- Support: https://help.usetoday.io/

## Maintainers

See [DEVELOPING.md](DEVELOPING.md) for the plugin layout, validation, Messages
API example, and directory submission steps.
