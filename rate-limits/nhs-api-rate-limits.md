# NHS API Rate Limits

## Overview

NHS England's API platform (built on Apigee) applies rate limiting across its API portfolio. Specific published limits vary by API. The platform uses SpikeArrest and quota policies to protect backend clinical systems. Most limits are not publicly documented at the per-API level and are communicated during the onboarding process.

---

## Known Published Rate Limits

### NHS Website Content Syndication API
- **Default:** 4,000 requests per hour
- **Higher volumes:** Must be pre-arranged in writing with the NHS syndication team
- **Cache requirement:** Syndicated content must be refreshed at least once every 7 days

### General API Platform (Apigee)
- NHS England operates its API management platform using Apigee Edge / Apigee X.
- Rate limiting is enforced centrally at the gateway for all registered client applications.
- SpikeArrest policies smooth traffic spikes by distributing limits across smaller intervals.
- Quota enforcement is per-application key (API key or OAuth client).

---

## Environments and Their Characteristics

| Environment | Base URL | Rate Limits |
|---|---|---|
| Sandbox | `https://sandbox.api.service.nhs.uk/` | Lenient; simulated responses |
| Integration | `https://int.api.service.nhs.uk/` | Moderate; for testing against live-like systems |
| Production | `https://api.service.nhs.uk/` | Enforced; documented during onboarding |

---

## Clinical APIs (GP Connect, EPS, PDS)

- Rate limits for clinical APIs (Personal Demographics Service, GP Connect, Electronic Prescription Service) are not published on the public developer portal.
- Limits are agreed upon during the assurance and onboarding process specific to each supplier's use case and estimated throughput.
- Applications must declare expected volume during onboarding; unexpected volume spikes may result in throttling or suspension.

---

## HTTP Status Codes for Rate Limiting

When rate limits are exceeded, the NHS API platform returns:

- `429 Too Many Requests` — quota or rate limit exceeded
- `503 Service Unavailable` — downstream system unavailable or overloaded

Applications should implement exponential backoff and honour `Retry-After` response headers.

---

## Best Practices

1. Cache responses where clinically appropriate (e.g., organisation reference data, terminology)
2. Use sandbox environments for load testing; never load-test production
3. Contact NHS England Developer Support (api.management@nhs.net) before any high-volume integration
4. Declare expected peak throughput during the Digital Onboarding Service process
5. Implement circuit breakers and graceful degradation for critical clinical integrations

---

## References

- API Policies: https://digital.nhs.uk/developer/guides-and-documentation/api-policies-and-best-practice
- NHS Developer Community (rate limiting discussion): https://developer.community.nhs.uk/t/rate-limiting-specifically-content-syndication-api/3047
- Digital Onboarding Service: https://digital.nhs.uk/developer/guides-and-documentation/onboarding-process
