# 04 — Adoption Sequence and CI Safeguards

## Applying githubrules to any existing app
1. **Gain access** to this private repo and target app. Resolve genuine access issues; never falsely report reading inaccessible files.
2. **Pin** the current githubrules commit or release tag. Read files 01–04, then 05 for the reusable invitation prompt.
3. **Inspect** existing AGENTS.md/CLAUDE.md, controller, tasks, CI, deployment instructions and branch protections. Do not overwrite or duplicate them.
4. **Compare** existing requirements with the universal policy; higher-priority or stricter legitimate constraints survive. Record material conflicts.
5. **Add a small reference** to project agent/controller instructions: `Follow .githubrules/PROJECT_CONFIG.md and githubrules policy at pinned ref; prefer speed-first risk-based implementation, subject to existing higher-priority instructions.`
6. **Adapt** the configuration template to the *real* stack/limits. Put source pin and any exceptions into `.githubrules/ADOPTION.md`; do not store secrets.
7. **Make only justified CI changes**. Keep required checks functional; test GitHub Actions syntax and relevant trigger/permission paths. CI changes should not needlessly delay independent feature work.
8. **Proceed with development**. Do not make policy installation a sprawling project.
9. **Report** files changed, policy ref, preserved safeguards, checks performed, remaining unknowns and next app task.

## New app
Inspect the planned stack, set initial project values, implement a **small relevant required check**, separate expensive R2/R3/release verification, then begin feature work. Do not invent an elaborate CI pipeline before code exists.

## CI acceptance checklist
- [ ] Existing branch/ruleset required checks identified and preserved.
- [ ] PR check reliably completes (including doc-only PRs); avoid workflow-level path filters that strand required check as pending.
- [ ] If merge queue enabled, check relevant `merge_group` triggers.
- [ ] Cheap validation before expensive work.
- [ ] Actual dependency/runtime setup for this stack; no fictitious script path.
- [ ] Job timeouts reflect measurements, not arbitrary target completion.
- [ ] Obsolete PR runs cancelled when safe; releases/deploys protected.
- [ ] High-risk code still gets applicable security and integration verification.
- [ ] Untrusted PR code cannot access privileged secrets/tokens.
- [ ] Versioned trusted actions/dependencies appropriately.
- [ ] Known failing suites separated only with issue/owner/alternative coverage/recovery plan.
- [ ] No auto top-ups; GitHub account-level enforced budget settings verified separately if hard stop needed.
- [ ] Test actual YAML/config with project tooling and appropriate PR.

## Not a universal workflow
No generic `ci.yml` is installed by this repo. A copied workflow could break a Python, iOS, Node, Rust, mobile or database project. The target controller **must generate stack-specific CI** and verify the actual script commands and permissions.

## Updating existing adoption
Pin newer githubrules source, diff the changed rules, reconcile with current project policy and constraints, test policy/CI adjustments, then update the pin. Never silently rewrite active application configurations.
