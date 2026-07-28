# .github

Default community health files for every repository owned by
[@ehtishammubarik](https://github.com/ehtishammubarik).

GitHub falls back to the files in this repository for any repo of mine that does not define its
own. That means a single edit here updates the contributing guide, security policy, support
instructions, and issue and pull request templates across all of them.

| File | Applies to |
| :--- | :--- |
| `CONTRIBUTING.md` | Any repo without its own contributing guide |
| `SECURITY.md` | Any repo without its own security policy |
| `CODE_OF_CONDUCT.md` | Any repo without its own code of conduct |
| `SUPPORT.md` | Any repo without its own support doc |
| `.github/ISSUE_TEMPLATE/` | Any repo without its own issue templates |
| `.github/PULL_REQUEST_TEMPLATE.md` | Any repo without its own PR template |

A repository's own file always wins. Lookup order is that repo's `.github/` folder, then its root,
then its `docs/` folder, then these defaults.

This repository must stay **public** for the fallback to work. It has no effect on my profile page,
which is driven separately by
[ehtishammubarik/ehtishammubarik](https://github.com/ehtishammubarik/ehtishammubarik).
