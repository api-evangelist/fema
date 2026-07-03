# OpenFEMA (fema)

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
