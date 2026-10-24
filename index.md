# Knowledge base index

This file is the single-page map of your knowledge base. Assistants read `index.md` first to find the right note without scanning every folder, and update `index.md` whenever a note is added, confirmed, or retired.

**Statuses:**
- **`draft`** = written, waiting for the owner's review and confirmation (cite with a warning that it is not settled yet).
- **`confirmed`** = read and approved by the owner (safe to cite as the owner's rule).
- **`example`** = starter pattern only — never cite as the owner's rule. Remove an `example` row when a real note replaces it.

## Topic Notes

| Topic | Folder | Status | Owner | Last reviewed |
|---|---|---|---|---|
| [Example: What this work is](business/example-what-this-work-is.md) | `business/` | `example (do not cite)` | owner | YYYY-MM-DD |
| [Example: How a request moves](operations/example-how-a-request-moves.md) | `operations/` | `example (do not cite)` | owner | YYYY-MM-DD |
| [Example: When invoices go out](finance/example-when-invoices-go-out.md) | `finance/` | `example (do not cite)` | owner | YYYY-MM-DD |
| [Example: How messages should sound](customers/example-how-messages-should-sound.md) | `customers/` | `example (do not cite)` | owner | YYYY-MM-DD |
| [Example: What needs a yes first](policies/example-what-needs-a-yes-first.md) | `policies/` | `example (do not cite)` | owner | YYYY-MM-DD |
| [Example: How I like help](personal/example-how-i-like-help.md) | `personal/` | `example (do not cite)` | owner | YYYY-MM-DD |

## Standards

Industry standards and how they apply to your assistants and client work. Start with the core principle. These are reference pages, not policy decisions, and using them does not make anyone certified or compliant.

| Page | Standard | Why it matters |
|---|---|---|
| [standards/core-principle.md](standards/core-principle.md) | Core principle (human in the loop + deterministic automation) | The rule every other page builds on: scripts for repeatable steps, agents for judgment, a person approves anything consequential |
| [standards/nist-ai-rmf.md](standards/nist-ai-rmf.md) | NIST AI RMF 1.0 + AI 600-1 (GenAI Profile) | Free US framework for managing AI risk in your assistants and client AI workflows |
| [standards/owasp-llm-top-10-2025.md](standards/owasp-llm-top-10-2025.md) | OWASP Top 10 for LLM Applications 2025 | Top security risks for chat/phone agents and assistant teams (prompt injection, excessive agency) |
| [standards/owasp-top-10-and-asvs.md](standards/owasp-top-10-and-asvs.md) | OWASP Top 10:2025 + ASVS 5.0.0 | Review checklist and acceptance criteria for websites and web apps |
| [standards/nist-csf-2.md](standards/nist-csf-2.md) | NIST CSF 2.0 | Common framework for cybersecurity outcomes (Govern, Identify, Protect, Detect, Respond, Recover) |
| [standards/cis-controls-v8-ig1.md](standards/cis-controls-v8-ig1.md) | CIS Controls v8.1 IG1 | Practical small-business security baseline (56 safeguards) |
| [standards/iso-iec-42001.md](standards/iso-iec-42001.md) | ISO/IEC 42001:2023 (reference only) | How to answer client questions about AI management systems truthfully without claiming certification |
| [standards/ftc-safeguards-and-irs-4557.md](standards/ftc-safeguards-and-irs-4557.md) | FTC Safeguards Rule (16 CFR 314) + IRS Pub 4557 | Rules tax and accounting firms must follow when handling customer financial data |
| [standards/hipaa-basics.md](standards/hipaa-basics.md) | HIPAA Privacy, Security, Breach Notification | Rules for clinic work; when a BAA is needed; keep PHI out of assistants by default |
| [standards/mapping-template.md](standards/mapping-template.md) | Standards mapping (fill-in template) | Internal checklist to record what your team already does per standard and what is left to do |

## Automation

How assistants check for existing tools, log repeated work as automation ideas, and get new automations accepted. Start with [automation/README.md](automation/README.md).

| Page | What it covers |
|---|---|
| [automation/README.md](automation/README.md) | Overview of how your assistants decide what to automate and where each file fits |
| [automation/when-script-vs-agent.md](automation/when-script-vs-agent.md) | Script for steps that must be right every time, agent for judgment work, a person for decisions that matter |
| [automation/tool-registry.md](automation/tool-registry.md) | Check your tool registry before doing a task by hand; add an entry when you build a reusable tool |
| [automation/automation-ideas-log.md](automation/automation-ideas-log.md) | When and how to log repeated work as an automation candidate; nothing is built until the owner picks it |
| [automation/promotion-rule.md](automation/promotion-rule.md) | A new automation stays `draft` until its approver accepts two good runs; the approver is never the builder |
| [automation/examples.md](automation/examples.md) | Four illustrative `EXAMPLE` automation ideas for a small business (do not cite as real decisions) |

## Published Content & Articles (Optional)

Index your live blog posts, guides, or public documentation here so assistants can cite and share your real URLs without guessing links. Remove the example row below when you add your first real article.

| Title & Link | Slug / Source | Date | Summary | When to share |
|---|---|---|---|---|
| _Example: How We Handle New Requests_ (`https://example.com/blog/how-we-handle-requests` — replace with a real URL) | `/blog/how-we-handle-requests` | YYYY-MM-DD | _Example row only (do not cite)._ One-sentence summary of what the article explains. | _Example:_ When a customer asks what happens after they submit a request |
