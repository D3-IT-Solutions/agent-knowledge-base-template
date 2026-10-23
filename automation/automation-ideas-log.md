# Automation ideas: log repeated work

This page is your team's logging rule for repeated work: if a task has been done by hand more than once, or uses a lot of tokens, log it as an idea so it can be considered for a script, routine or connector. Background: the [core principle](../standards/core-principle.md) favors deterministic automation for repeatable steps, with a person approving anything consequential.

## When to log an idea

Log an idea when either is true:

- A task has been done by hand **more than once**.
- A task uses **a lot of tokens** (AI usage) for work that follows the same steps each time.

Check the [tool registry](tool-registry.md) first; the tool may already exist.

## Where to log it

Pick one place and write it here: an issue tracker with an `automation-candidate` label works well, or a single ideas file. Copy [automation-ideas-template.md](automation-ideas-template.md) for each idea. See [examples.md](examples.md) for the shape.

- Ideas go in: _(fill in)_

## What each idea must say

| Item | What to write |
|---|---|
| What is repeated | The task and its steps, in plain words |
| How often | How many times it has happened and when (dates or links), not an estimate of savings |
| Who does it now | Which person or assistant |
| Suggested builder and approver | Who would build and run it, and who would accept its runs (never the same) |
| Proposed automation | A script, a routine (scheduled or repeated agent run), or a connector, and roughly what it would do |
| Human approval | Which step stays with a person |
| Inputs and outputs | What it reads and what it produces |
| Risks | What could go wrong if it ran unattended |
| Done when | What a good run looks like (feeds the [promotion rule](promotion-rule.md)) |

Do not invent time or money savings. If you count something, link where the count came from.

## What happens next

1. Whoever coordinates the work (or the owner) reviews new ideas on a set rhythm, such as weekly, and brings the top picks to the owner.
2. **Nothing gets built until the owner picks it.** Logging an idea is not approval to build.
3. When the owner picks one, they name a **builder** and an **approver**. The approver is the owner or a person they name, and is never the builder. The builder builds it on a branch, adds a `draft` registry entry ([tool-registry.md](tool-registry.md)), and follows the [promotion rule](promotion-rule.md); only the approver accepts runs and promotes it.
4. Ideas the owner does not pick stay open or get closed with a short reason.

Last reviewed: 2026-10-22
