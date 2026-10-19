# 03 — Project Configuration Template

Copy to the **target app** as `.githubrules/PROJECT_CONFIG.md`. Inspect first; complete known settings. **Unknown is not unlimited.** Keep secrets out of the file.

```yaml
application:
  name: "TO_FILL"
  purpose: "TO_FILL"
  repository: "owner/repo"
  existing_instructions: ["CLAUDE.md", "AGENTS.md"]
  task_tracker: "TO_DETECT"
  architecture: "TO_DETECT"
governance:
  githubrules_source: "https://github.com/vvrapid/githubrules"
  githubrules_ref: "PIN_COMMIT_OR_VERSION"
  controller: "TO_ASSIGN"
  max_concurrent_workers: null    # must be approved/established; null != unlimited
  worker_spawn_supported: null
  read_permissions: "ESTABLISH"
  edit_permissions: "ESTABLISH"
  merge_permissions: "ESTABLISH"
  deploy_permissions: "ESTABLISH"
  production_data_permissions: "ESTABLISH"
  approval_required_for: ["extra_spend", "irreversible_prod_changes", "privacy_exceptions", "required_release"]
budgets:
  ai_models_approved: []
  ai_spend_limit: null
  github_actions_spend_limit: null
  external_api_spend_limit: null
  automatic_topups: false
testing:
  fast_local_command: "DETECT"
  unit_command: "DETECT"
  integration_command: "DETECT"
  browser_command: "DETECT"
  required_pr_checks: ["DETECT"]
  merge_queue_enabled: null
  release_gate: "DETECT"
  known_broken_tests: "EXISTING_TRACKER_OR_NONE"
deployment:
  environment: "DETECT"
  release_approvals: "DETECT"
  rollback: "DETECT"
```

**Instructions:** Values must be observed from application tooling/project instructions or established through user approval. Do not make up a worker cap, spend limit, mandatory command or approval. Reuse existing project configuration if equivalent. If YAML is unsuitable for the project, use equivalent Markdown.
