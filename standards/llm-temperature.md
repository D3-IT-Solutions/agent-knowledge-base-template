# LLM temperature & determinism by task type

**Last reviewed:** 2026-10-25

## Why this matters

Sampling `temperature` controls how much randomness an AI model uses when choosing the next word or token:
- **Too high on operational, tax, or financial tasks (`> 0.2`):** Leads to inconsistent classifications, broken JSON schemas, non-repeatable tool calls, and invented or rounded numbers.
- **Too low on brainstorming (`0.0`):** Can make marketing copy or outreach drafts sound stiff and repetitive.

Set `temperature` explicitly by task type so deterministic work stays repeatable and creative work stays human-reviewed.

## Recommended temperature tiers by task type

| Tier | Setting | Task types | Required guardrails |
|---|---|---|---|
| **1. Deterministic ops, tax, finance & JSON** | **`temperature: 0.0`** | Tax and accounting calculations, invoice/receipt extraction, structured JSON or schema output, SQL/database queries, code and security audits, compliance checks, tool routing | **Use `0.0`.** Validate output against a schema and verify numbers with scripts or source documents. |
| **2. Grounded triage & classification** | **`temperature: 0.2`** | Front-desk call/message intake, lead qualification, support ticket routing, citing Q&A over knowledge base notes, inbox/meeting summaries | Ground answers strictly in retrieved notes; refuse or ask when a fact is missing rather than guessing. |
| **3. Conversational web assistants** | **`temperature: 0.4`** | Customer-facing website chat answering service, pricing, and scheduling questions | Bound with system-prompt rules, approved price lists, and human approval before booking or quoting custom work. |
| **4. Creative & outreach drafting** | **`temperature: 0.6 – 0.7`** | Marketing copy, blog post ideas, outreach email/social draft options, brainstorming | **Human-reviewed drafts only.** Always require owner approval before sending or publishing; never use for tool execution or financial numbers. |

## Rules for code and API calls

1. **Default to `0.0` in agent harnesses and shared utilities.** Make callers opt into higher temperatures only for conversational or creative steps.
2. **Pass `temperature` explicitly.** Do not rely on provider defaults (many APIs default to `1.0` when omitted).
3. **Split data extraction from message drafting.** Run extraction and policy/math checks at `temperature: 0.0`, then pass the verified data into the drafting step (`0.2–0.4`).

## Behavioral equivalent for host-managed assistants (like Grok Bot, Cursor, or Claude)

When you use a chat or coding assistant where the host app controls the model's sampling temperature and does not expose a numeric `temperature` setting per message, enforce **"effective temperature `0.0`"** on operational, financial, and tax work through three habits:

1. **Verify before reporting:** Read exact numbers and text from files, command output, or connected tools—never guess a number, URL, or status.
2. **Keep memory clean ([`standards/memory-hygiene.md`](memory-hygiene.md)):** Cap durable assistant memory (`profile`) at ≤ 25–30 standing rules and prune old task notes so stale context does not act like random noise.
3. **Use scripts for repeatable math and checks ([`standards/core-principle.md`](core-principle.md)):** Run deterministic scripts and tests instead of doing multi-step calculations in freehand prose.
