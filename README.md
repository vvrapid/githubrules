# githubrules — Universal AI Development System

**Version:** 3.1 · **Maintained:** 19 October 2026 · **Status:** canonical policy

This private repository contains the reusable **speed-first, risk-based** operating standard for AI-assisted application development (Claude Code, Z.ai, Codex, and other developer agents). It is an **instruction library**, not an application or a CI workflow to install unchanged into every project.

## Start here — in this order

| Step | File | Purpose |
|---|---|---|
| 1 | [01-UNIVERSAL-POLICY.md](01-UNIVERSAL-POLICY.md) | Non-negotiable universal principles, testing, quality and cost controls |
| 2 | [02-CONTROLLER-RUNBOOK.md](02-CONTROLLER-RUNBOOK.md) | Exact controller/worker workflow and anti-bottleneck rules |
| 3 | [03-PROJECT-CONFIG-TEMPLATE.md](03-PROJECT-CONFIG-TEMPLATE.md) | Small configuration to adapt the policy to each actual app |
| 4 | [04-ADOPTION-AND-CI.md](04-ADOPTION-AND-CI.md) | Safe, ordered installation into new/existing repositories, including CI |
| 5 | [05-ONE-MESSAGE-PROMPT.md](05-ONE-MESSAGE-PROMPT.md) | **The single message to give any AI developer** |

## Simplest usage

1. Give the AI developer the message in **[05-ONE-MESSAGE-PROMPT.md](05-ONE-MESSAGE-PROMPT.md)**.
2. Give it access to **this private repository** and the application repository. It must not pretend it read this material if access is unavailable.
3. The agent inspects the application, records its actual project-specific limits, installs **compact local controller instructions**, and applies risk-appropriate CI improvements without destroying existing configurations.
4. The agent **continues building the app**. Adopting this policy must not become a standalone, lengthy project.

**No automatic deployment. No automatic top-ups. No secret sharing. No blanket full-suite CI on every change.** Existing project rules and required safety gates remain in force until deliberately and safely updated.

## How the system fits together

```text
githubrules (central, versioned reference)
    |
    +-- 01 policy: what every app must respect
    +-- 02 runbook: how controllers and workers operate
    +-- 03 template: what varies by app
    +-- 04 adoption: how to apply without breaking projects
    +-- 05 prompt: one instruction for any developer
    |
    v
Application repository
    +-- existing CLAUDE.md / AGENTS.md / controller instruction (brief reference)
    +-- .githubrules/PROJECT_CONFIG.md (real project-specific settings)
    +-- .githubrules/ADOPTION.md (source version/commit and deviations)
    +-- existing code, tests and workflows (preserved and selectively improved)
```

## Update policy

- This repository is the **canonical source**. Do not fork the universal rules into multiple competing documents.
- Each application records which version/commit it adopted. Updates to this repository do **not** silently change application permissions, CI or deployment gates.
- A future controller may compare versions and adopt a newer release after checking conflicts and project requirements.
- Prefer **small improvements to existing files** over adding administrative machinery.
- If central documentation and higher-priority platform/security restrictions conflict, the stricter legitimate safeguards prevail.

## Practical goal

**Fastest delivery of verified working software within security, data, release and spending limits.** The controller manages; workers build; testing is proportional to risk; GitHub checks only do useful work.
