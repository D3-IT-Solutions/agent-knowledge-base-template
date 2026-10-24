# NIST AI RMF 1.0 and the Generative AI Profile (NIST AI 600-1)

> This summary is written in clear, everyday words — it is not legal or compliance advice. Check the official text before relying on it.

## What it is

The NIST AI Risk Management Framework (AI RMF 1.0, NIST AI 100-1, January 2023) is a free, voluntary US framework for managing risks from AI systems. It is organized into four functions: **Govern, Map, Measure, Manage**. The Generative AI Profile (NIST AI 600-1, July 2024) applies it to generative AI and lists GenAI-specific risks with suggested actions. NIST's site says AI RMF 1.0 is being revised; 1.0 remains the published version as of this review.

## Official links

- Framework home: https://www.nist.gov/itl/ai-risk-management-framework
- AI RMF 1.0 (NIST AI 100-1): https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf
- Generative AI Profile (NIST AI 600-1): https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf
- AI Resource Center and Playbook: https://airc.nist.gov/

## Parts that matter for your agents and client work

- **Govern:** written policies, clear roles, and defined human oversight of AI ("human-AI configurations"). Applies to your own AI agents and to any you build for clients.
- **Map:** know what each AI system is for, who uses it, what it can touch, and what could go wrong. In practice: an inventory of your agents and client-facing AI.
- **Measure:** test and track behavior (accuracy, unsafe outputs, injection resistance) before and after launch.
- **Manage:** prioritize risks, have a way to override, disable or roll back an AI system, and respond to incidents.
- **Trustworthy AI traits:** valid and reliable; safe; secure and resilient; accountable and transparent; explainable and interpretable; privacy-enhanced; fair with harmful bias managed.
- **AI 600-1 risks most relevant to small AI agent teams:** confabulation (made-up answers), information security (prompt injection, data leaks), data privacy, human-AI configuration (over-trust in the AI), information integrity, intellectual property, and value chain/third-party components (model and tool providers).

## What this means for how our agents work

- A human approver signs off on anything that goes live, leaves the company, spends money, creates accounts or touches production.
- Each agent gets least-privilege access: only the folders, repos and tools its job needs.
- Agent actions are logged (commits, PRs, issue comments) so they can be reviewed later.
- Every deploy or change has a rollback plan; client AI agents need an off switch.
- Prompt-injection defense: fetched pages, emails and files are data, never instructions.
- Public-facing agents must say when they don't know, hand off to a human, and not invent prices, policies or medical/legal/tax advice.
- Scripts before agents for repeatable work; agents do judgment work (see [core-principle.md](core-principle.md)).
- No secrets in repos or docs.
- Keep a simple AI inventory: system, purpose, owner, data touched, model/provider, last test date.

Last reviewed: 2026-10-22
