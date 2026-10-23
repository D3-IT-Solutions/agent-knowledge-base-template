# Tool registry: check before you do it by hand

Keep one list of your reusable scripts, routines and connectors so an assistant does not rebuild or hand-run something that already exists. Start from [registry-template.yaml](registry-template.yaml).

## Where it is

Pick one place for the registry and write it here, for example a `registry.yaml` file in a private repository your assistants can read. Search it with your editor's search or a command-line search tool (for example `rg -i <keyword> registry.yaml`).

- Registry location: _(fill in)_
- How to search it: _(fill in)_

## Before you start a task

1. Search the registry for the task (try two or three keywords: the tool, the output, the kind of customer).
2. If an entry fits and its status is `accepted`, use it as written in its `how_to_run` field. Do not hand-run the steps instead.
3. If the entry is still `draft`, you may use it, but treat its output as unverified and say so.
4. If nothing fits, do the task, then decide whether it should become an idea ([automation-ideas-log.md](automation-ideas-log.md)).

## When you build a reusable tool, add an entry

Add the entry in the same change (pull request) as the tool. Every entry needs:

| Field | What to write |
|---|---|
| `id` | Short unique slug, lowercase with hyphens |
| `name` | Plain-language name |
| `kind` | `script`, `routine` (a scheduled or repeated agent run), or `connector` |
| `builder` | The person (or assistant role) that built it and runs it |
| `approver` | The person who accepts its runs and promotes it (the owner or someone they name); never the builder |
| `status` | `draft` until it passes the [promotion rule](promotion-rule.md), then `accepted` |
| `location` | Where the code or instructions live |
| `how_to_run` | The exact command or steps |
| `inputs` | What it needs |
| `outputs` | What it produces and where |
| `human_approval` | Which step a person approves (for example "a person sends"), or `none` if it only reads and reports |
| `accepted_runs` | Links to the good-run records (see [promotion-rule.md](promotion-rule.md)) |
| `last_reviewed` | Date (YYYY-MM-DD) |

Never put secrets, tokens, account numbers or customer personal data in an entry. Point to where a secret is stored, not the secret.

Last reviewed: 2026-10-22
