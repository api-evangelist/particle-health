---
name: particle-health-fhir-r4-resource-query
description: Create a FHIR R4 Patient resource in Particle Health, run a FHIR-native network query, poll it to completion, then search and read individual US Core resources.
api: Particle Health
operations:
  - getAuthToken
  - createFhirPatient
  - createFhirPatientQuery
  - getFhirPatientQueryStatus
  - getFhirPatientEverything
  - searchFhirResources
  - readFhirResource
---

# Particle Health: FHIR R4 Resource Query

Ground truth: `arazzo/particle-health-fhir-r4-resource-query-workflow.yml` and
`openapi/particle-health-fhir-api-openapi.yml`. Docs note this is Particle's **legacy** but still
supported FHIR query flow for existing customers — new customers are onboarded onto Deltas or CCDA
instead (`docs.particlehealth.com/docs/legacy-api-implementation`).

## Steps

1. **Authenticate** — `GET /auth` (operationId `getAuthToken`).
2. **Create a FHIR Patient** — `POST /r4/Patient` (operationId `createFhirPatient`) with demographics.
   Returns a FHIR Patient resource with an ID.
3. **Launch the query** — `POST /r4/Patient/{patient_id}/query` (operationId
   `createFhirPatientQuery`) starts a network query against Carequality/CommonWell for that patient.
4. **Poll for completion** — `GET /r4/Patient/{patient_id}/query` (operationId
   `getFhirPatientQueryStatus`) until the query reaches a terminal state.
5. **Collect everything** — `GET /r4/Patient/{patient_id}/$everything` (operationId
   `getFhirPatientEverything`) returns a FHIR Bundle of every resource retrieved, paged.
6. **Search a specific resource type** — `GET /r4/{resource_type}` (operationId
   `searchFhirResources`), scoped to the patient, to narrow to one US Core resource type
   (e.g. `Encounter`, `Condition`, `MedicationStatement`).
7. **Read a single resource** — `GET /r4/{resource_type}/{resource_id}` (operationId
   `readFhirResource`) to fetch one resource by type and ID.

## Rules to carry forward

- This is the legacy flow; the Deltas API (`particle-health-deltas-api-openapi.yml`) is Particle's
  recommended replacement and adds incremental/delta retrieval on top of the same query mechanics.
- Webhook notification on query completion follows CloudEvents type
  `com.particlehealth.api.v2.query` — poll OR subscribe to the webhook, not both, to avoid racing.
- Standard auth/rate-limit/sandbox rules apply.
