# NHS API

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
