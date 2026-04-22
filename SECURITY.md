# Security Policy

## Reporting a vulnerability

Email `security@zero.ski`. PGP welcome but not required. Please include:

- The repository (or deployment surface) affected
- A description of the issue and its impact
- Steps to reproduce, or a proof-of-concept
- Your disclosure timeline preferences, if any

We aim to acknowledge reports within **3 business days** and to provide a substantive response within **10 business days**.

## Coordinated disclosure

We follow a **90-day coordinated disclosure** window by default. The clock starts when we acknowledge the report.

- Within the window: we investigate, prepare a fix, and coordinate a release.
- At the end of the window: we publish a security advisory, even if a fix is not fully shipped, so downstream users can take protective action.
- Extensions are negotiated in good faith when a fix is in progress but needs more time.

If we believe a report is being actively exploited in the wild, we may disclose sooner in coordination with the reporter.

## In-scope repositories

The following open-source repositories are in scope for this policy:

- [tokencube/zeroski](https://github.com/tokencube/zeroski) — Rust kernel-verify + CLI
- [tokencube/zero-protocol](https://github.com/tokencube/zero-protocol) — Protocol spec + conformance
- [tokencube/.github](https://github.com/tokencube/.github) — this repo (org profile + defaults)

Additional repositories (`zero-sdk-ts`, `zeroski-rfcs`, and future open-source components) are covered by this policy once they go public; the authoritative list is the set of public repos under the [tokencube](https://github.com/tokencube) organization.

A repository that publishes its own `SECURITY.md` at the repo root overrides this org-wide default for that repository only.

## Out of scope

The following are **not** covered by this policy:

- The closed-source cloud service operated at `zero.ski`, `tokencube.ai`, and subdomains. That runtime (including private components such as `tokencube/zero` or `tokencube/zero-cloud`) has its own disclosure channel; contact `security@zero.ski` and we will route you.
- Denial-of-service findings that require unreasonably large inputs, pathological concurrency, or resource exhaustion at the host level. We treat these as capacity-planning issues, not protocol vulnerabilities, unless the report demonstrates amplification or asymmetric cost.
- Issues in third-party dependencies where the appropriate channel is the upstream project. We will of course accept reports on how we integrate a vulnerable dependency.
- Social-engineering, physical security, and findings against infrastructure we do not operate.

## Safe harbor

We will not pursue legal action against researchers who:

- Make a good-faith effort to comply with this policy
- Avoid privacy violations, destruction of data, and degradation of service
- Give us a reasonable opportunity to resolve the issue before public disclosure
- Do not exploit a finding beyond what is necessary to demonstrate it

## Acknowledgements

We are happy to credit reporters in the advisory. Let us know the name or handle you would like to use, or ask to remain anonymous.
