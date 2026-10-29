# contract-opf / playbooks

Published, corpus-derived negotiation **playbooks** in the
[Open Playbook Format (OPF)](https://github.com/contract-opf/opf), as
pedagogical examples of the format. Every playbook here is published under
**[PLAYBOOK-POLICY.md](PLAYBOOK-POLICY.md)**.

> **Not legal advice.** This playbook is a reference artifact describing one
> organization's negotiating positions for one type of agreement. It is not
> legal advice, and it is not a substitute for it.
>
> **No attorney-client relationship.** Publishing, reading, downloading,
> adapting, or executing this playbook creates no attorney-client relationship
> with its author, its originating organization, or any contributor.
>
> **No warranty.** It is provided as-is. No warranty is given that it is
> current, complete, accurate, or suitable for any particular transaction,
> counterparty, industry, or jurisdiction. Law changes; positions that were
> sound when recorded may not be sound now.
>
> **Attorney review is mandatory.** Any output produced by executing this
> playbook is a tool recommendation only and must be reviewed and approved by a
> qualified attorney before it is relied on or sent to a counterparty.
>
> **Modification changes legal effect.** Adapting a playbook — adding,
> removing, or altering positions, thresholds, or rules — can change the legal
> effect of the output it produces. An adaptation is the adapter's
> responsibility alone.
>
> **No endorsement of adaptations.** Neither the original author nor the
> originating organization endorses, reviews, or is responsible for any
> adapted, derived, or downstream version.

## Educational Affiliation Agreement — Negotiation Playbook (OPF 0.6)

A real, corpus-derived playbook compiled by
[`playbook-engine`](https://github.com/contract-opf/playbook-engine) from 44
negotiated educational-affiliation agreements (161 negotiation versions)
between Exos and university and college counterparties, then de-identified for
publication.

| Field | Value |
|---|---|
| **Author / originating organization** | Exos |
| **Intended agreement type** | Educational Affiliation Agreement for Student Internships (`agreement_type.id` `educational-affiliation`): a clinical or practicum placement agreement between a host facility and a university or college |
| **Intended user** | The **host facility** (the side that places students on site) reviewing a school's draft or defending its own form. The positions are directional: read from the school's side, they invert. |
| **Jurisdictional scope** | United States only, with no single governing law. The counterparties are public and private institutions in many states, and most deals that carry a governing-law clause (14 of 17) apply the institution's own state's law. Several public institutions also carry their state's immunities and public-records statutes. Not written for any non-US jurisdiction. |
| **Current as of** | May 2026, the latest signing date in the corpus (deals signed May 2023 to May 2026) |
| **Last reviewed** | 28 October 2026, by the General Counsel of the originating organization |
| **Version and change history** | See [Changes](#changes) below |
| **Source** | Derived from a corpus by `playbook-engine` 1.0.1 (OPF 0.6, `digest_version` 5), not authored by hand. The corpus is private and is not included. |
| **License** | [CC BY 4.0](LICENSE) (see PLAYBOOK-POLICY.md Part 3) |

**What it is, and is not.** This is an **evidence-only** playbook: the
Evidence section (what the 44 deals signed, opened with and refused, clause by
clause, every text cited) and its digest. It carries **no Posture and no Floor**:
no negotiating intent and no hard lines were authored for it. Those are
deliberately left empty, so a reviewer executing it gets the precedent record
with no instructions about what to do.

**De-identification.** The corpus is private. Every counterparty is
pseudonymized (`Counterparty-N`) or replaced by its role ("the Institution").
The following are replaced by labelled placeholders:
- institution and hospital names, and the names of colleges, schools,
  departments and programs (`[college]`, `[school]`, `[department]`, `[program]`)
- people's names (`[name]`)
- cities and street addresses (`[place]`, `[address redacted]`)
- e-mail addresses, URLs, phone numbers and file paths (`[redacted]`)
- contract numbers
- state-specific statutes and programs that would narrow a public counterparty (`[state law]`)
- two forms of our own affiliate entity names (`[Exos affiliate]`)

Deal ids are neutral (`deal-01` … `deal-44`), and signing dates are coarsened to
the month. Exos, the publishing party, and its other affiliates are named
deliberately. The only proper
nouns kept by design are contract vocabulary, federal statutes (HIPAA, FERPA,
Title IX, ADA) and state names: in governing-law, venue and sovereign-immunity
terms, and where an institution describes itself under its state's law. Dates
inside clause text are kept as signed.

| File | What it is |
|---|---|
| [`index.html`](https://contract-opf.github.io/playbooks/) | **Start here.** The single-file playbook page: the Playbook and Evidence views per clause, with the canonical JSON embedded |
| `playbook.opf.json` | The canonical OPF 0.6 document: evidence (the per-deal precedent record and verified absences), the digest, the manifest and dossiers, the corpus audit trail and the content hash |
| `LICENSE` | CC BY 4.0, with the full legal code |
| `playbook.digest.json` | A convenience copy of the document's `digest` section (`digest_version` 5, about 37K tokens): the compact model-facing projection. The canonical copy is inside `playbook.opf.json`. |

The page embeds the canonical JSON verbatim in a
`<script id="opf-canonical" type="application/json">` block. Extract it, parse
it, and verify `identity.content_hash`. `identity.supersedes` names the private
artifact this public profile was derived from.

## Changes

- **OPF 0.6** (this version). Recompiled from the current corpus by engine
  1.0.1 in the 0.6 format: a verdict-free precedent record per deal and
  clause, with no stance, band or risk verdicts. Each record shows what the
  deal opened with, what it signed and the asks refused before signing. Other
  additions:
  - each non-standard text compared to our standard part by part
  - our former forms, reconstructed from the corpus
  - verified absences
  - month-level signing dates

  Replaces the OPF 0.3 example. The 0.3 `summary.historical_stance` and
  `observed_positions` no longer exist, because the format retired them. Dates
  are now months, not quarters.
- **OPF 0.3** (July 2026). First published example.

Format spec: [`contract-opf/opf`](https://github.com/contract-opf/opf).
Compiler: [`contract-opf/playbook-engine`](https://github.com/contract-opf/playbook-engine).
