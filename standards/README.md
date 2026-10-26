# Standards

Reference pages in clear, everyday words on industry standards that matter when AI assistants or agents help run a small business. Each page says what the standard is, links the official source, and ends with concrete rules for how agents should work.

These are summaries, not legal or compliance advice, and using them does not make anyone certified or compliant. Check the official text before relying on a page, and re-check versions at least once a year.

Start with the core principle:

| Page | Standard | Why it matters |
|------|----------|----------------|
| [core-principle.md](core-principle.md) | Human in the loop + deterministic automation | The rule the other pages build on: scripts for repeatable steps, agents for judgment, a human approver for anything consequential |
| [memory-hygiene.md](memory-hygiene.md) | Memory hygiene & pruning (≤ 25–30 `profile` facts) | Keep assistant memory lean for standing rules only; put project specs in the KB/repo and prune obsolete task notes |
| [llm-temperature.md](llm-temperature.md) | LLM temperature by task type (`0.0` / `0.2` / `0.4` / `0.6–0.7`) | Set `0.0` for deterministic ops/tax/JSON, `0.2` for triage, `0.4` for web chat, and `0.6–0.7` for human-reviewed creative drafts |
| [nist-ai-rmf.md](nist-ai-rmf.md) | NIST AI RMF 1.0 + AI 600-1 (GenAI Profile) | Free US framework for managing AI risk |
| [owasp-llm-top-10-2025.md](owasp-llm-top-10-2025.md) | OWASP Top 10 for LLM Applications 2025 | Top security risks for chat and phone agents (prompt injection, excessive agency) |
| [owasp-top-10-and-asvs.md](owasp-top-10-and-asvs.md) | OWASP Top 10:2025 + ASVS 5.0.0 | Review checklist and acceptance criteria for websites and web apps |
| [nist-csf-2.md](nist-csf-2.md) | NIST CSF 2.0 | Common language for security (Govern, Identify, Protect, Detect, Respond, Recover) |
| [cis-controls-v8-ig1.md](cis-controls-v8-ig1.md) | CIS Controls v8.1 IG1 | Practical small-business security baseline (56 safeguards) |
| [iso-iec-42001.md](iso-iec-42001.md) | ISO/IEC 42001:2023 (reference only) | How to answer questions about AI management certification truthfully |
| [ftc-safeguards-and-irs-4557.md](ftc-safeguards-and-irs-4557.md) | FTC Safeguards Rule (16 CFR 314) + IRS Pub 4557 | Rules for tax, accounting and other financial clients |
| [hipaa-basics.md](hipaa-basics.md) | HIPAA Privacy, Security, Breach Notification | Rules for clinic clients; when a BAA is needed |
| [mapping-template.md](mapping-template.md) | All of the above | Fill-in table: what you do today, evidence, and to-dos |

Copy `mapping-template.md` into a new file (or fill it in place) to record your own practices. Update each page's "Last reviewed" date when you re-check it.
