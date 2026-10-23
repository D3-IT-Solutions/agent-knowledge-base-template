# Automation

How your assistants decide what to automate, find tools that already exist, log new automation ideas, and get a new automation accepted. Read [../standards/core-principle.md](../standards/core-principle.md) first:

> "Human in the loop and deterministic automation are more important than ever with the emergence of AI."

| Page | What it covers |
|------|----------------|
| [when-script-vs-agent.md](when-script-vs-agent.md) | Script, agent or person: who does which kind of step (decision table) |
| [tool-registry.md](tool-registry.md) | Check your tool registry before doing a task by hand; add an entry when you build a reusable tool |
| [automation-ideas-log.md](automation-ideas-log.md) | When and how to log repeated work as an automation idea |
| [promotion-rule.md](promotion-rule.md) | A new automation stays a draft until its approver (never its builder) accepts two good runs |
| [registry-template.yaml](registry-template.yaml) | Commented example registry to copy (entries are labeled EXAMPLE) |
| [automation-ideas-template.md](automation-ideas-template.md) | Fill-in template for one automation idea |
| [examples.md](examples.md) | Four illustrative EXAMPLE ideas for a small business |

Order of operations for any task:

1. Check the registry ([tool-registry.md](tool-registry.md)). If a tool exists, use it.
2. If not, decide script vs agent vs person ([when-script-vs-agent.md](when-script-vs-agent.md)).
3. If you did it by hand and it repeats, log an idea ([automation-ideas-log.md](automation-ideas-log.md)).
4. Once the owner picks it, the builder builds it, and it stays a draft until the approver (never the builder) accepts two good runs under the [promotion rule](promotion-rule.md).

Assistants must not cite anything labeled EXAMPLE as the owner's decision.

Last reviewed: 2026-10-22
