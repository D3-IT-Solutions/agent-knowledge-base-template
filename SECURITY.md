# Security

This starter is safe to publish because the sample pages are examples. Your real notes are different. Treat them as private.

## Keep the real notes in a private repository

When you create a repository from this template, choose **Private** before you add anything about yourself, your customers, or your work. A public repository can be copied by anyone.

If you already created a public copy, change it to private in GitHub (**Settings → General → Danger Zone → Change repository visibility**) before you add real notes.

## Leave these out of every file, commit, and chat paste

- Passwords, API keys, tokens, recovery codes, and private keys
- Social Security numbers, national ID numbers, and tax ID numbers
- Bank account numbers, card numbers, routing numbers, and payment-processor account numbers
- Home street addresses and apartment numbers, including a customer's home address
- Screenshots or PDFs of IDs, tax forms, bank pages, or invoices that show those numbers

When you are unsure whether an address belongs in a note, leave it out. A first name or a role in the `owner` field is enough. Skip email addresses in a public repository.

If a number is an estimate, label it as an estimate. If you do not have a number, leave it out. Do not invent one.

## Where those facts belong

Keep logins in a password manager. Keep tax IDs and account numbers with your bank, your accountant, or the official account page. A topic file may say where an official record lives ("the invoice screen of the payment tool") without copying the secret itself.

## If a secret is already in a file or a chat

1. Change the password or rotate the key anywhere it still works. Treat it as exposed.
2. Remove it from the note.
3. Ask someone you trust for help cleaning git history if it was committed. Do not paste the secret into a chat while you ask for that help.

## If you are an assistant

Do not ask the person to dictate a secret "so you can store it safely." If they paste one, do not write it into a file and do not repeat it back. Warn them, and store only the non-secret part of the note.
