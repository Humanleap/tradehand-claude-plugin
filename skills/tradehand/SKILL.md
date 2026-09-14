---
name: tradehand
description: Browse UK trades and public Tradehand listings, then continue an instant quote on Tradehand.
---

Use Tradehand MCP at `https://tradehand.com/api/mcp` over Streamable HTTP.

- Public journey tools: `browse_trades`, `search_traders`, `get_trader`, `get_service_options`, `prepare_instant_quote`.
- Also listed: `get_page_markdown`, `get_agent_discovery`, `read_okf_concept` (site reading, not quoting).
- Linked tools: `get_customer_access`, `list_my_jobs`, `get_job`, `prepare_booking`; with write: `submit_instant_quote`, `prepare_quote_decision`, `confirm_quote_decision`. Host booking continues on Tradehand `/book` for the customer to review. Hosts do not commit a slot or take payment. Checkout, if shown, is pending/due — not paid.
- Instant quote works before a trader is assigned. Matching taken is not an appointment.
- Named listing intent must be `preferred` or `exclusive`. A profile click is not exclusivity.
- Anonymous `prepare_instant_quote` validates only. Linked write scope may persist a reviewable preparation; it still does not text, charge, or assign.
- `submit_instant_quote` takes `preparationToken`, `expectedRevision`, `idempotencyKey`, and `confirmationReference` only. Never pass session tokens, contact ids, or `confirmed: true`. First-party continue is `/instant-quote?prep=` — same customer reviews stored facts and sends.
- Prices and assignment come from tool results. Never invent them.
- Missing backend config is `service_unavailable`, not an empty job list.
- Do not start checkout, deposits, or refunds. Anthropic financial-transaction permission is separate and not granted here.
