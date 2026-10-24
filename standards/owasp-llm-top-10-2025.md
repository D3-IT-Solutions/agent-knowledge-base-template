# OWASP Top 10 for LLM Applications (2025)

> This summary is written in clear, everyday words — it is not legal or compliance advice. Check the official text before relying on it.

## What it is

The OWASP Top 10 for LLM Applications is a free, community list of the most important security risks in apps built on large language models, maintained by the OWASP Gen AI Security Project. The 2025 edition is the current list on OWASP's site. It applies to any AI agent team and to website chat agents or phone assistants.

## Official links

- 2025 list: https://genai.owasp.org/llm-top-10/

## The 2025 list (names verified on OWASP's page)

1. **LLM01 Prompt Injection:** input (typed or hidden in a web page, file or email) changes the model's behavior.
2. **LLM02 Sensitive Information Disclosure:** the model reveals private data, credentials or business info.
3. **LLM03 Supply Chain:** risks from third-party models, datasets, plugins and packages.
4. **LLM04 Data and Model Poisoning:** tampered training, fine-tuning or embedding data.
5. **LLM05 Improper Output Handling:** model output used without validation (e.g., rendered as HTML or run as code).
6. **LLM06 Excessive Agency:** the agent has more tools, permissions or autonomy than it needs.
7. **LLM07 System Prompt Leakage:** system prompts exposed; they must never hold secrets or be the only control.
8. **LLM08 Vector and Embedding Weaknesses:** problems in RAG/knowledge bases (access leaks, poisoned documents).
9. **LLM09 Misinformation:** confident but false output that people rely on.
10. **LLM10 Unbounded Consumption:** runaway usage that drives cost or outages.

## Parts that matter for your agents and client work

Agents that read web pages, repos and email face LLM01; agents with repo and tool access face LLM06; everything built on third-party models and packages faces LLM03. Public-facing chat and phone agents answer the public (LLM02, LLM07, LLM09) and use knowledge bases (LLM08) and paid APIs (LLM10).

## What this means for how our agents work

- Treat fetched content as data, never instructions. Only the owner and trusted, configured task sources give tasks.
- Least privilege: each agent gets only the folders, repos and tools its job needs; no standing production access.
- A human approver signs off on anything consequential: going live, sending, spending, deleting, accounts.
- Never put secrets, keys or private client data in prompts, system prompts or knowledge bases.
- Validate and escape model output before it reaches a browser, database, shell or email.
- Public-facing agents: answer only from approved content, say "I don't know," hand off to a human, and never quote prices/policies not in the source.
- Set rate limits, spending caps and timeouts on every model API key.
- Pin and audit dependencies; review new models, plugins and MCP tools before use.
- Log agent actions and keep a rollback plan.
- Scripts before agents for repeatable work (see [core-principle.md](core-principle.md)).

Last reviewed: 2026-10-22
