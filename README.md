# contract-opf / playbooks

Published, corpus-derived negotiation **playbooks** in the
[Open Playbook Format (OPF)](https://github.com/contract-opf/playbook-engine),
as pedagogical examples of the format.

## Educational Affiliation Agreement — Negotiation Playbook (OPF 0.3)

A real, corpus-derived playbook compiled by `playbook-engine` from 44 real
educational-affiliation agreements (161 negotiation versions) between Exos and
university counterparties.

**Privacy.** The source corpus is private and is NOT included. Every
counterparty identity is pseudonymized (`Counterparty-N`) or redacted —
institution names and variants, individuals, phone numbers, e-mail
addresses/domains, street/city/ZIP addresses, URLs, and e-signature audit
trails. Counterparties are referred to by the neutral role term "the
Institution." Dates are coarsened to quarters. Exos, the publishing party, is
named deliberately.

Leak-safety is **verified, not asserted**: the artifact passes the engine's two
fail-closed, list-independent publish gates — institution/address and
contact-identity (phones / e-mails / URLs) — plus a deterministic known-entity
backstop and independent adversarial scans of the JSON and rendered HTML. The
only proper nouns that remain by design are generic contract vocabulary,
statute names (HIPAA, FERPA), governing-law jurisdictions, and Exos itself.

| File | What it is |
|---|---|
| [`index.html`](https://contract-opf.github.io/playbooks/) | **Start here** — the single-file playbook: human-readable document + machine-readable payloads |
| `playbook.opf.json` | The canonical OPF 0.3 document (evidence, digest, corpus audit trail, content hash) |
| `playbook.digest.json` | The compact model-facing digest (~38K tokens): per-clause stances, preferred variations, deduplicated exemplar forms |

The HTML bundle embeds the canonical JSON verbatim in a
`<script id="opf-canonical" type="application/json">` block — extract it, parse
it, and verify `identity.content_hash`. `identity.supersedes` names the private
(internal) artifact this public profile was derived from.

Format spec and compiler: [`contract-opf/playbook-engine`](https://github.com/contract-opf/playbook-engine).
