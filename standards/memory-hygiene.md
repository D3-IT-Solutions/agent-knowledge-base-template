# Memory hygiene & pruning (keep assistant memory lean, put facts in the KB)

**Last reviewed:** 2026-10-25

## Why this matters

Many AI assistants (including Grok Bot, Cursor, Claude, and custom agents) have a built-in durable memory (`profile` or `shared_profile`) that gets injected into every prompt. If an assistant saves every small UI tweak, temporary task instruction, or one-off bug fix into its durable memory:

1. **Prompt bloat:** Old notes fill up the prompt window and crowd out current instructions.
2. **Stale rules override current files:** An outdated memory note from last week's iteration can contradict today's code or confirmed knowledge base note.
3. **Scattered truth:** When project specs live inside one assistant's private memory instead of this repository, other assistants cannot read or cite them.

## What belongs in assistant `profile` memory (Target cap: ≤ 25–30 facts)

Keep durable assistant memory short, non-redundant, and capped at **25–30 concise facts** per assistant:

- **Identity and role:** Who the owner is, what the business or team does, and which role this assistant plays.
- **Standing operating rules & approval gates:** What always requires a human "yes" first (sending external messages, spending money, deleting data, deploying to production).
- **Security boundaries:** How secrets and credentials are handled (for example, password manager vaults and environment variables—never in files or chat).
- **Personal workflow preferences:** How the owner likes answers formatted, when reminders are welcome, and which channels or lists to use.

## What belongs in the knowledge base or code repository instead

Do **not** save these in assistant `profile` memory:

- **Iterative website, UI, or code tweaks:** CSS changes, button labels, layout adjustments, or feature specs. Put those in the project repository and its tests.
- **One-off bug fixes or finished tasks:** Temporary debugging steps or completed ticket instructions.
- **Detailed business policies, pricing tables, or SOPs:** Write those as topic notes in this knowledge base (`business/`, `operations/`, `policies/`, `finance/`) and index them in [`index.md`](../index.md) so every assistant shares one source of truth.
- **Duplicate or superseded rules:** Before saving a new memory fact, check if an existing memory entry already covers the topic. Replace the old entry instead of adding a duplicate.

## Pruning cadence & procedure

1. **When `profile` memory exceeds ~25–30 entries (or after a multi-step build sprint):**
   - Review current memory entries.
   - Move any lasting project specifications or business rules into this knowledge base (or the project repo) and update [`index.md`](../index.md).
   - Delete (`forget`) obsolete task notes, superseded UI instructions, and duplicate facts from assistant memory.
2. **When the owner changes a rule:**
   - Update the matching note in this knowledge base and delete (`forget`) the old rule from assistant memory in the same turn so stale instructions never linger.
