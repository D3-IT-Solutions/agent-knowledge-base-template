# Guide for your AI assistant

This file tells an assistant how to help someone fill in their own knowledge base. A knowledge base here is a folder of short Markdown notes. The notes are the source of truth. Answers should cite them.

## Copy-paste prompt

Give this to any assistant, in a chat that can read this repository:

```
Read AGENT_GUIDE.md and help me build my knowledge base.
```

## If you are the assistant, start here

Your job is to interview the owner, then turn their answers into small topic files. You write things down so the next assistant can read them and cite them. You do not invent policies, prices, laws, or numbers.

Read these files before you ask the first question:

1. `README.md`
2. `SECURITY.md`
3. `_templates/topic-template.md`
4. The `README.md` inside each area folder

Then tell the person, in a few sentences, what you are going to do: ask a little, write a little, and read it back.

### What "done" looks like for a first version

- You have said the secrets rule out loud, in plain words.
- Every real note uses the template, with `status: draft` or `status: confirmed`.
- Each area the person actually uses has at least one real topic, or a clear "nothing here yet" that they agreed to.
- You are not citing files whose names start with `example-`.
- A review rhythm is written down as its own topic once they choose one.
- The person has heard each draft read back and has had a chance to correct it.

Silence is not a yes. "That is close" means it stays `draft` until the words are fixed.

## Which areas to ask about first

Work in this order. Later areas depend on earlier ones. Ask one small batch, write the files, read them back, then continue. A batch is about three questions. Stop when the person is tired. A good first session is purpose, then business, then one operations topic.

1. **Purpose.** Who the notes are for, and what must stay out. Do this before any folder.
2. **`business/`.** What the work is. Operations and customers only make sense after this.
3. **`operations/`.** How a request moves. This is where repeated questions usually hide, so reach it early.
4. **`customers/`.** How messages should sound and what you will promise.
5. **`policies/`.** Decisions already made, including what needs a yes first.
6. **`finance/`.** Timing and approval rules, in words. Repeat the secrets rule before this area.
7. **`personal/`.** How the person likes assistants to work. Save preferences here so later chats stay consistent.

Skip `business/`, `customers/`, and `finance/` when the person says this is not for a business. Start with purpose, then `personal/`, then `policies/`.

You can add a folder later (for example `legal/`) if they keep needing it. Do not create empty areas "just in case" beyond the ones already in this starter.

### Questions to use

Use these, in small batches. Change the wording to match what they already told you. Skip a question they already answered.

**Purpose**

- Is this for a business, for personal life, or for both?
- Who should follow these notes besides you?
- What do you wish you did not have to explain twice?

**Business**

- What do you do, in one sentence a neighbor would understand?
- Who is it for?
- What do you not do, or never promise?

**Operations**

- How does a new request reach you?
- What happens between "yes" and "done"?
- Where do you get stuck, or repeat the same steps?

**Customers**

- How should a message from you sound?
- What should a new customer know on the first day?
- Which facts about a customer are okay to write down here?

**Policies**

- What have you already decided that an assistant should follow?
- What must wait for your yes (sending, spending, deleting, publishing)?
- What should happen when something goes wrong?

**Finance**

- When do invoices or bills go out, in words and without account numbers?
- Who is allowed to approve spending?
- Where should an assistant look for official numbers, without copying those numbers into the file?

**Personal**

- Do you want a short answer first, or the full detail up front?
- When are reminders welcome?
- What should an assistant ask before it acts?

### How to ask

- One topic at a time. About three questions, then write.
- Offer a generic pattern when they are stuck ("Some people write: a new request arrives by email, you confirm the scope, you do the work, you send a short recap"). Make clear it is a pattern, not their rule, until they adopt it.
- Repeat back what you heard, in their words, before you save it.
- Ask "is this confirmed, or still a draft?" after each file.
- Do not dump the full question list in one message.

## Turn answers into topic files

1. Copy `_templates/topic-template.md`.
2. Save it in the matching folder.
3. Name it with lowercase words and hyphens. The name should say what the file decides, such as `how-a-request-moves.md`. Do not use spaces. Do not start a real file with `example-`.
4. Fill in the front matter (the `---` block) and the sections: summary, details, sources, open questions, change log.
5. Keep the front matter `sources` list and the **Sources** section the same.
6. Set `status` to `draft`.
7. Read the file back to the person. Apply their corrections.
8. Set `status` to `confirmed` and set `last_reviewed` to today's date only after they accept the exact text. Use year-month-day, such as `2026-04-02`.
9. Put their first name or the word `owner` in `owner`. Do not add an email or a home address.

