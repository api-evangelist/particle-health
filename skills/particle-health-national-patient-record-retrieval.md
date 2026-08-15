---
name: particle-health-national-patient-record-retrieval
description: Authenticate, register a patient, run a national query across Particle's connected health information networks, poll until complete, then collect the aggregated clinical record in C-CDA and FHIR formats.
api: Particle Health
operations:
  - getAuthToken
  - submitPatient
  - createPatientQuery
  - getPatientQueryStatus
  - getCcdaFiles
  - getFhirDatasets
---

# Particle Health: National Patient Record Retrieval

Ground truth: `arazzo/particle-health-patient-record-retrieval-workflow.yml` and
`openapi/particle-health-patients-api-openapi.yml`, `openapi/particle-health-queries-api-openapi.yml`,
`openapi/particle-health-ccda-api-openapi.yml`, `openapi/particle-health-fhir-api-openapi.yml`.
This is the flagship end-to-end flow: pull a longitudinal record for a patient from Particle's
320M+ patient / 160K+ organization footprint (Carequality, CommonWell, eHealth Exchange, TEFCA/QHIN,
state HIEs, Surescripts).

## Steps

1. **Authenticate** — `GET /auth` (operationId `getAuthToken`).
2. **Register the patient** — `POST /api/v2/patients` (operationId `submitPatient`) with
   demographics; get back a Particle Patient ID (PPID).
3. **Launch the national query** — `POST /api/v1/queries` (operationId `createPatientQuery`).
   Behind the scenes Particle updates its Master Patient Index, runs its Record Locator algorithm
   to find candidate network partners, splits the query into per-partner subqueries (often hundreds),
   and de-duplicates/normalizes results as they return (see `docs.particlehealth.com/docs/life-of-a-query`
   for the full internal pipeline).
4. **Poll for completion** — `GET /api/v1/queries/{id}` (operationId `getPatientQueryStatus`), or
   subscribe to the `com.particlehealth.api.v2.query` webhook instead of polling.
5. **Collect the C-CDA record** — `GET /api/v2/patients/{particle_patient_id}/ccda` (operationId
   `getCcdaFiles`) downloads a zip of C-CDA documents (or a single file with its native content type).
6. **Collect the FHIR record** — `GET /api/v2/patients/{particle_patient_id}/fhir` (operationId
   `getFhirDatasets`) returns a FHIR Bundle with paging and incremental sync.

## Rules to carry forward

- Deltas (`particle-health-deltas-api-openapi.yml`) is Particle's recommended flow when you need
  only the data that changed since a prior query for the same patient — swap step 5/6 for the
  equivalent `/deltas/...` endpoints once Deltas is enabled for your account.
- Flat format (`particle-health-flat-api-openapi.yml`) is a third output shape (normalized columnar
  domains: ALLERGIES, ENCOUNTERS, MEDICATIONS, etc.) — same query, different collection endpoint.
- Sandbox base URL `https://sandbox.particlehealth.com` is capped at 500 queries/org/day and returns
  only synthetic patients — see `sandbox/particle-health-sandbox.yml`.
- Standard auth (bearer JWT, 1hr TTL) and rate-limit (429 → back off ~60s) rules apply throughout.
