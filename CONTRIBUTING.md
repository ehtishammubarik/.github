# Contributing

Thanks for taking the time. These are defaults across my repositories; a specific repo may override
them with its own guide.

## Before you open a pull request

Open an issue first for anything beyond a typo or an obvious bug fix. It is cheaper to agree on the
approach in a paragraph than to review the wrong implementation.

## Pull requests

- One logical change per PR. If the title needs the word "and", split it.
- Explain **why** in the description. The diff already shows what.
- Include the reproduction or the test that fails before your change and passes after.
- Note anything you did not do: known gaps, follow-ups, deliberate omissions.

## Commit messages

```
<type>(<scope>): <imperative summary, 72 chars or less>

Why this change exists. Constraints and trade-offs. Anything the next
reader would otherwise have to re-derive from the diff.

Refs: #123
```

Types: `feat`, `fix`, `refactor`, `perf`, `docs`, `test`, `build`, `ci`, `chore`, `revert`.

Avoid `wip`, `fix typo`, `update`, and `asdf`. Squash them before you push.

## Infrastructure repositories

Extra rules where a change can touch live systems:

- Terraform: run `terraform fmt` and `terraform validate`. Paste the relevant `plan` output in the
  PR. Never commit `.tfstate` or `.terraform/`.
- Kubernetes: manifests must set resource requests and limits, a readiness or liveness probe, and an
  explicit image tag. No `:latest`.
- Shell: `set -euo pipefail`, and `shellcheck` clean.
- Never commit credentials, `.env`, `*.pem`, private keys, or kubeconfigs. If you push one by
  accident, say so immediately and rotate it at the provider. Removing the commit is not enough.

## What I look for in review

Correctness first, then blast radius, then readability. A change that is clever but hard to reason
about at 3am during an incident is not an improvement.
