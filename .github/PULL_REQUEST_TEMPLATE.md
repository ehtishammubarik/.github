## What this changes

<!-- One or two sentences. The diff shows what; explain why it exists. -->

## Related issue

<!-- Closes #123, or "none, this is a typo fix". Open an issue first for anything larger. -->

## How it was verified

<!-- Commands run, tests added, manual steps. "It builds" is not verification. -->

```
paste real output here
```

## Blast radius

<!-- What breaks if this is wrong? Who notices? How do we roll it back? -->

## Checklist

- [ ] One logical change. The title does not need the word "and".
- [ ] Explains why, not just what.
- [ ] No credentials, `.env`, `*.pem`, private keys, kubeconfigs, or `*.tfstate` in the diff.
- [ ] No build artifacts (`node_modules/`, `.terraform/`, `dist/`, `__pycache__/`).
- [ ] Docs or README updated if behaviour changed.

### Infrastructure changes only

- [ ] `terraform fmt` and `terraform validate` are clean; `plan` output pasted above.
- [ ] Kubernetes manifests set resource requests and limits, a probe, and an explicit image tag.
- [ ] Shell scripts use `set -euo pipefail` and pass `shellcheck`.

## Anything left undone

<!-- Known gaps, deliberate omissions, follow-ups. Say so here rather than leaving it to be found. -->
