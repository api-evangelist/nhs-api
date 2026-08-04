# NHS API

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

NHS England's API management platform providing FHIR R4 and REST APIs for healthcare interoperability across the NHS. The platform covers GP Connect (appointment management and access record), Personal Demographics Service, Electronic Prescription Service, Summary Care Records, NHS login (OpenID Connect for citizens), Booking and Referral, Organisation Data Service, and content syndication.

**Developer Portal:** https://digital.nhs.uk/developer  
**API Catalogue:** https://digital.nhs.uk/developer/api-catalogue  
**GitHub:** https://github.com/NHSDigital  
**Developer Community:** https://developer.community.nhs.uk/

## APIs Catalogued

| API | Description |
|---|---|
| Personal Demographics Service - FHIR API | Search, retrieve, and update patient demographic data from the national NHS patient database |
| GP Connect Access Record Structured - FHIR API | Retrieve structured clinical records (medications, allergies, consultations) from GP practices |
| GP Connect Appointment Management - FHIR API | Book, amend, and cancel GP practice appointments |
| GP Connect Access Document - FHIR API | Retrieve clinical documents stored at GP practices |
| Electronic Prescription Service - FHIR API | Create, sign, dispense, and track NHS electronic prescriptions |
| EPS Prescription Tracker - FHIR API | Track real-time prescription status within EPS |
| NHS Login API | OpenID Connect identity service for citizen authentication |
| Booking and Referral - FHIR API | Send booking and referral information between NHS service providers |
| Organisation Data Service - FHIR API | Access NHS organisation reference data by ODS code |
| NHS Website Content API | Syndicate NHS-approved health information content |
| Spine Directory Service - FHIR API | Discover endpoint and accreditation data for NHS Spine-connected systems |
| NHS e-Referral Service - FHIR API | Manage outpatient referrals between primary and secondary care |
| Elective Waiting List API | Access national NHS waiting list data |

## Authentication

NHS APIs use a layered authentication model:

- **CIS2 / NHS Smartcard OAuth2** — For healthcare worker user-restricted access (GP Connect, PDS, EPS)
- **Application-restricted (signed JWT)** — For machine-to-machine / system-level access
- **NHS Login (OIDC)** — For citizen-facing applications

## Environments

| Environment | Base URL |
|---|---|
| Sandbox | `https://sandbox.api.service.nhs.uk/` |
| Integration | `https://int.api.service.nhs.uk/` |
| Production | `https://api.service.nhs.uk/` |

## Access & Onboarding

All production access requires formal onboarding through the NHS Digital Onboarding Service. There are no commercial pricing tiers — APIs are free at the point of use for NHS-commissioned services and accredited suppliers. See [plans/nhs-api-plans.md](plans/nhs-api-plans.md) for details.

## Rate Limits

The NHS Website Content API has a default limit of 4,000 requests/hour. Clinical API rate limits are agreed during onboarding. See [rate-limits/nhs-api-rate-limits.md](rate-limits/nhs-api-rate-limits.md) for details.

## Files

- `apis.yml` — APIs.json 0.19 provider profile
- `plans/nhs-api-plans.md` — Access plans and onboarding tiers
- `rate-limits/nhs-api-rate-limits.md` — Rate limiting documentation
- `finops/nhs-api-finops.md` — Cost and FinOps guidance
