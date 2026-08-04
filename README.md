# OpenFEMA (fema)

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

OpenFEMA is FEMA's open data platform, publishing free, public, machine-readable datasets on disaster declarations, public assistance grants, hazard mitigation projects, the National Flood Insurance Program (NFIP), and emergency alerting through a read-only RESTful API. The API uses OData-style query string parameters (`$filter`, `$select`, `$top`, `$skip`, `$orderby`) over individually versioned dataset endpoints, requires no API key or subscription, and returns JSON, CSV, or Parquet.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fema/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fema/refs/heads/main/apis.yml)

## No pricing, no plans

OpenFEMA is free U.S. government open data. There is no API key, no subscription, no usage-based billing, and no tiered plan structure to document - so this repository intentionally has no `plans/` or `finops/` directory. The only constraint on usage is the per-call record limit described in `rate-limits/fema-rate-limits.yml` (1,000 records per call by default, 10,000 maximum via `$top`, with `$skip`/`$count` paging or the beta `$allrecords=true` for full downloads).

## Tags

- Government
- Open Data
- Emergency Management
- Disaster
- FEMA
- Public Safety

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### FEMA Disaster Declarations Summaries API

Summarized dataset of every official FEMA disaster declaration since 1953 - major disaster, emergency, and fire management assistance declarations - by state, county (FIPS), incident type, and declaration date.

- **Human URL:** [https://www.fema.gov/openfema-data-page/disaster-declarations-summaries-v2](https://www.fema.gov/openfema-data-page/disaster-declarations-summaries-v2)
- **Base URL:** `https://www.fema.gov/api/open/v2`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/disaster-declarations-summaries-v2)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA Public Assistance Funded Projects Details API

Obligated Public Assistance grant projects (project worksheets) funded under the PA program, including damage category, project amount, and federal share obligated. Joins to the Public Assistance Applicants dataset via `applicantId`.

- **Human URL:** [https://www.fema.gov/openfema-data-page/public-assistance-funded-projects-details-v1](https://www.fema.gov/openfema-data-page/public-assistance-funded-projects-details-v1)
- **Base URL:** `https://www.fema.gov/api/open/v1`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/public-assistance-funded-projects-details-v1)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA Hazard Mitigation Assistance Projects API

Funded projects under FEMA's Hazard Mitigation Assistance programs - Hazard Mitigation Grant Program (HMGP), Flood Mitigation Assistance (FMA), and (historically) Pre-Disaster Mitigation (PDM) - including project type, status, and federal cost share obligated.

- **Human URL:** [https://www.fema.gov/about/openfema/data-sets](https://www.fema.gov/about/openfema/data-sets)
- **Base URL:** `https://www.fema.gov/api/open/v3`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/about/openfema/data-sets)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA NFIP Redacted Policies API

Policy-level transactions from the National Flood Insurance Program (NFIP) system of record, redacted to protect policyholder personally identifiable information - coverage amounts, premium, construction, and flood zone attributes by community.

- **Human URL:** [https://www.fema.gov/openfema-data-page/fima-nfip-redacted-policies-v2](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-policies-v2)
- **Base URL:** `https://www.fema.gov/api/open/v2`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-policies-v2)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA NFIP Redacted Claims API

NFIP claims transactions redacted to protect policyholder PII - date of loss, cause of damage, building/contents payouts, and elevation data by community.

- **Human URL:** [https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims-v2](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims-v2)
- **Base URL:** `https://www.fema.gov/api/open/v2`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims-v2)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA IPAWS Archived Alerts API

Archive of public alerts issued through the Integrated Public Alert and Warning System (IPAWS) - the federal system that aggregates EAS, Wireless Emergency Alerts, and NOAA Weather Radio - returned as Common Alerting Protocol (CAP) messages. Hierarchical/nested payload, unique among OpenFEMA datasets.

- **Human URL:** [https://www.fema.gov/openfema-data-page/ipaws-archived-alerts-v1](https://www.fema.gov/openfema-data-page/ipaws-archived-alerts-v1)
- **Base URL:** `https://www.fema.gov/api/open/v1`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/ipaws-archived-alerts-v1)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA Web Disaster Summaries API

Per-disaster financial summary totals - approved Individual Assistance applications, Public Assistance obligations, and Hazard Mitigation grant amounts - sourced raw from FEMA's NEMIS system of record.

- **Human URL:** [https://www.fema.gov/openfema-data-page/fema-web-disaster-summaries-v1](https://www.fema.gov/openfema-data-page/fema-web-disaster-summaries-v1)
- **Base URL:** `https://www.fema.gov/api/open/v1`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/fema-web-disaster-summaries-v1)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FEMA OpenFEMA Dataset Catalog API

Self-describing metadata layer for the whole platform - the `OpenFemaDataSets` endpoint lists every dataset and version, and the `OpenFemaDataSetFields` endpoint returns the data dictionary (field name, type, and description) for any dataset/version pair.

- **Human URL:** [https://www.fema.gov/openfema-data-page/openfema-data-sets-v1](https://www.fema.gov/openfema-data-page/openfema-data-sets-v1)
- **Base URL:** `https://www.fema.gov/api/open/v1`

#### Properties

- [Documentation](https://www.fema.gov/about/openfema/api)
- [API Reference](https://www.fema.gov/openfema-data-page/openfema-data-sets-v1)
- [OpenAPI](openapi/fema-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fema.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fema.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.fema.gov/)
- [Documentation](https://www.fema.gov/about/openfema/api)
- [Rate Limits](rate-limits/fema-rate-limits.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
