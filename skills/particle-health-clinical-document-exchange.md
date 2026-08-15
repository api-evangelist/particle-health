---
name: particle-health-clinical-document-exchange
description: Submit a clinical document (e.g., a C-CDA or discharge summary) into a patient's Particle Health record, then read it back and list every document on file for that patient.
api: Particle Health
operations:
  - getAuthToken
  - submitDocument
  - getDocument
  - getPatientDocuments
---

# Particle Health: Clinical Document Exchange

Ground truth: `arazzo/particle-health-clinical-document-exchange-workflow.yml` and
`openapi/particle-health-documents-api-openapi.yml`.

## Steps

1. **Authenticate** — `GET /auth` (operationId `getAuthToken`); bearer JWT, 1-hour TTL.
2. **Submit the document** — `POST /api/v1/documents` (operationId `submitDocument`) with the
   document payload plus metadata (patient reference, MIME type, e.g. CCDA or discharge summary).
   Returns a document ID.
3. **Read it back** — `GET /api/v1/documents/{id}` (operationId `getDocument`) to retrieve the
   single document and its metadata (confirms ingestion/linkage succeeded).
4. **List all documents for the patient** — `GET /api/v1/documents/patient/{id}` (operationId
   `getPatientDocuments`) to enumerate every document Particle has on file for that patient
   (internal ID or Particle Patient ID accepted).

## Rules to carry forward

- `DELETE /api/v1/documents/{id}` (operationId `deleteDocument`) exists in the same OpenAPI file for
  removing a submitted document — not part of this workflow's happy path but available.
- No documented idempotency-key header — resubmitting the same document payload was not confirmed to
  dedupe; treat each submit call as creating a new document unless you track IDs client-side.
- Auth, rate-limit, and sandbox rules are identical to the other Particle Health flows — see
  `authentication/particle-health-authentication.yml` and `rate-limits/particle-health-rate-limits.yml`.
