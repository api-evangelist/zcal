# Zcal (zcal)

Zcal is a free scheduling platform for booking meetings via shareable scheduling links, meeting polls, and team pages (round-robin and collective). Zcal does not publish a general-purpose public REST API; programmatic integration is delivered through outbound webhooks (event.created, event.rescheduled, event.cancelled) and no-code connectors such as Zapier and Make, plus native integrations including Zoom, Stripe, Google Analytics, and Meta Pixel.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zcal/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zcal/refs/heads/main/apis.yml)

## Tags

- Scheduling
- Calendar
- Booking
- Meetings
- Webhooks

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Zcal Scheduling Links

Unlimited shareable scheduling links, meeting polls, and customizable booking pages let invitees self-serve a time. This is a product surface managed through the Zcal web application; there is no documented public REST API for creating or managing scheduling links programmatically.

- **Human URL:** [https://help.zcal.co/](https://help.zcal.co/)

#### Tags

- Scheduling
- Booking
- Links

#### Properties

- [Documentation](https://help.zcal.co/)
- [Website](https://zcal.co/)
- [OpenAPI](openapi/zcal-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/zcal.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zcal.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zcal Bookings

Bookings (events) capture timing, hosts, attendees, location, and custom question responses. Booking data is surfaced to external systems through outbound webhooks rather than a queryable public REST API.

- **Human URL:** [https://help.zcal.co/](https://help.zcal.co/)

#### Tags

- Bookings
- Events
- Attendees

#### Properties

- [Documentation](https://help.zcal.co/)
- [Website](https://zcal.co/)
- [OpenAPI](openapi/zcal-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/zcal.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zcal.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zcal Integrations and Webhooks

Outbound webhooks POST a JSON payload to a subscriber URL when a booking is created, rescheduled, or cancelled. Payloads can be verified with an optional HMAC SHA-256 signature via the x-zcal-webhook-signature header. Connectors such as Zapier and Make, plus native Zoom, Stripe, Google Analytics, and Meta Pixel integrations, extend automation without a public REST API.

- **Human URL:** [https://help.zcal.co/integrations/webhooks](https://help.zcal.co/integrations/webhooks)

#### Tags

- Webhooks
- Integrations
- Automation

#### Properties

- [Documentation](https://help.zcal.co/integrations/webhooks)
- [Documentation](https://help.zcal.co/integrations/webhooks/webhook-payload)
- [OpenAPI](openapi/zcal-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/zcal.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zcal.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/zcal)
- [Website](https://zcal.co/)
- [Documentation](https://help.zcal.co/)
- [Plans](plans/zcal-plans-pricing.yml)
- [Rate Limits](rate-limits/zcal-rate-limits.yml)
- [Fin Ops](finops/zcal-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

## Note on API Availability

As of this catalog entry (2026-06-21), Zcal does **not** offer a documented, general-purpose public REST API. The only documented programmatic surface is **outbound webhooks** that notify a subscriber URL of booking lifecycle events. Inbound automation (creating links, reading bookings) is handled through no-code platforms (Zapier, Make) and native product integrations, not a published HTTP API. The OpenAPI document in this repository therefore declares an empty `paths: {}` and documents the webhook surface in its description; it does not fabricate REST endpoints.
