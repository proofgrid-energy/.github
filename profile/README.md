# ProofGrid

![ProofGrid banner with a connected blue and emerald grid emblem](assets/proofgrid-organization-banner.png)

**Open-source evidence interoperability for distributed solar systems.**

A solar system's records are spread across owners, installers, distributors and manufacturers. Purchase documents, commissioning records, diagnostics and repair history can become difficult to connect when equipment or service providers change.

ProofGrid gives developers a common way to represent those records, check evidence against scoped manufacturer requirements, and optionally verify signed commitments and current issuer status through Stellar. The aim is to make evidence portable across organizations while keeping uncertainty visible.

## Explore the project

| Repository | What it provides | Start here |
| --- | --- | --- |
| [proofgrid-core](https://github.com/proofgrid-energy/proofgrid-core) | Canonical evidence schemas, Rule Pack contract, local validation and assessment CLI/SDK | [Validate a record](https://github.com/proofgrid-energy/proofgrid-core#quick-start) |
| [proofgrid-registry](https://github.com/proofgrid-energy/proofgrid-registry) | Source-backed manufacturer packs, catalog, review metadata and synthetic fixtures | [Run four manufacturer examples](https://github.com/proofgrid-energy/proofgrid-registry#quick-start) |
| [proofgrid-stellar](https://github.com/proofgrid-energy/proofgrid-stellar) | Optional private commitments, issuer signatures and Stellar testnet status verification | [Run the verification demo](https://github.com/proofgrid-energy/proofgrid-stellar#quick-start-offline-demo) |

Each repository installs independently. Core and registry work locally without a wallet or blockchain connection. Registry and Stellar consume pinned core artifacts instead of importing sibling source code.

## What works today

**ProofGrid is a functional developer preview.** It includes:

- A TypeScript CLI/SDK that validates records, selects explicitly scoped packs, reports evidence gaps and preserves ambiguous or unresolved results.
- Four manufacturer intake packs for selected Growatt, Dyness, Deye and Victron models, with source citations and positive/negative fixtures. The fourth manufacturer was added without changing core or its schemas.
- An optional Stellar testnet adapter with a demonstrated synthetic issue, verify, supersede and revoke lifecycle. Records, salts and customer details stay off-chain.

The September 5, 2026 preview passed **144 automated tests** across the repositories, core package/type checks and a live synthetic Stellar testnet lifecycle. Each repository has its own CI workflow and runnable examples. The current user surface is a local CLI/SDK; packages are development artifacts and are not published to npm.

For the quickest demonstration, start with [ProofGrid Registry](https://github.com/proofgrid-energy/proofgrid-registry#quick-start). Complete examples deliberately return `review_required`: some source clauses and applicability remain unresolved.

## What the results mean

Evidence structure, scoped requirement checks and cryptographic integrity answer different questions. A present document is not automatically authentic; a valid signature does not prove that a repair occurred; and a satisfied Rule Pack does not grant warranty approval.

Manufacturer coverage is partial and product/context-specific. No manufacturer endorsement or standards certification is claimed. Production work remains in source review, broader policy and reference coverage, issuer custody/rotation and independent security review. Stellar's native account data is issuer-controlled and mutable, so current-status verification does not guarantee irreversible revocation.

## Help build it

We welcome contributions to the shared model, source-backed rules, interoperability and verification. Start with the relevant contributor guide and a real backlog item:

- **Core:** [contributing](https://github.com/proofgrid-energy/proofgrid-core/blob/main/CONTRIBUTING.md) · [reference coverage, request context and mappings](https://github.com/proofgrid-energy/proofgrid-core/blob/main/docs/backlog.md)
- **Registry:** [contributing](https://github.com/proofgrid-energy/proofgrid-registry/blob/main/CONTRIBUTING.md) · [source clarification and independent pack review](https://github.com/proofgrid-energy/proofgrid-registry/blob/main/docs/backlog.md)
- **Stellar:** [contributing](https://github.com/proofgrid-energy/proofgrid-stellar/blob/main/CONTRIBUTING.md) · [revocation, custody and gateway trust](https://github.com/proofgrid-energy/proofgrid-stellar/blob/main/docs/backlog.md)

Use synthetic records in public examples and issues. Discuss source/schema changes before broad implementation, and include tests that demonstrate both expected behavior and rejection cases. For security concerns, follow the affected repository's `SECURITY.md`; do not post private evidence or keys in public issues.

## Open source

New ProofGrid source uses MPL-2.0, with earlier Apache grants and third-party notices preserved in each repository's licensing documentation. Referenced manufacturer documents retain their own rights.