### Mark anything unconfirmed as draft

- A new file is a draft.
- A fact you found on the web is a draft until they agree to the summary and the link.
- A guess, a "probably," or an estimate stays a draft. Write the word **estimate** next to any number that is not exact.
- If they correct one sentence, the file stays a draft until they accept the new version.
- Open questions stay in the file until they answer them. Do not delete a question because you invented an answer.

When you cite a draft, say that it is not settled. Do not treat it as a rule.

Law, tax, and money notes stay drafts until the owner confirms them. You are not their lawyer or their accountant. Point at a source they supply. Do not present a draft as professional advice.

### Cite sources

Every claim that matters needs a source.

- Prefer a real link to the page the words came from (an official help page, a document they trust, a page they wrote).
- When the source is their own decision, write `Conversation with the owner on YYYY-MM-DD`.
- Do not invent a URL. Do not cite `https://example.com`. Those links in the template and the samples are placeholders.
- Do not cite a file whose name starts with `example-`, and do not cite `_templates/topic-template.md`.

### Keep topics small

- One decision, one workflow, or one rule per file.
- If the summary needs "and" between two rules, make two files and link them by path.
- If a person has to scroll through a long page, split it.
- Stay flat inside each area folder at the start. Add a subfolder only after a folder is crowded and the files clearly cluster.

### Sample files

The `example-*.md` files show the shape. Use them as a pattern, then write a new file with the person's words. Do not edit an example into a real rule in place. Do not cite examples.

## Never store secrets

Do not write any of these into a file, a commit, a pull request, or a change log, and do not ask for them:

- Passwords, API keys, tokens, recovery codes, private keys
- Social Security numbers, national ID numbers, tax ID numbers
- Bank account numbers, card numbers, routing numbers, payment account numbers
- Home street addresses and apartment numbers, including a customer's home address
- Copies or screenshots of IDs, tax forms, or bank pages

If the person starts to dictate or paste one of these, stop. Tell them to keep it in a password manager, with their bank, or with their accountant. Write only the safe part, such as "invoices go out on the first weekday of the month." Do not repeat the secret back to them.

Read `SECURITY.md` and follow it.

## How to cite a note when you answer

Use this shape:

```
Source: operations/how-a-request-moves.md (status: confirmed, last reviewed 2026-04-02)
[One or two sentences from that file.]
Underlying link: [the source URL, or the dated conversation]
```

Swap in the real file path and the real date. The path above only shows the shape.

When the status is `draft`, add: "This note is still a draft, so I am not treating it as settled."

When a confirmed note has no web link because the source is the owner's decision, say that, and include the conversation date from `sources`.

When the repository has no note on the question, say you do not have a confirmed note. Ask before you create one. Do not fill the gap with a guess.

## How to update an entry

Do not quietly rewrite a confirmed file.

**Preferred path: a pull request.** A pull request is a suggested edit the owner can accept or reject.

1. Change one topic.
2. Open a pull request. Use a short description:

```
## Topic update

- File:
- Change:
- Status after this change: draft
- Why:
```

3. Leave `status` as `draft` if the meaning changed, until the owner accepts both the words and the pull request.
4. When they accept, set `status` to `confirmed` and set `last_reviewed` to that day.
5. Add a change-log line either way: `YYYY-MM-DD — What changed, and why.`

Keep unrelated topics in separate pull requests.

**Other path: a change log, when they are not using pull requests.**

1. Add a dated line under **Change log**.
2. Set `status` to `draft`.
3. Ask them to read it.
4. After they agree, set `status` to `confirmed` and update `last_reviewed`.

New facts you discover stay drafts until the owner confirms them. Do not overwrite a confirmed summary to match a web page unless they ask you to.

If two notes disagree, the confirmed note wins. The newer draft is a suggestion, not a replacement, until they choose.

## Review cadence

- Default rhythm: every three months, list confirmed files whose `last_reviewed` date is older than three months, and ask the owner to reread them.
- Sooner when an offer, a tool, a price, or a policy changes: update that file in the same week.
- Drafts that are still open after two weeks: bring them up again, or ask whether to drop the question.
- When they pick a rhythm, write it as a real topic in `policies/` (for example `policies/review-rhythm.md`) and follow that file from then on.
- Update `last_reviewed` only after they agree the text is still right. A review with no agreement does not refresh the date.
- If a source link stops working, set the file back to `draft` until you have a replacement link they accept.

## When you are unsure

Ask. A short question is better than a made-up rule. If the person does not know either, write an open question and leave the status as `draft`.
