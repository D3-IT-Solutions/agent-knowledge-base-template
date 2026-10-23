# Promotion rule: two good runs, accepted by the approver

A new routine or automation stays **`draft`** until its **approver** accepts **two good runs**. Only then does its registry entry ([tool-registry.md](tool-registry.md)) change to **`accepted`**.

This keeps the [core principle](../standards/core-principle.md): automation is trusted only after a person has checked what it actually did.

## Roles

| Role | Who | Does |
|---|---|---|
| **Builder** | The person or assistant that makes the automation | Builds it, runs it, records each run, keeps the registry entry up to date |
| **Approver** | The owner, or a person the owner names for that automation. Never the builder. | Checks each run's output, gives or withholds the OK, and promotes the entry from `draft` to `accepted` |

Both are named in the registry entry (`builder`, `approver`).

## What a good-run record includes

The builder records each run where the idea or the build is tracked (an issue comment, a pull request comment, or a dated line in the idea file) and links it from the registry entry's `accepted_runs` field:

| Item | What to write |
|---|---|
| Date | When it ran (YYYY-MM-DD, with time and zone if it matters) |
| What ran | The exact command or routine, its version, and the inputs |
| Output link | Link to the output, log, report or file it produced |
| Approver's OK | The approver's explicit acceptance, with name and date |

A run is not "good" if it needed a hand fix, skipped a step, or its output was not checked.

## Rules

- **Nobody accepts their own work.** The builder, or anyone (person or assistant) who ran the automation, can never be the approver for it. Only the approver accepts runs and changes the status to `accepted`.
- Two good runs must be separate runs on real (or realistic) inputs, not the same run counted twice.
- Any change to what the automation does (new steps, new outputs, new permissions) puts it back to `draft` until the approver accepts two new good runs.
- `accepted` does not remove the human approval step. If the entry says a person sends or approves, that still holds.

Last reviewed: 2026-10-22
