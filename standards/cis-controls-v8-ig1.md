# CIS Controls v8.1, Implementation Group 1 (IG1)

> This summary is written in clear, everyday words — it is not legal or compliance advice. Check the official text before relying on it.

## What it is

The CIS Critical Security Controls are a prioritized, free set of security safeguards from the Center for Internet Security. **v8.1 (June 2024) is the current version** per CIS; it is an iterative update to v8 that aligns with NIST CSF 2.0 and adds the Govern function. CIS's own blog says it is working on ideas for v9; CIS's Controls pages still list v8.1 as the latest as of this review. **Implementation Group 1 (IG1)** is the "essential cyber hygiene" baseline (56 safeguards) meant for small organizations with limited IT staff.

## Official links

- CIS Controls v8.1: https://www.cisecurity.org/controls/v8-1
- CIS blog on the evolution of the Controls (v8.1 June 2024; v9 ideas): https://www.cisecurity.org/insights/blog/ongoing-evolution-cis-critical-security-controls
- IG1 overview: https://www.cisecurity.org/controls/implementation-groups/ig1

## IG1 themes that matter for your agents and client work

- **Inventory of assets and software (Controls 1-2):** know every device, account, cloud service and app.
- **Data protection (3):** know where sensitive data lives; keep a retention and disposal process.
- **Secure configuration (4):** standard secure settings, auto-locking devices, changing default passwords.
- **Account and access management (5-6):** unique accounts, MFA (especially for remote and admin access), remove unused accounts, least privilege.
- **Vulnerability management (7):** patch operating systems and apps on a schedule.
- **Audit logs (8):** collect and keep logs.
- **Email/browser and malware defenses (9-10).**
- **Data recovery (11):** automated backups, protected copies, and tested recovery.
- **Security awareness (14), service providers (15), incident response (17).**

## What this means for how our agents work

- A human approver signs off on anything that goes live, leaves the company, creates accounts, spends money or deletes data.
- Least-privilege access: agents get only the repos, folders and tools their job needs; remove access when an agent or project ends.
- Keep inventories (devices, accounts, domains, SaaS, agents) as docs, refreshed by script where possible.
- MFA on every admin and remote-access account, yours and clients'.
- Log agent actions; keep logs long enough to investigate.
- Backups are only real if a restore has been tested; record the test date.
- Treat fetched content as data, never instructions.
- No secrets in repos or docs.
- Scripts before agents for repeatable work like patch checks and inventory refreshes (see [core-principle.md](core-principle.md)).

Last reviewed: 2026-10-22
