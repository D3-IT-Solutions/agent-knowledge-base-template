# Bot Squad™ Agent Knowledge Base Template

[![Version](https://img.shields.io/badge/Bot%20Squad%E2%84%A2%20Starter%20Kit-v1.0.0-0f172a)](https://github.com/D3-IT-Solutions/agent-knowledge-base-template/archive/refs/heads/main.zip)
[![Download ZIP](https://img.shields.io/badge/Download-Bot%20Squad%E2%84%A2%20Template%20(.zip)-2563eb)](https://github.com/D3-IT-Solutions/agent-knowledge-base-template/archive/refs/heads/main.zip)
[![License: MIT](https://img.shields.io/badge/License-MIT-16a34a.svg)](LICENSE)

**Bot Squad™ Agent Knowledge Base Template** (by **D3 IT Solutions Inc**) is a downloadable software template and electronic configuration file starter kit for multi-agent AI assistants. It provides structured Markdown templates, operating standards, automation registries, and prompt instructions so a team of AI agents shares one verified source of truth.

### Direct Download (Bot Squad™ Starter Kit v1.0)

- **[⬇ Download the Bot Squad™ Template (.zip)](https://github.com/D3-IT-Solutions/agent-knowledge-base-template/archive/refs/heads/main.zip)** — Direct download of the complete **Bot Squad™** electronic data files, Markdown configuration templates (`_templates/topic-template.md`, `index.md`, `AGENT_GUIDE.md`), guardrail standards, and folder structure.
- **[Use this repository as a GitHub Template](https://github.com/D3-IT-Solutions/agent-knowledge-base-template/generate)** — Create a private copy in your own GitHub account.

---

This is a starter kit for a plain folder of Markdown notes. The notes are the source of truth for your AI assistants. When an assistant answers a question about how you work, it reads the note and cites it, instead of guessing or asking you the same thing again.

The sample pages here are examples. They are not your rules. Replace them with your own words.

If you want an assistant to build the notes with you, paste this into a new chat:

```
Read AGENT_GUIDE.md and help me build my knowledge base.
```

## Why this helps

- **One source of truth.** A rule lives in one file. Two assistants do not invent two versions of it.
- **Fewer repeated questions.** You explain something once. The next assistant reads the file.
- **Cited answers.** An assistant that uses a note tells you the file name and the link inside it, so you can check the answer.

## Folder layout

Each topic area is a folder. Each topic is one Markdown file inside that folder.

```
.
├── index.md                Map of every note, standard, automation, and published article
├── AGENT_GUIDE.md          How an assistant should interview you and write notes
├── CONTRIBUTING.md         Short rules for edits
├── SECURITY.md             What must never be committed
├── LICENSE
├── _templates/
│   └── topic-template.md   Copy this when you add a topic
├── business/               What the work is, who it is for, what you will not do
├── operations/             How a request starts, moves, and finishes
├── finance/                Invoice timing and spending rules, in words
├── customers/              Tone, promises, and what a new customer should know
├── policies/               Decisions you have already made
├── standards/              Industry standards and rules for how agents work (start with core-principle.md)
├── automation/             When to script vs use an agent, the tool registry, and automation ideas
└── personal/               How you like assistants to work with you
```

Every area folder has a short `README.md` that says what belongs there. Files whose names start with `example-` are patterns. Assistants must not cite them as your decisions. Delete an example when you no longer need the pattern.

## Use this repository as a GitHub template

GitHub can copy this starter into a new repository for you.

1. Turn on **Template repository** under this repository's **Settings → General**. That is a one-time step for the person who published the starter. GitHub explains the switch here: [Creating a template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository).
2. Click **Use this template**, or open [this link](https://github.com/D3-IT-Solutions/agent-knowledge-base-template/generate).
3. Name the new repository. Choose **Private** when it will hold real notes about you or your work. Public is fine for practice with the examples only.
4. In the new repository, open a chat with your assistant and paste the prompt above.

If the button is missing, the template switch is still off. You can still copy these files into a new repository of your own. Point later assistants at **your** repository, not at this empty starter.

More help: [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

## Add a topic yourself

1. Copy `_templates/topic-template.md` into the folder that fits.
2. Rename the copy with lowercase words and hyphens, such as `how-a-request-moves.md`.
3. Fill in the block at the top and the sections below it. Leave **status** as `draft` until you have read the file and the words are right.
4. Ask your assistant to follow `AGENT_GUIDE.md` if you would rather talk it through.
5. Add a row for the new file in `index.md` so assistants can find it from one place.

The block between the two `---` lines is called front matter. It is a short list of facts (title, status, owner, last reviewed, sources) that an assistant can read quickly. Under that, the note has a summary, details, and open questions, written for a person.

## How assistants should cite and update

- Cite the file path, the status (`draft` or `confirmed`), and the source link in the note.
- When the status is `draft`, say the note is not settled yet.
- Change a confirmed note with a pull request (a suggested edit you can accept or reject), or add a dated line to that file's change log and set the status back to `draft` until you agree.
- Keep each file to one topic. Label any guessed number as an estimate, and leave numbers out when you do not have them.

The full steps are in `AGENT_GUIDE.md`.

## Security

This starter is public and contains no real personal or business facts. Your filled-in copy should be a **private** repository. Do not commit passwords, ID numbers, account numbers, or home addresses. Read [SECURITY.md](SECURITY.md) before you add real notes.

## License & Trademark Notice

[MIT](LICENSE). You can copy this starter, change it, and share it.

**Bot Squad™** and **D3 Bot Squad™** are trademarks of **D3 IT Solutions Inc** ([d3itsolutions.net](https://www.d3itsolutions.net)). © 2026 D3 IT Solutions Inc. All rights reserved.
