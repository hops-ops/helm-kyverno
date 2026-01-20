### What's changed in v0.1.0

* feat: initial commit (by @patrickleet)

* chore(deps): update unbounded-tech/workflow-simple-release action to v2.1.1 (#2) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat(deps): update helm release kyverno to v3.6.2 (#1) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* chore(deps): update unbounded-tech/workflows-crossplane action to v2.13.0 (#4) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat: helm chart xrd (by @patrickleet)

* chore(deps): update unbounded-tech/workflow-vnext-tag action to v1.21.0 (#6) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat(deps): update crossplane-contrib/provider-helm docker tag to v1.0.6 (#5) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* fix: add ClusterRoleBinding to e2e test for namespace creation (by @patrickleet)

  The Helm provider service account needs cluster-admin permissions
  to create namespaces when installing charts.

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>

* fix: add missing configuration.yaml for provider dependencies (by @patrickleet)

  The configuration.yaml file is required to declare provider dependencies
  for schema validation during the CI build process.

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>


