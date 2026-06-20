# Sieve (sieve)

Sieve is an AI media-processing platform that exposes prebuilt functions and apps for video, audio, and image understanding - transcription, dubbing, lip-sync, object tracking and segmentation, background removal, and more. Functions are run asynchronously as jobs via a single REST push endpoint, with results retrieved by polling or delivered via webhooks.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sieve/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sieve/refs/heads/main/apis.yml)

## Tags

- AI
- Video
- Audio
- Media Processing
- Async Jobs

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Sieve Jobs Push API

Submit a function or app to run as an asynchronous job via POST /push, passing the function name (author/name[:version]) and an inputs object. Returns a job id used to track status and retrieve outputs.

- **Human URL:** [https://docs.sievedata.com/guide/integration/integrate-apis](https://docs.sievedata.com/guide/integration/integrate-apis)
- **Base URL:** `https://mango.sievedata.com/v2`

#### Tags

- Jobs
- Push
- Async

#### Properties

- [Documentation](https://docs.sievedata.com/guide/integration/integrate-apis)
- [API Reference](https://docs.sievedata.com/reference-v2/api/push-new-job)
- [OpenAPI](openapi/sieve-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sieve.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sieve.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sieve Jobs Status API

Retrieve a single job by id (GET /jobs/{job_id}) with its status, outputs, and error, list all organization jobs (GET /jobs) filtered by status, and cancel a running job (DELETE /jobs/{job_id}).

- **Human URL:** [https://docs.sievedata.com/reference-v2/api/get-job](https://docs.sievedata.com/reference-v2/api/get-job)
- **Base URL:** `https://mango.sievedata.com/v2`

#### Tags

- Jobs
- Status
- Outputs

#### Properties

- [Documentation](https://docs.sievedata.com/reference-v2/api/get-job)
- [API Reference](https://docs.sievedata.com/reference-v2/api/list-jobs)
- [OpenAPI](openapi/sieve-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sieve.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sieve.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sieve Functions API

Look up metadata for a public or custom function by owner and name (GET /functions/{owner_name}/{function_name}), including the latest version, its inputs, outputs, and runtime configuration.

- **Human URL:** [https://docs.sievedata.com/reference-v2/api/get-function](https://docs.sievedata.com/reference-v2/api/get-function)
- **Base URL:** `https://mango.sievedata.com/v2`

#### Tags

- Functions
- Catalog
- Apps

#### Properties

- [Documentation](https://docs.sievedata.com/reference-v2/api/get-function)
- [API Reference](https://docs.sievedata.com/reference-v2/api/get-function)
- [OpenAPI](openapi/sieve-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sieve.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sieve.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Sieve Webhooks API

Register webhook callbacks on a job (via the webhooks array on POST /push) so Sieve POSTs notifications - job.start, job.complete, job.complete.no_output, job.new_output - to your URL instead of polling. Retried up to ten times with exponential backoff until a 200 is received.

- **Human URL:** [https://docs.sievedata.com/guide/integration/webhooks](https://docs.sievedata.com/guide/integration/webhooks)
- **Base URL:** `https://mango.sievedata.com/v2`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://docs.sievedata.com/guide/integration/webhooks)
- [OpenAPI](openapi/sieve-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sieve.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sieve.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/sieve-community)
- [LinkedIn](https://www.linkedin.com/company/sievedata)
- [Website](https://www.sievedata.com)
- [Documentation](https://docs.sievedata.com)
- [Plans](plans/sieve-plans-pricing.yml)
- [Rate Limits](rate-limits/sieve-rate-limits.yml)
- [Fin Ops](finops/sieve-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
