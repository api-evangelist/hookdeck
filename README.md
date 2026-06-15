# Hookdeck (hookdeck)

Hookdeck is a Toronto-based webhook and event-infrastructure platform. The Hookdeck Event Gateway sits between webhook senders and your services to receive, verify, queue, retry, transform, filter, route, and observe events reliably at scale. Hookdeck exposes a fully versioned REST Admin API, a CLI for local development, language SDKs (TypeScript, Go, Python, .NET), a Terraform provider, and the open-source Outpost project for self-hostable outbound webhook delivery.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hookdeck/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hookdeck/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Webhooks
- Event Gateways
- Gateways
- Events
- Event Infrastructure
- Event-Driven
- Messaging
- Queues
- Retries
- Transformations
- Observability

## Timestamps

- **Created:** 2025-08-19
- **Modified:** 2026-05-25

## APIs

### Hookdeck Connections API

Create, update, list, archive, pause, and unpause connections. A connection routes events from a Source to a Destination and may carry rules (retry, alert, transform, filter, delay) that determine how the gateway processes events along that path.

- **Human URL:** [https://hookdeck.com/docs/api](https://hookdeck.com/docs/api)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Webhooks
- Event Gateways
- Connections

#### Properties

- [Documentation](https://hookdeck.com/docs/api)
- [OpenAPI](openapi/hookdeck-connections-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-connections-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-connections-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-connection-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Sources API

Manage sources — the upstream endpoints (webhook senders or push channels) that ingest events into Hookdeck. Sources support platform-specific verification (Stripe, GitHub, Twilio, Shopify, and many more), allowed HTTP methods, allowed content types, allowed IPs, and a configurable custom response returned to the caller.

- **Human URL:** [https://hookdeck.com/docs/sources](https://hookdeck.com/docs/sources)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Webhooks
- Sources
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/sources)
- [OpenAPI](openapi/hookdeck-sources-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-sources-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-sources-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-source-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Destinations API

Manage destinations — the downstream targets (HTTP endpoints, AWS SQS, Azure Service Bus, GCP Pub/Sub, Kafka, RabbitMQ, MongoDB, and more) where Hookdeck delivers events. Supports configurable auth methods, rate limiting, path forwarding, archival, and pause/disable controls.

- **Human URL:** [https://hookdeck.com/docs/destinations](https://hookdeck.com/docs/destinations)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Webhooks
- Destinations
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/destinations)
- [OpenAPI](openapi/hookdeck-destinations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-destinations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-destinations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-destination-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Events API

List, retrieve, retry, mute, and inspect events and their delivery attempts. An event is any request Hookdeck received from a source; an attempt is each delivery try against a destination, including status, response body, response time, and error code.

- **Human URL:** [https://hookdeck.com/docs/events](https://hookdeck.com/docs/events)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Webhooks
- Events
- Attempts
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/events)
- [OpenAPI](openapi/hookdeck-events-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-events-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-events-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hookdeck-attempt-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Requests API

List and inspect raw requests received by Hookdeck. A request precedes events and is what gets accepted at the gateway boundary before verification, fan-out, transformation, and routing produce one or more downstream events.

- **Human URL:** [https://hookdeck.com/docs/requests](https://hookdeck.com/docs/requests)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Webhooks
- Requests
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/requests)
- [OpenAPI](openapi/hookdeck-requests-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-requests-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-requests-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-request-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Transformations API

Manage transformations — sandboxed JavaScript executed against events to mutate headers, body, path, or query string before delivery. Also includes a sandboxed run endpoint for testing transformation code against sample event payloads.

- **Human URL:** [https://hookdeck.com/docs/transformations](https://hookdeck.com/docs/transformations)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Transformations
- Webhooks
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/transformations)
- [OpenAPI](openapi/hookdeck-transformations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-transformations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-transformations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-transformation-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Bookmarks API

Save bookmarked events for quick replay and one-click testing during development. Bookmarks let your team capture canonical event payloads and trigger them on demand into any destination.

- **Human URL:** [https://hookdeck.com/docs/bookmarks](https://hookdeck.com/docs/bookmarks)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Bookmarks
- Webhooks
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/bookmarks)
- [OpenAPI](openapi/hookdeck-bookmarks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-bookmarks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-bookmarks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hookdeck Bulk Operations API

Plan, schedule, and cancel bulk operations that retry or cancel many events, requests, or ignored events at once. Each bulk operation reports per-batch counts, total scope, and live progress, and can be cancelled mid-run.

- **Human URL:** [https://hookdeck.com/docs/bulk-retries](https://hookdeck.com/docs/bulk-retries)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Bulk Operations
- Webhooks
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/bulk-retries)
- [OpenAPI](openapi/hookdeck-bulk-operations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-bulk-operations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-bulk-operations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hookdeck Issues API

Track issues that occur on events, requests, and backpressure, and manage the triggers (rules) that open and route issues to Slack, Email, Microsoft Teams, Discord, BetterUptime, and other channels.

- **Human URL:** [https://hookdeck.com/docs/issues](https://hookdeck.com/docs/issues)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Issues
- Issue Triggers
- Observability

#### Properties

- [Documentation](https://hookdeck.com/docs/issues)
- [OpenAPI](openapi/hookdeck-issues-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-issues-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-issues-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hookdeck-issue-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Hookdeck Metrics API

Query aggregated metrics for events, requests, and attempts — success counts, failure counts, response time, throughput, and SLA bands grouped by source, destination, or connection. Backs the dashboard analytics and downstream observability bridges.

- **Human URL:** [https://hookdeck.com/docs/metrics](https://hookdeck.com/docs/metrics)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Metrics
- Observability
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/metrics)
- [OpenAPI](openapi/hookdeck-metrics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hookdeck Integrations API

Configure platform integrations that adapt Hookdeck behavior for specific source platforms — including signature verification, header normalization, allowed event types, and platform-aware retries (e.g., Stripe, GitHub, Twilio, Shopify, Linear).

- **Human URL:** [https://hookdeck.com/docs/integrations](https://hookdeck.com/docs/integrations)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Integrations
- Webhooks
- Event Gateways

#### Properties

- [Documentation](https://hookdeck.com/docs/integrations)
- [OpenAPI](openapi/hookdeck-integrations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-integrations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-integrations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hookdeck Notifications API

Manage how your team is notified when issues occur — channel routing, mute windows, per-team subscriptions, and the templates rendered to Slack, Email, Microsoft Teams, and Discord.

- **Human URL:** [https://hookdeck.com/docs/notifications](https://hookdeck.com/docs/notifications)
- **Base URL:** `https://api.hookdeck.com/2025-07-01`

#### Tags

- Notifications
- Observability

#### Properties

- [Documentation](https://hookdeck.com/docs/notifications)
- [OpenAPI](openapi/hookdeck-notifications-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hookdeck-notifications-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hookdeck-notifications-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Documentation](https://hookdeck.com/docs)
- [API Reference](https://hookdeck.com/docs/api)
- [OpenAPI](https://api.hookdeck.com/2025-07-01/openapi) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Getting Started](https://hookdeck.com/docs/hookdeck-basics)
- [Authentication](https://hookdeck.com/docs/authentication)
- [Pricing](https://hookdeck.com/pricing)
- [Plans](plans/hookdeck-plans-pricing.yml)
- [Rate Limits](rate-limits/hookdeck-rate-limits.yml)
- [Fin Ops](finops/hookdeck-finops.yml)
- [JSON-LD](json-ld/hookdeck-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Blog](https://hookdeck.com/blog)
- [C L I](https://hookdeck.com/docs/cli)
- [C L I](https://github.com/hookdeck/hookdeck-cli)
- [SDK](https://github.com/hookdeck/hookdeck-typescript-sdk)
- [SDK](https://github.com/hookdeck/hookdeck-go-sdk)
- [SDK](https://github.com/hookdeck/hookdeck-python-sdk)
- [SDK](https://github.com/hookdeck/hookdeck-dotnet-sdk)
- [SDK](https://www.npmjs.com/package/@hookdeck/sdk)
- [Terraform Provider](https://registry.terraform.io/providers/hookdeck/hookdeck/latest/docs)
- [GitHub Organization](https://github.com/hookdeck)
- [GitHub Repository](https://github.com/hookdeck/hookdeck-api-schema)
- [GitHub Repository](https://github.com/hookdeck/outpost)
- [Open Source](https://hookdeck.com/outpost)
- [Agent Skill](https://github.com/hookdeck/webhook-skills)
- [Quickstart](https://hookdeck.com/docs/use-cases/receive-webhooks/quickstart)
- [Documentation](https://hookdeck.com/docs/use-cases/send-webhooks)
- [Documentation](https://hookdeck.com/event-gateway)
- [Documentation](https://hookdeck.com/outpost)
- [Changelog](https://hookdeck.com/changelog)
- [Status Page](https://status.hookdeck.com/)
- [Sign Up](https://dashboard.hookdeck.com/signup)
- [Login](https://dashboard.hookdeck.com/signin)
- [Contact](https://hookdeck.com/contact)
- [About](https://hookdeck.com/company)
- [Customers](https://hookdeck.com/customers)
- [Careers](https://hookdeck.com/careers)
- [Terms of Service](https://hookdeck.com/terms)
- [Privacy Policy](https://hookdeck.com/privacy)
- [Security](https://trust.hookdeck.com)
- [Data Processing Addendum](https://hookdeck.com/dpa)
- [X (Twitter)](https://x.com/Hookdeck)
- [LinkedIn](https://www.linkedin.com/company/hookdeck)
- [Slack](https://join.slack.com/t/hookdeckdevelopers/shared_invite/zt-yw7hlyzp-EQuO3QvdiBlH9Tz2KZg5MQ)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
