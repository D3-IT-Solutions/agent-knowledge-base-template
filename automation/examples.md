# EXAMPLE automation ideas

> Illustrative only: these are EXAMPLES, not anyone's real tools or decisions; adapt them to your own work before using them.

Each example follows [automation-ideas-template.md](automation-ideas-template.md). Assistants must not cite these as the owner's decisions.

## EXAMPLE 1: Invoice reminder draft run

- **Repeated task:** Someone checks which invoices are past due, then writes a reminder message for each customer.
- **How often:** Whenever invoices go past due; in this example, checked weekly.
- **Proposed automation:** A routine that reads the list of unpaid invoices from your invoicing tool (read-only connector), picks the ones past due, and drafts one polite reminder per customer from a fixed template. Drafts are saved for review, never sent.
- **What stays human-approved:** A person reads each draft and sends the reminder. The routine never sends, changes an invoice, or charges anyone.
- **Done when:** On two separate runs, the drafted list matches the invoicing tool's past-due list exactly, each draft uses the right name and invoice reference, nothing was sent automatically, and the approver (not the builder) OKs both runs.

## EXAMPLE 2: Weekly site uptime and SSL/TLS certificate check

- **Repeated task:** Someone opens each website to confirm it loads and checks when its SSL/TLS certificate expires.
- **How often:** Weekly.
- **Proposed automation:** A scheduled script that requests each site on a list, records the response status, and reads the certificate expiry date, then writes a short report that flags any site that is down or whose certificate expires soon.
- **What stays human-approved:** The check is read-only. A person decides and makes any fix (renewing a certificate, changing hosting or DNS).
- **Done when:** On two separate runs, the report lists every site on the list, matches a manual spot check of at least one site, flags a test entry known to be down (for example a non-resolving test address) or an expired test certificate, and the approver (not the builder) OKs both runs.

## EXAMPLE 3: Lead list dedupe and format script

- **Repeated task:** Someone cleans an exported lead list by removing duplicates and fixing how names, emails and phone numbers are written before importing it.
- **How often:** Each time a new list is exported.
- **Proposed automation:** A script that reads the exported CSV, removes duplicates after normalizing (same email, or same phone number), formats fields the same way, and writes a clean CSV plus a log of every removed or changed row.
- **What stays human-approved:** A person reviews the log and decides whether to import the clean list or contact anyone on it. The script does not import or send anything.
- **Done when:** On two separate real lists, the output has no duplicates by the stated rules, every change appears in the log, a person's spot check finds no wrongly merged rows, and the approver (not the builder) OKs both runs.

## EXAMPLE 4: Monthly backup restore test

- **Repeated task:** Someone confirms backups can actually be restored, not just that they exist.
- **How often:** Monthly.
- **Proposed automation:** A routine that restores the latest backup into a separate test location (never over live data), runs a fixed set of checks (files present, a known record readable, the app or site starts), records the results, and leaves the restored test copy in place, flagged in its report as ready to remove. It never deletes anything itself.
- **What stays human-approved:** A person reviews the result, decides what to do about any failure, and deletes the test copy (deleting needs a person, see [when-script-vs-agent.md](when-script-vs-agent.md)). Any restore into the live system is done only by a person.
- **Done when:** On two separate monthly runs, the restore completes in the test location, all checks pass or failures are clearly reported, live data is untouched, the test copy is flagged for a person to remove, and the approver (not the builder) OKs both runs.
