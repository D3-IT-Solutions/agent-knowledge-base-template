# Standards mapping (fill-in template)

> **Core principle:** Human in the loop and deterministic automation are more important than ever with the emergence of AI. See [core-principle.md](core-principle.md).

Use this table to record what your team already does for each standard and what is left to do. Be honest: this is an internal working view, **not** a compliance or certification claim. "Evidence" should point to something a reviewer can check (a policy file, CI workflow, log, screenshot, dated test record).

Answer "Do we do this?" with **Yes / Partly / No / Not applicable**.

| Standard | Practice | Do we do this? | Evidence | To-do |
|----------|----------|----------------|----------|-------|
| Core principle | Repeatable steps run as tested scripts or CI Actions, not ad-hoc agent runs | | | |
| Core principle | A human approver signs off on going live, sending, spending, deleting, new accounts | | | |
| NIST AI RMF / AI 600-1 | Inventory of AI systems (purpose, owner, data, model/provider, last test) | | | |
| NIST AI RMF / AI 600-1 | AI systems can be overridden, disabled or rolled back | | | |
| OWASP LLM Top 10 | Fetched content treated as data, never instructions (prompt-injection defense) | | | |
| OWASP LLM Top 10 | Agents have least-privilege tools and permissions (Excessive Agency) | | | |
| OWASP LLM Top 10 | Spending caps and rate limits on model API keys | | | |
| OWASP Top 10 / ASVS | Top 10 review on every web app change; ASVS level chosen as acceptance criteria | | | |
| OWASP Top 10 / ASVS | Secret scanning, static analysis and dependency audit in CI | | | |
| NIST CSF 2.0 | Named owner for security decisions (Govern) | | | |
| NIST CSF 2.0 | Written incident response plan (Respond/Recover) | | | |
| CIS Controls v8.1 IG1 | Asset and software inventory | | | |
| CIS Controls v8.1 IG1 | MFA on all admin, email and remote accounts | | | |
| CIS Controls v8.1 IG1 | Periodic access reviews, with dates recorded | | | |
| CIS Controls v8.1 IG1 | Backups with a tested restore, with dates recorded | | | |
| CIS Controls v8.1 IG1 | Data retention and disposal policy | | | |
| ISO/IEC 42001 (reference) | Certification status recorded truthfully; no unsupported claims | | | |
| FTC Safeguards / IRS 4557 | If serving tax/financial clients: written description of your safeguards; WISP help offered without claiming compliance | | | |
| HIPAA | If serving clinics: PHI kept out of agents by default; BAA process before any PHI | | | |
| All | No secrets in repos or docs | | | |
| All | Agent actions logged and reviewable | | | |

Add rows as needed. Review this table at least yearly and after major changes.

Last reviewed: 2026-10-22
