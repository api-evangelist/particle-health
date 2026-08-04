# Particle Health (particle-health)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Particle Health is a healthcare data interoperability platform that aggregates patient medical records from across the US healthcare system into a single RESTful API. Particle is connected to all three nationwide health information exchange networks (Carequality, CommonWell, eHealth Exchange), TEFCA / QHIN partners, state HIEs (Healthix in New York, Manifest MedEx in California), and Surescripts for pharmacy data. The platform exposes patient demographics, clinical resources, and document retrieval via FHIR R4, C-CDA, Flat, and Deltas formats, layered with deduplication, normalization, AI summarization (Particle Snapshot), real-time encounter and transition alerts (Particle Signal), and longitudinal patient journey tracking (Particle Navigator). Customer segments include value-based care organizations, payers, health systems, primary and specialty providers, and digital health developers.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/particle-health/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/particle-health/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- ADT
- C-CDA
- Care Coordination
- Carequality
- Clinical Data
- CommonWell
- Deltas
- eHealth Exchange
- EHR
- FHIR
- Health Data
- Health Information Exchange
- Healthcare
- HIE
- HL7
- HL7v2
- Interoperability
- Medical Records
- Patients
- Pharmacy
- QHIN
- Surescripts
- TEFCA
- USCDI

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Particle Health API

The Particle Health API is a RESTful interface for patient demographic registration, clinical data querying, and document retrieval across all major US health information networks. Developers register a patient via demographics, submit a query under a defined Purpose of Use, and asynchronously receive normalized clinical data in FHIR R4 Bundles, C-CDA documents, Flat datasets, or Deltas (incremental change sets). The API also exposes batch query, network participant search, patient provider mapping, and webhook event notifications for query completion, ADT, transitions, encounters, and AI output. Authentication uses OAuth 2 Client-Credentials grant with JWT access tokens scoped to a project.

- **Human URL:** [https://docs.particlehealth.com/](https://docs.particlehealth.com/)
- **Base URL:** `https://api.particlehealth.com`

#### Tags

- C-CDA
- Carequality
- CommonWell
- Deltas
- eHealth Exchange
- FHIR
- Health Data
- HIE
- HL7
- HL7v2
- Interoperability
- Patients
- QHIN
- TEFCA
- USCDI

#### Properties

- [Documentation](https://docs.particlehealth.com/)
- [API Reference](https://docs.particlehealth.com/reference/getting-started)
- [Authentication](https://docs.particlehealth.com/docs/auth-and-keys)
- [Getting Started](https://docs.particlehealth.com/docs/getting-started-for-developers)
- [Sandbox](https://docs.particlehealth.com/docs/test-patient-sandbox)
- [Postman](https://www.postman.com/particlehealth/particle-health-api) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [L L Ms](https://docs.particlehealth.com/llms.txt)
- [Webhooks](https://docs.particlehealth.com/docs/webhook-event-notifications)
- [Rate Limits](https://docs.particlehealth.com/docs/rate-limiting-and-quotas)
- [Supported F H I R Resources](https://docs.particlehealth.com/docs/supported-fhir-resources)
- [Networks](https://docs.particlehealth.com/docs/networks)
- [Data Normalization](https://docs.particlehealth.com/docs/data-normalization)
- [Data Deduplication](https://docs.particlehealth.com/docs/data-deduplication)
- [Data Provenance](https://docs.particlehealth.com/docs/data-provenance)
- [Purposes Of Use](https://docs.particlehealth.com/docs/purposes-of-use)
- [Delegation Of Authority](https://docs.particlehealth.com/docs/delegation-of-authority)
- [OpenAPI](openapi/particle-health-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/particle-health.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/particle-health.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](spectral/particle-health-spectral.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)

## Common Properties

- [GitHub Organization](https://github.com/ParticleHealth)
- [LinkedIn](https://www.linkedin.com/company/particle-health)
- [Twitter](https://twitter.com/particle_health)
- [YouTube](https://www.youtube.com/channel/UCMT35sx6GKvA1mzMP6qyVkw)
- [Website](https://particlehealth.com/)
- [Documentation](https://docs.particlehealth.com/)
- [API Reference](https://docs.particlehealth.com/reference/getting-started)
- [Developer](https://docs.particlehealth.com/docs/getting-started-for-developers)
- [Sandbox](https://docs.particlehealth.com/docs/test-patient-sandbox)
- [Status Page](https://status.particlehealth.com/)
- [Changelog](https://docs.particlehealth.com/docs/)
- [Glossary](https://docs.particlehealth.com/docs/glossary)
- [Blog](https://particlehealth.com/blog)
- [Resources](https://particlehealth.com/resources)
- [Contact](https://particlehealth.com/contact)
- [Support](undefined)
- [Compliance Contact](undefined)
- [Media Contact](undefined)
- [Press Releases](https://particlehealth.com/blog)
- [Postman](https://www.postman.com/particlehealth/particle-health-api) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [L L Ms](https://docs.particlehealth.com/llms.txt)
- [JSON-LD](json-ld/particle-health-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/particle-health-patient-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/particle-health-query-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Plans](plans/particle-health-plans-pricing.yml)
- [Rate Limits](rate-limits/particle-health-rate-limits.yml)
- [Fin Ops](finops/particle-health-finops.yml)
- [Vocabulary](vocabulary/particle-health-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
