---
name: particle-health-network-provider-discovery
description: Register a patient, run a network query, then discover which healthcare organizations and providers across Particle's connected networks hold records for that patient.
api: Particle Health
operations:
  - getAuthToken
  - submitPatient
  - createPatientQuery
  - getPatientQueryStatus
  - getPatientProviderMap
  - searchNetworkParticipantsByState
---

# Particle Health: Network Provider Discovery

Ground truth: `arazzo/particle-health-network-provider-discovery-workflow.yml` and
`openapi/particle-health-patients-api-openapi.yml`, `openapi/particle-health-queries-api-openapi.yml`,
`openapi/particle-health-providermap-api-openapi.yml`,
`openapi/particle-health-networkparticipants-api-openapi.yml`.

## Steps

1. **Authenticate** — `GET /auth` (operationId `getAuthToken`).
2. **Register the patient** — `POST /api/v2/patients` (operationId `submitPatient`) to get a PPID.
3. **Launch a network query** — `POST /api/v1/queries` (operationId `createPatientQuery`) starts a
   one-time query across connected HIEs/TEFCA partners.
4. **Poll for completion** — `GET /api/v1/queries/{id}` (operationId `getPatientQueryStatus`).
5. **Read the provider map** — `GET` the Patient Provider Map endpoint (operationId
   `getPatientProviderMap`) to get the set of healthcare organizations associated with the patient,
   each enriched with directory info (NPI, address, managing organization). Requires the Patient
   Provider Map feature to be enabled on the project — contact Particle to turn it on. Returns an
   empty `providers` array (not an error) when there is nothing on file.
6. **Search the network directory directly** — `GET /api/v1/networkparticipants/state/{state}`
   (operationId `searchNetworkParticipantsByState`) to browse organizations in Particle's connected
   networks by state (siblings exist for zip code search) — useful for locating Centers of Excellence
   or specialty providers independent of a specific patient.

## Rules to carry forward

- Patient Provider Map is a gated feature — do not assume it is available on every project; a `403`
  or feature-disabled response is expected until Particle enables it.
- Standard auth/rate-limit/sandbox rules apply.
