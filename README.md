# tokencube/.github

This repository provides **org-level GitHub community health files** for the [tokencube](https://github.com/tokencube) organization.

## What lives here

| Path | Purpose |
| --- | --- |
| `profile/README.md` | Rendered as the org landing page at https://github.com/tokencube. **Do not rename this file** — GitHub looks for exactly that path. |
| `profile/LICENSE` | License for the profile page prose (CC BY-SA 4.0). |
| `CODE_OF_CONDUCT.md` | Org-wide default. Used by any `tokencube/*` repo that does not define its own. |
| `SECURITY.md` | Org-wide default disclosure policy. Lists the in-scope OSS repos. |
| `CONTRIBUTING.md` | Org-wide default contribution guide. Repo-specific versions take precedence. |
| `PULL_REQUEST_TEMPLATE.md` | Default PR template. |
| `ISSUE_TEMPLATE/config.yml` | Default issue chooser config (Discussions + security link). |
| `LICENSE` | License for this repo's contents. |

## How GitHub picks up these defaults

GitHub automatically surfaces community health files from a repo named `.github` in the same organization when the target repo does not have its own. This lets us keep one source of truth for CoC / Security / Contributing across every public `tokencube/*` repository, while still allowing individual repos to override any file by shipping its own copy.

## Changing a file here

Changes to org-wide defaults affect every downstream `tokencube/*` repo that relies on the default. Prefer a PR + short discussion over a direct push to `main`.

## License

See [LICENSE](./LICENSE). Prose in `profile/` is CC BY-SA 4.0 (see `profile/LICENSE`).
