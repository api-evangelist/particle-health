# Particle Health

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Particle Health is a healthcare data interoperability platform that aggregates patient medical records from across the US healthcare system into a single RESTful API. Particle is connected to all three nationwide health information exchange networks (Carequality, CommonWell, eHealth Exchange), TEFCA / QHIN partners, state HIEs (Healthix in New York, Manifest MedEx in California), and Surescripts for pharmacy data. The platform exposes patient demographics, clinical resources, and document retrieval via FHIR R4, C-CDA, Flat, and Deltas formats, layered with deduplication, normalization, AI summarization (Particle Snapshot), real-time encounter and transition alerts (Particle Signal), and longitudinal patient journey tracking (Particle Navigator). Customer segments include value-based care organizations, payers, health systems, primary and specialty providers, and digital health developers.

**Areas:** ADT · C-CDA · Care Coordination · Carequality · Clinical Data · CommonWell · Deltas · eHealth Exchange · Electronic Health Records · FHIR · Health Data · Health Information Exchange

## Particle Health on APIs.io

Everything profiled for Particle Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/particle-health/](https://apis.io/providers/particle-health/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [Particle Health Authentication API](https://apis.io/apis/particle-health/particle-health-authentication-api/) — OAuth 2 client-credentials JWT issuance.
- [Particle Health Batches API](https://apis.io/apis/particle-health/particle-health-batches-api/) — Batch query orchestration over patient cohorts.
- [Particle Health CCDA API](https://apis.io/apis/particle-health/particle-health-ccda-api/) — C-CDA clinical document retrieval.
- [Particle Health Deltas API](https://apis.io/apis/particle-health/particle-health-deltas-api/) — Incremental change retrieval since a previous query.
- [Particle Health Documents API](https://apis.io/apis/particle-health/particle-health-documents-api/) — Document upload, retrieval, and deletion.
- [Particle Health FHIR API](https://apis.io/apis/particle-health/particle-health-fhir-api/) — FHIR R4 resource search and read.
- [Particle Health Files API](https://apis.io/apis/particle-health/particle-health-files-api/) — Query result file download.
- [Particle Health Flat API](https://apis.io/apis/particle-health/particle-health-flat-api/) — Flat (normalized columnar) clinical data domains.
- [Particle Health HL7v2 API](https://apis.io/apis/particle-health/particle-health-hl7v2-api/) — HL7v2 ADT messages.
- [Particle Health NetworkParticipants API](https://apis.io/apis/particle-health/particle-health-networkparticipants-api/) — Directory search over connected network organizations.
- [Particle Health Notifications API](https://apis.io/apis/particle-health/particle-health-notifications-api/) — Project-level webhook notification configuration.
- [Particle Health Patients API](https://apis.io/apis/particle-health/particle-health-patients-api/) — Patient demographic registration and lookup.
- [Particle Health Projects API](https://apis.io/apis/particle-health/particle-health-projects-api/) — Project and service-account management.
- [Particle Health ProviderMap API](https://apis.io/apis/particle-health/particle-health-providermap-api/) — Patient provider mapping across the network.
- [Particle Health Queries API](https://apis.io/apis/particle-health/particle-health-queries-api/) — One-time network query orchestration.
- [Particle Health Signal API](https://apis.io/apis/particle-health/particle-health-signal-api/) — Real-time encounter, transition, and ADT alerts.
- [Particle Health Subscriptions API](https://apis.io/apis/particle-health/particle-health-subscriptions-api/) — Patient subscription management for Signal.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (5)

Multi-step workflows that chain operations into a business task.

- [Particle Health ADT Event Subscription](https://apis.io/arazzos/particle-health/particle-health-adt-subscription-workflow/)
- [Particle Health Clinical Document Exchange](https://apis.io/arazzos/particle-health/particle-health-clinical-document-exchange-workflow/)
- [Particle Health FHIR R4 Resource Query](https://apis.io/arazzos/particle-health/particle-health-fhir-r4-resource-query-workflow/)
- [Particle Health Network Provider Discovery](https://apis.io/arazzos/particle-health/particle-health-network-provider-discovery-workflow/)
- [Particle Health National Patient Record Retrieval](https://apis.io/arazzos/particle-health/particle-health-patient-record-retrieval-workflow/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Particle Health Webhooks](https://apis.io/asyncapis/particle-health/particle-health-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [particle-health-mcp.yml](https://apis.io/servers/particle-health/particle-health-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Particle Health Agentic Access](https://apis.io/agentic-access/particle-health/particle-health-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Particle Health Patient](https://apis.io/schemas/particle-health/particle-health-patient/)
- [Particle Health Query](https://apis.io/schemas/particle-health/particle-health-query/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Particle Health Context](https://apis.io/jsonld/particle-health/particle-health-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Particle Health Vocabulary](https://apis.io/vocabularies/particle-health/particle-health-vocabulary/)

#### Collections (35)

Postman and Open Collection request collections.

- [Particle Health API](https://apis.io/collections/particle-health/open-particle-health/)
- [Particle Health Authentication API](https://apis.io/collections/particle-health/open-particle-health-authentication-api/)
- [Particle Health Authentication Batches API](https://apis.io/collections/particle-health/open-particle-health-batches-api/)
- [Particle Health Authentication CCDA API](https://apis.io/collections/particle-health/open-particle-health-ccda-api/)
- [Particle Health Authentication Deltas API](https://apis.io/collections/particle-health/open-particle-health-deltas-api/)
- [Particle Health Authentication Documents API](https://apis.io/collections/particle-health/open-particle-health-documents-api/)
- [Particle Health Authentication FHIR API](https://apis.io/collections/particle-health/open-particle-health-fhir-api/)
- [Particle Health Authentication Files API](https://apis.io/collections/particle-health/open-particle-health-files-api/)
- [Particle Health Authentication Flat API](https://apis.io/collections/particle-health/open-particle-health-flat-api/)
- [Particle Health Authentication HL7v2 API](https://apis.io/collections/particle-health/open-particle-health-hl7v2-api/)
- [Particle Health Authentication NetworkParticipants API](https://apis.io/collections/particle-health/open-particle-health-networkparticipants-api/)
- [Particle Health Authentication Notifications API](https://apis.io/collections/particle-health/open-particle-health-notifications-api/)
- [Particle Health Authentication Patients API](https://apis.io/collections/particle-health/open-particle-health-patients-api/)
- [Particle Health Authentication Projects API](https://apis.io/collections/particle-health/open-particle-health-projects-api/)
- [Particle Health Authentication ProviderMap API](https://apis.io/collections/particle-health/open-particle-health-providermap-api/)
- [Particle Health Authentication Queries API](https://apis.io/collections/particle-health/open-particle-health-queries-api/)
- [Particle Health Authentication Signal API](https://apis.io/collections/particle-health/open-particle-health-signal-api/)
- [Particle Health Authentication Subscriptions API](https://apis.io/collections/particle-health/open-particle-health-subscriptions-api/)
- [Particle Health Authentication API](https://apis.io/collections/particle-health/postman-particle-health-authentication-api/)
- [Particle Health Authentication Batches API](https://apis.io/collections/particle-health/postman-particle-health-batches-api/)
- [Particle Health Authentication CCDA API](https://apis.io/collections/particle-health/postman-particle-health-ccda-api/)
- [Particle Health Authentication Deltas API](https://apis.io/collections/particle-health/postman-particle-health-deltas-api/)
- [Particle Health Authentication Documents API](https://apis.io/collections/particle-health/postman-particle-health-documents-api/)
- [Particle Health Authentication FHIR API](https://apis.io/collections/particle-health/postman-particle-health-fhir-api/)
- [Particle Health Authentication Files API](https://apis.io/collections/particle-health/postman-particle-health-files-api/)
- …and 10 more published on APIs.io

#### Overlays (17)

OpenAPI overlays, including conversational phrasing for each operation.

- [Particle Health Authentication Api Overlay](https://apis.io/overlays/particle-health/particle-health-authentication-api-overlay/)
- [Particle Health Batches Api Overlay](https://apis.io/overlays/particle-health/particle-health-batches-api-overlay/)
- [Particle Health Ccda Api Overlay](https://apis.io/overlays/particle-health/particle-health-ccda-api-overlay/)
- [Particle Health Deltas Api Overlay](https://apis.io/overlays/particle-health/particle-health-deltas-api-overlay/)
- [Particle Health Documents Api Overlay](https://apis.io/overlays/particle-health/particle-health-documents-api-overlay/)
- [Particle Health Fhir Api Overlay](https://apis.io/overlays/particle-health/particle-health-fhir-api-overlay/)
- [Particle Health Files Api Overlay](https://apis.io/overlays/particle-health/particle-health-files-api-overlay/)
- [Particle Health Flat Api Overlay](https://apis.io/overlays/particle-health/particle-health-flat-api-overlay/)
- [Particle Health Hl7V2 Api Overlay](https://apis.io/overlays/particle-health/particle-health-hl7v2-api-overlay/)
- [Particle Health Networkparticipants Api Overlay](https://apis.io/overlays/particle-health/particle-health-networkparticipants-api-overlay/)
- [Particle Health Notifications Api Overlay](https://apis.io/overlays/particle-health/particle-health-notifications-api-overlay/)
- [Particle Health Patients Api Overlay](https://apis.io/overlays/particle-health/particle-health-patients-api-overlay/)
- [Particle Health Projects Api Overlay](https://apis.io/overlays/particle-health/particle-health-projects-api-overlay/)
- [Particle Health Providermap Api Overlay](https://apis.io/overlays/particle-health/particle-health-providermap-api-overlay/)
- [Particle Health Queries Api Overlay](https://apis.io/overlays/particle-health/particle-health-queries-api-overlay/)
- [Particle Health Signal Api Overlay](https://apis.io/overlays/particle-health/particle-health-signal-api-overlay/)
- [Particle Health Subscriptions Api Overlay](https://apis.io/overlays/particle-health/particle-health-subscriptions-api-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Particle Health — jsonschema rules](https://apis.io/rules/particle-health/particle-health-jsonschema-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Particle Health Authentication](https://apis.io/security/particle-health/particle-health-authentication/)
- [Particle Health Domain Security](https://apis.io/security/particle-health/particle-health-domain-security/)
- [Particle Health Trust Center](https://apis.io/security/particle-health/particle-health-trust-center/)
- [Particle Health Vulnerability Disclosure](https://apis.io/security/particle-health/particle-health-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Particle Health Plans Pricing](https://apis.io/plans/particle-health/particle-health-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Particle Health Rate Limits](https://apis.io/rate-limits/particle-health/particle-health-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Particle Health Finops](https://apis.io/finops/particle-health/particle-health-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://particlehealth.com/)
- [Documentation](https://docs.particlehealth.com/)
- [API reference](https://docs.particlehealth.com/reference/getting-started)
- [Changelog](https://docs.particlehealth.com/docs/)
- [Blog](https://particlehealth.com/blog)
- [Terms of service](https://particlehealth.com/terms-of-use)
- [Privacy policy](https://particlehealth.com/privacy-policy)
- [GitHub](https://github.com/ParticleHealth)
- [Status](https://status.particlehealth.com/)

## API Evangelist rating

**Kin Score 58.5** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 76.7 |
| Contract quality | 58.9 |
| Contract governance | 23.5 |
| Operational transparency | 80.3 |
| Developer ergonomics | 56.4 |
| Access clarity | 44.7 |

**Agent readiness 37.0** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | mostly |

**Regulatory alignment 34.4** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/particle-health/](https://apis.io/providers/particle-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Particle Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/particle-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
