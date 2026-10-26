# AGENTS.md — Bot Squad™ Agent Knowledge Base

This repository is the shared source of truth for AI assistants working with the owner.

## 1. Read First
1. [`index.md`](index.md) — Single-page map of every topic note, standard, automation rule, and published article. Read `index.md` first before scanning folders.
2. [`AGENT_GUIDE.md`](AGENT_GUIDE.md) — How to interview the owner, write and cite topic notes, manage `draft` vs. `confirmed` statuses, and keep `index.md` in sync.
3. [`SECURITY.md`](SECURITY.md) — Strict rules on secrets, credentials, and personal data that must never be committed.
4. [`standards/core-principle.md`](standards/core-principle.md), [`standards/memory-hygiene.md`](standards/memory-hygiene.md), & [`standards/llm-temperature.md`](standards/llm-temperature.md) — Core operating guardrails, memory hygiene rules, and task-tiered LLM temperature settings (`0.0` deterministic ops/tax/JSON, `0.2` triage, `0.4` web chat, `0.6–0.7` human-reviewed creative drafts).

## 2. Memory Hygiene & Pruning Rule
- **Keep durable assistant memory (`profile`) lean (≤ 25–30 concise facts).** Only save standing operating rules, identity/role boundaries, security rules, and explicit owner preferences in durable memory.
- **Do not save iterative UI tweaks, one-off bug fixes, or temporary task specs in `profile` memory.** Put lasting project specs and policies into this knowledge base (or the code repository) and index them in [`index.md`](index.md).
- **Prune stale or duplicate memory facts** whenever `profile` exceeds ~25–30 entries, after a multi-turn build sprint, or whenever the owner updates an existing rule. See [`standards/memory-hygiene.md`](standards/memory-hygiene.md).

## 3. Citing & Updating Notes
- Always cite the file path, `status` (`draft` or `confirmed`), and `last_reviewed` date when answering from this knowledge base.
- Never cite `example-*.md` starter files as the owner's actual rules.
- Update [`index.md`](index.md) in the same commit or pull request whenever a note is added, confirmed, or retired.
