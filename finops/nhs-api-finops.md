# NHS API FinOps

## Overview

NHS England APIs are publicly funded and free at the point of use for NHS-commissioned services and accredited NHS IT suppliers. There is no monetary pricing model, API metering fee, or usage-based billing. Cost considerations are operational in nature, not transactional.

---

## Cost Model

### Direct API Costs
- **Zero** — No per-call fees, no subscription fees, no tiered billing for any NHS API.
- The NHS API platform is funded by NHS England as part of the national digital infrastructure for health.

### Indirect / Operational Costs

Organisations integrating with NHS APIs should budget for the following:

| Cost Category | Description |
|---|---|
| Onboarding / Assurance | Staff time for completing Digital Onboarding Service, Data Security and Protection Toolkit (DSPT), and clinical safety assessments |
| SCAL Compliance | Supplier Conformance Assessment (SCAL) for EPS, GP Connect, and other regulated APIs requires dedicated engineering and QA resource |
| Infrastructure | Spine-connected APIs may require NHS Spine connection, NHS network (HSCN), or dedicated infrastructure |
| HSCN Connectivity | Access to certain Spine APIs requires Health and Social Care Network (HSCN) connectivity, which carries its own contract and cost |
| Legal & IG | Information Governance agreements, Data Sharing Agreements, and legal review for data access agreements |
| Clinical Safety | DCB0129 / DCB0160 clinical safety case documentation for clinical systems |

---

## NHS Website Content Syndication

The Content Syndication API is free but governed by terms of use:
- Attribution to the NHS website is mandatory (NHS logo + link-back)
- Content must be refreshed no less than once every 7 days
- Exceeding 4,000 requests/hour without written agreement may result in access suspension
- No commercial use of syndicated content without explicit permission

---

## NHS Login (Citizen Identity)

- Free for NHS-commissioned services and approved third-party health apps
- Private commercial applications may be required to demonstrate public benefit and undergo additional review
- No per-login fee; no OAuth token metering

---

## Budget Planning Guidance

For organisations building NHS-integrated applications:

1. **Engineering hours:** Allow 3–12 months for full onboarding and assurance depending on API complexity
2. **HSCN costs:** Contact HSCN suppliers (BT, Vodafone, etc.) for network pricing if Spine connectivity is required
3. **Compliance overhead:** DSPT annual submission + clinical safety documentation are recurring costs
4. **Support:** NHS England Developer Community and Developer Support (api.management@nhs.net) are free

---

## Key Resources

- Open API Policy: https://www.england.nhs.uk/digitaltechnology/connecteddigitalsystems/interoperability/open-api/
- Digital Onboarding: https://digital.nhs.uk/developer/guides-and-documentation/onboarding-process
- HSCN Information: https://digital.nhs.uk/services/health-and-social-care-network
- Data Security and Protection Toolkit: https://www.dsptoolkit.nhs.uk/
- Terms of Use: https://onboarding.prod.api.platform.nhs.uk/PolicyPages/TermsOfUsePolicy
