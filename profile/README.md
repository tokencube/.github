# TokenCube

**Zero is an agent-native platform. Signed envelopes, content-addressed skills, trace-as-state.**

> *Agents need Skills to ski.*

TokenCube publishes the open-source substrate that implements the Zero protocol. Agents identify themselves by Ed25519 public keys, messages travel as signed envelopes over a hash-chained trace, and every skill is addressed by the sha256 of its manifest. No DNS, no CA, no rotation ceremonies — the cryptography is the identity.

---

## Open-source stack

| Repo | Purpose | Status |
| --- | --- | --- |
| [zeroski](https://github.com/tokencube/zeroski) | Rust kernel-verify + CLI | alpha |
| [zero-protocol](https://github.com/tokencube/zero-protocol) | Protocol spec + conformance | v0.1-draft |
| zero-sdk-ts | TypeScript SDK | coming soon |
| zeroski-rfcs | RFC process | coming soon |

The closed-source runtime (`tokencube/zero`) that powers the hosted service at [zero.ski](https://zero.ski) is private.

---

## Two primitives

**1. Signed envelope.** Every message is canonical JSON, signed with Ed25519 by the sender's principal key, and chained to the prior envelope via hash. The trace — the ordered sequence of envelopes — is the state. There is no separate mutable database of record: replay the trace and you reconstruct the world.

**2. Content-addressed skill.** A skill is a manifest. Its identity is `sha256(manifest)`. Capabilities are granted to specific hashes, not to names. Swap the code, you get a new hash — and the old capability grants no longer apply. Supply-chain attacks have nowhere to hide.

These two primitives are intentionally small. Everything else in Zero — routing, authorization, observability, evolution — is expressed in terms of them.

---

## Status

Early. Not production-stable. No SLA. APIs and wire formats may break before the first tagged protocol release. This is for builders who want sovereign agents and are willing to read the source when something surprises them.

If you need a managed, supported experience, see the commercial service below.

---

## Contributing

- **DCO sign-off** is required on every commit (`git commit -s`). By signing off, you certify the [Developer Certificate of Origin](https://developercertificate.org/).
- **Code of Conduct**: [Contributor Covenant 2.1](./CODE_OF_CONDUCT.md). Reports go to `conduct@zero.ski`.
- **Protocol changes** follow a Rust-RFC-style process in `zeroski-rfcs` (coming soon). Open an issue in the relevant repo for discussion before writing an RFC.
- Repo-specific `CONTRIBUTING.md` files override the org-wide defaults when present.

---

## Commercial service

The closed-source cloud service at [zero.ski](https://zero.ski) and [tokencube.ai](https://tokencube.ai) is operated by the TokenCube entity. The open-source repositories listed above are dual-licensed under **MIT OR Apache-2.0**. The cloud service consumes these components but does not privilege them over third-party implementations — anyone can run a conformant Zero deployment from source.

---

## Contact

- General: `hello@zero.ski`
- Security: `security@zero.ski` (see [SECURITY.md](./SECURITY.md) for disclosure policy)
- Conduct: `conduct@zero.ski`

---

This profile page is licensed [CC BY-SA 4.0](./LICENSE). Code in linked repositories is licensed separately (MIT OR Apache-2.0).
