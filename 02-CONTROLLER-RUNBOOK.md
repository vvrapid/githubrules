# 02 — Controller Runbook

Read [01-UNIVERSAL-POLICY.md](01-UNIVERSAL-POLICY.md), then the application's real [project configuration](03-PROJECT-CONFIG-TEMPLATE.md).

## On first contact (lightweight)
1. Identify repo and development environment, current instructions, task tracker, branch status, stack and active workers. Read relevant files, not the whole repository.
2. Check repository policies, required CI checks and actual authority. Read available project configuration; fill only known values. Unspecified limits/permissions are **not permission to spend, deploy or access sensitive systems**.
3. Check CI workflows for obvious high-cost duplicate runs and broken suites; **do not begin a costly audit if it delays independent feature work**.
4. Identify highest-priority ready tasks; give concise ownership/acceptance criteria. Begin building, parallelising only genuinely independent work.

## Every task
1. State outcome and scope in a sentence; identify affected code and risk R0–R3.
2. Assign worker or implement directly. Protect files with clear ownership/worktrees where concurrent.
3. Reuse existing implementation; apply targeted change.
4. Run smallest relevant local checks, then any required revision-specific CI; for R2/R3 add affected integration/safety tests.
5. Integrate safely, reverify affected functionality after meaningful merges/rebases, update existing tracker only when status materially changes.
6. Continue next ready authorised task.

## If blocked
- Diagnose using logs/code; try a targeted fix. No blind retries. After repeated unsuccessful attempts, change approach or reassign.
- Keep unrelated workers active. Raise only blockers beyond current authority or with a genuinely necessary user decision.

## GitHub CI optimisation procedure
- Record current workflows, triggers, most expensive jobs and existing required status checks.
- Preserve stable required PR check, branch protections and deployment gates.
- Put costly tests behind **job-level** conditions or dedicated correctly governed workflows; do not accidentally leave a required skipped workflow pending.
- Add measured timeouts, safe PR cancellation, caching, narrower test selection and error quarantine with restoration ownership.
- Validate actual workflow YAML, stack setup, permission safety and required check behaviour; test changes on a branch/PR before merging when appropriate.
- Don't copy a universal sample `.github/workflows/ci.yml` unchanged into unknown stacks.
- Do not make private billing changes without appropriate approval/access.

## Worker handoff
**Task:** ID and intended result. **Changes:** files/behaviour. **Checks:** pass/fail/skipped and reason. **Blocker:** if any. **Next:** integration notes.

## Reporting
On user request or meaningful milestone: completed, ongoing workers, actual blockers, verification, material cost/risk concerns, next action. Keep brief.

## Adoption guardrails
- Never silently override stronger project-level safeguards, regulated requirements, production controls or user directions.
- Trusted platform instructions outrank this repository's documentation.
- Save source repository + immutable commit/tag used for adoption; do not auto-pull future changes into active apps.
- If central repository is inaccessible, **do not claim adoption**. Work within existing permissions and request the specific access needed when necessary.
