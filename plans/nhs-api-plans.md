# NHS API Access Plans

## Overview

NHS England APIs are not offered under commercial pricing tiers in the conventional sense. Access is governed by formal onboarding, assurance, and data sharing agreements rather than subscription plans. There are no public pay-as-you-go or freemium tiers. All production access requires approval through the NHS Digital Onboarding Service.

---

## Access Tiers

### 1. Sandbox / Open Access (Development)

- **Who:** Any developer exploring NHS APIs
- **Cost:** Free, no registration required for sandbox endpoints
- **Base URL:** `https://sandbox.api.service.nhs.uk/`
- **Limitations:** Simulated responses; no real patient data; limited to development and testing only
- **Key APIs:** Personal Demographics Service, Electronic Prescription Service, NHS App API, Booking & Referral
- **No onboarding required**

### 2. Integration Testing (Path-to-Live)

- **Who:** Suppliers and organisations progressing through the assurance process
- **Cost:** Free
- **Base URL:** `https://int.api.service.nhs.uk/`
- **Limitations:** Test environment only; requires NHS login or test CIS2 credentials; limited to accredited test accounts
- **Requirement:** Organisation must have started the Digital Onboarding Service process and received integration environment credentials

### 3. Production Access (Clinical / Operational)

- **Who:** Accredited NHS system suppliers and NHS organisations
- **Cost:** Free at point of use; costs may arise from onboarding assurance, infrastructure, and NHS Spine connectivity
- **Base URL:** `https://api.service.nhs.uk/`
- **Limitations:** Full clinical governance and data sharing agreements required; restricted to specific use cases and user groups
- **Requirements:**
  - Registered NHS Organisation Data Service (ODS) code
  - Completed Data Security and Protection Toolkit (DSPT)
  - Passed the Digital Onboarding Service assurance process
  - Signed data sharing and access agreements
  - Clinical Safety Case (where applicable)
  - Supplier Conformance Assessment (SCAL) for certain APIs (e.g., EPS FHIR)

---

## NHS Website Content Syndication API

The NHS Website Content API (for health information syndication) operates under a separate lightweight registration:

- **Tier:** Free with API key
- **Rate Limit:** 4,000 requests per hour (default)
- **Higher Limits:** Available by written agreement with the NHS syndication team
- **Attribution:** Required — NHS logo and link-back mandatory
- **Terms:** Content must be refreshed at least once every 7 days

---

## NHS Login

NHS login for citizen-facing applications uses a separate onboarding track:

- **Cost:** Free (public sector and NHS-commissioned services)
- **Environments:** Sandpit (`auth.sandpit.signin.nhs.uk`), Production (`auth.login.nhs.uk`)
- **Requirements:** Application must be reviewed and approved by the NHS login team; scopes and claims must be individually approved

---

## Key Onboarding Links

- Digital Onboarding Service: https://digital.nhs.uk/developer/guides-and-documentation/onboarding-process
- Digital Assurance: https://digital.nhs.uk/developer/assurance/digital-assurance-for-apis-and-services
- Terms of Use: https://onboarding.prod.api.platform.nhs.uk/PolicyPages/TermsOfUsePolicy
- NHS Open API Policy: https://www.england.nhs.uk/digitaltechnology/connecteddigitalsystems/interoperability/open-api/
