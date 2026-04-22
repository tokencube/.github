# Contributing to TokenCube projects

These are the org-wide defaults. A repository that ships its own `CONTRIBUTING.md` overrides this file for that repository only — always check the target repo first.

## Before you start

- **Open an issue first for non-trivial changes.** Bug fixes with a narrow, obvious scope can go straight to a pull request. Anything that adds a feature, changes behavior, touches the protocol, or rewrites more than a few files should start as an issue so we can discuss direction before you invest time.
- **Protocol changes go through RFCs.** If your change affects the envelope format, skill manifest, capability model, or any other wire-visible surface, the discussion happens in the `zeroski-rfcs` repository (coming soon). Until it's public, open a tracking issue in [zero-protocol](https://github.com/tokencube/zero-protocol) instead.
- **Search existing issues and discussions.** Someone may already be working on it, or we may have decided against it for a reason worth knowing.

## Developer Certificate of Origin

Every commit must be signed off under the [Developer Certificate of Origin](https://developercertificate.org/). Configure your local Git once:

```bash
git config --global user.name  "Your Name"
git config --global user.email "you@example.com"
```

Then sign off each commit:

```bash
git commit -s -m "fix(envelope): handle empty chain tail"
```

This appends a `Signed-off-by: Your Name <you@example.com>` trailer, which is your assertion that you have the right to submit the contribution under the repository's license. Pull requests with un-signed-off commits will be asked to rebase.

## Pull requests

- Keep PRs focused. One logical change per PR; split large work into a series.
- Update tests. If you add a code path, add a test that exercises it. If you fix a bug, add a test that would have caught it.
- Update docs. Protocol and public-API changes need a docs update in the same PR.
- Follow the repo's commit style. Most TokenCube repos use [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`, `perf:`, `ci:`).
- CI must be green before review.

## Code of Conduct

All contributors are expected to follow the [Code of Conduct](./CODE_OF_CONDUCT.md). Violations can be reported to `conduct@zero.ski`.

## Security issues

Do **not** file security issues as public GitHub issues. See [SECURITY.md](./SECURITY.md) and email `security@zero.ski`.

## Licensing

Unless a repository specifies otherwise, contributions are dual-licensed under **MIT OR Apache-2.0**. By opening a pull request you confirm that you are licensing your contribution under these terms.

## Questions

- General: open a Discussion in the target repo, or email `hello@zero.ski`.
- Security: `security@zero.ski`.
- Conduct: `conduct@zero.ski`.
