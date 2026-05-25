# Particle Health (particle-health)

Particle Health is a healthcare data interoperability platform that aggregates patient medical records from across the US healthcare system into a single RESTful API. Particle is connected to all three nationwide health information exchange networks (Carequality, CommonWell, eHealth Exchange), TEFCA / QHIN partners, state HIEs (Healthix in New York, Manifest MedEx in California), and Surescripts for pharmacy data. The platform exposes patient demographics, clinical resources, and document retrieval via FHIR R4, C-CDA, Flat, and Deltas formats, layered with deduplication, normalization, AI summarization (Particle Snapshot), real-time encounter and transition alerts (Particle Signal), and longitudinal patient journey tracking (Particle Navigator).

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/particle-health/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- ADT, C-CDA, Care Coordination, Carequality, Clinical Data, CommonWell, Deltas, eHealth Exchange, EHR, FHIR, Health Data, Health Information Exchange, Healthcare, HIE, HL7, HL7v2, Interoperability, Medical Records, Patients, Pharmacy, QHIN, Surescripts, TEFCA, USCDI

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Particle Health API

The Particle Health API is a RESTful interface for patient demographic registration, clinical data querying, and document retrieval across all major US health information networks. Developers register a patient via demographics, submit a query under a defined Purpose of Use, and asynchronously receive normalized clinical data in FHIR R4 Bundles, C-CDA documents, Flat datasets, or Deltas (incremental change sets). The API also exposes batch query, network participant search, patient provider mapping, and webhook event notifications for query completion, ADT, transitions, encounters, and AI output. Authentication uses OAuth 2 Client-Credentials grant with JWT access tokens scoped to a project.

**Human URL:** [https://docs.particlehealth.com/](https://docs.particlehealth.com/)

**Base URL:** `https://api.particlehealth.com`

#### Tags

- C-CDA, Carequality, CommonWell, Deltas, eHealth Exchange, FHIR, Health Data, HIE, HL7, HL7v2, Interoperability, Patients, QHIN, TEFCA, USCDI

#### Properties

- [Documentation](https://docs.particlehealth.com/)
- [API Reference](https://docs.particlehealth.com/reference/getting-started)
- [Authentication](https://docs.particlehealth.com/docs/auth-and-keys)
- [Getting Started for Developers](https://docs.particlehealth.com/docs/getting-started-for-developers)
- [Test Patient Sandbox](https://docs.particlehealth.com/docs/test-patient-sandbox)
- [Postman Collection](https://www.postman.com/particlehealth/particle-health-api)
- [LLMs.txt](https://docs.particlehealth.com/llms.txt)
- [Webhook Event Notifications](https://docs.particlehealth.com/docs/webhook-event-notifications)
- [Rate Limiting & Quotas](https://docs.particlehealth.com/docs/rate-limiting-and-quotas)
- [Supported FHIR Resources](https://docs.particlehealth.com/docs/supported-fhir-resources)
- [Networks and HIEs](https://docs.particlehealth.com/docs/networks)
- [Data Normalization](https://docs.particlehealth.com/docs/data-normalization)
- [Data Deduplication](https://docs.particlehealth.com/docs/data-deduplication)
- [Data Provenance](https://docs.particlehealth.com/docs/data-provenance)
- [Purposes of Use](https://docs.particlehealth.com/docs/purposes-of-use)
- [Delegation of Authority (DAuth)](https://docs.particlehealth.com/docs/delegation-of-authority)
- [OpenAPI](openapi/particle-health-openapi.yml)
- [Spectral Ruleset](spectral/particle-health-spectral.yml)

#### Naftiko Capabilities

- [Patients](capabilities/particle-health-patients.yaml)
- [Queries](capabilities/particle-health-queries.yaml)
- [FHIR](capabilities/particle-health-fhir.yaml)
- [Deltas](capabilities/particle-health-deltas.yaml)
- [Flat](capabilities/particle-health-flat.yaml)
- [CCDA](capabilities/particle-health-ccda.yaml)
- [Documents](capabilities/particle-health-documents.yaml)
- [Batches](capabilities/particle-health-batches.yaml)
- [Signal](capabilities/particle-health-signal.yaml)
- [Subscriptions](capabilities/particle-health-subscriptions.yaml)
- [Network Participants](capabilities/particle-health-network-participants.yaml)
- [HL7v2](capabilities/particle-health-hl7v2.yaml)

## Connected Networks

- Carequality
- CommonWell Health Alliance
- eHealth Exchange
- TEFCA Trusted Exchange Framework / QHIN
- Healthix (NY HIE)
- Manifest MedEx (CA HIE)
- Surescripts (Pharmacy Data)

## Products

- **Particle Insights Platform** — core data integration and interoperability platform
- **Particle Snapshot** — AI-generated clinical history summaries
- **Particle Signal** — real-time encounter, ADT, and transition alerts
- **Particle Workbench** — analytics surface for builder and data teams
- **Particle Navigator** — longitudinal patient journey tracking
- **Particle FOCUS** — pre-curated, specialty-specific datasets
- **TEFCA in a Box** — simplified TEFCA / QHIN network integration

## Solutions

- Value-Based Care Patient Data Aggregation
- Readmission Reduction with ADT Alerts
- Care Gap Closure
- Referral Management and Continuity of Care
- Patient Risk Stratification
- Treatment Eligibility Determination
- Medication Management and Reconciliation
- Pre-Visit Chart Preparation
- AI-Powered Clinical Summarization

## Common Properties

- [Website](https://particlehealth.com/)
- [Documentation](https://docs.particlehealth.com/)
- [API Reference](https://docs.particlehealth.com/reference/getting-started)
- [Getting Started for Developers](https://docs.particlehealth.com/docs/getting-started-for-developers)
- [Test Patient Sandbox](https://docs.particlehealth.com/docs/test-patient-sandbox)
- [Status Page](https://status.particlehealth.com/)
- [Glossary](https://docs.particlehealth.com/docs/glossary)
- [Blog](https://particlehealth.com/blog)
- [Contact](https://particlehealth.com/contact)
- [Postman Collection](https://www.postman.com/particlehealth/particle-health-api)
- [LLMs.txt](https://docs.particlehealth.com/llms.txt)
- [GitHub Organization](https://github.com/ParticleHealth)
- [LinkedIn](https://www.linkedin.com/company/particle-health)
- [Twitter](https://twitter.com/particle_health)
- [YouTube](https://www.youtube.com/channel/UCMT35sx6GKvA1mzMP6qyVkw)
- [JSON-LD Context](json-ld/particle-health-context.jsonld)
- [Patient JSON Schema](json-schema/particle-health-patient-schema.json)
- [Query JSON Schema](json-schema/particle-health-query-schema.json)
- [Plans & Pricing](plans/particle-health-plans-pricing.yml)
- [Rate Limits](rate-limits/particle-health-rate-limits.yml)
- [FinOps](finops/particle-health-finops.yml)
- [Vocabulary](vocabulary/particle-health-vocabulary.yml)

## Contacts

- **General:** contact@particlehealth.com
- **Support:** support@particlehealth.com
- **Compliance:** compliance@particlehealth.com
- **Media:** media@particlehealth.com

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
