# Hookdeck (hookdeck)

Hookdeck is a Toronto-based webhook and event-infrastructure platform. The Hookdeck Event Gateway sits between webhook senders and your services to receive, verify, queue, retry, transform, filter, route, and observe events reliably at scale. Hookdeck exposes a fully versioned REST Admin API (`api.hookdeck.com/2025-07-01`), a CLI for local development, language SDKs (TypeScript, Go, Python, .NET), a Terraform provider, and the open-source Outpost project for self-hostable outbound webhook delivery.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/hookdeck/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Webhooks, Event Gateways, Gateways, Events, Event Infrastructure, Event-Driven, Messaging, Queues, Retries, Transformations, Observability

## Timestamps

- **Created:** 2025-08-19
- **Modified:** 2026-05-25

## At a Glance

| Capability | Notes |
|---|---|
| Inbound gateway | HTTP sources with platform-aware signature verification (Stripe, GitHub, Twilio, Shopify, Linear, and more) |
| Outbound delivery | HTTP endpoints, AWS SQS, Azure Service Bus, GCP Pub/Sub, Kafka, RabbitMQ, MongoDB, Hookdeck-as-destination |
| Reliability | Persistent queue, retries with backoff, dead-letter, bulk retry, bulk cancel |
| Transforms | Sandboxed JavaScript transformations with a sandboxed test runner |
| Routing | Connections from Source → Destination with filters, delays, alerts, and per-rule transforms |
| Observability | Aggregated metrics, full event/request/attempt history, Issue Triggers, Slack/Email/Teams/Discord/BetterUptime channels |
| API versioning | Date-based segment in base URL (e.g., `2025-07-01`) |
| Self-host | [Outpost](https://hookdeck.com/outpost) for outbound webhook delivery (open source) |

## APIs

### Hookdeck Connections API
Create, update, list, archive, pause, and unpause connections. A connection routes events from a Source to a Destination and may carry rules (retry, alert, transform, filter, delay) that determine how the gateway processes events along that path.

**Human URL:** [https://hookdeck.com/docs/api](https://hookdeck.com/docs/api)

- [Documentation](https://hookdeck.com/docs/api)
- [OpenAPI](openapi/hookdeck-connections-api-openapi.yml)
- [JSON Schema — Connection](json-schema/hookdeck-connection-schema.json)
- [Naftiko Capability — Connections](capabilities/hookdeck-connections.yaml)
- [Naftiko Capability — Connections topology](capabilities/hookdeck-connections-topology.yaml)

### Hookdeck Sources API
Manage sources — the upstream endpoints (webhook senders or push channels) that ingest events into Hookdeck. Sources support platform-specific verification, allowed HTTP methods, allowed content types, allowed IPs, and a configurable custom response returned to the caller.

**Human URL:** [https://hookdeck.com/docs/sources](https://hookdeck.com/docs/sources)

- [OpenAPI](openapi/hookdeck-sources-api-openapi.yml)
- [JSON Schema — Source](json-schema/hookdeck-source-schema.json)
- [Naftiko Capability — Sources](capabilities/hookdeck-sources.yaml)
- [Naftiko Capability — Sources discovery](capabilities/hookdeck-sources-discovery.yaml)

### Hookdeck Destinations API
Manage destinations — the downstream targets where Hookdeck delivers events. Supports HTTP endpoints, AWS SQS, Azure Service Bus, GCP Pub/Sub, Kafka, RabbitMQ, MongoDB, and more, with configurable auth methods, rate limits, path forwarding, archival, and pause/disable controls.

**Human URL:** [https://hookdeck.com/docs/destinations](https://hookdeck.com/docs/destinations)

- [OpenAPI](openapi/hookdeck-destinations-api-openapi.yml)
- [JSON Schema — Destination](json-schema/hookdeck-destination-schema.json)
- [Naftiko Capability — Destinations](capabilities/hookdeck-destinations.yaml)
- [Naftiko Capability — Destinations registry](capabilities/hookdeck-destinations-registry.yaml)
- [Naftiko Capability — Spec-driven destination](capabilities/hookdeck-spec-driven-destination.yaml)

### Hookdeck Events API
List, retrieve, retry, mute, and inspect events and their delivery attempts. An event is any request Hookdeck received from a source; an attempt is each delivery try against a destination, including status, response body, response time, and error code.

**Human URL:** [https://hookdeck.com/docs/events](https://hookdeck.com/docs/events)

- [OpenAPI](openapi/hookdeck-events-api-openapi.yml)
- [JSON Schema — Event](json-schema/hookdeck-event-schema.json)
- [JSON Schema — Attempt](json-schema/hookdeck-attempt-schema.json)
- [Naftiko Capability — Events](capabilities/hookdeck-events.yaml)
- [Naftiko Capability — Events replay](capabilities/hookdeck-events-replay.yaml)
- [Naftiko Capability — Attempts](capabilities/hookdeck-attempts.yaml)

### Hookdeck Requests API
List and inspect raw requests received by Hookdeck. A request precedes events and is what gets accepted at the gateway boundary before verification, fan-out, transformation, and routing produce one or more downstream events.

**Human URL:** [https://hookdeck.com/docs/requests](https://hookdeck.com/docs/requests)

- [OpenAPI](openapi/hookdeck-requests-api-openapi.yml)
- [JSON Schema — Request](json-schema/hookdeck-request-schema.json)
- [Naftiko Capability — Requests](capabilities/hookdeck-requests.yaml)

### Hookdeck Transformations API
Manage transformations — sandboxed JavaScript executed against events to mutate headers, body, path, or query string before delivery. Includes a sandboxed run endpoint for testing transformation code against sample event payloads.

**Human URL:** [https://hookdeck.com/docs/transformations](https://hookdeck.com/docs/transformations)

- [OpenAPI](openapi/hookdeck-transformations-api-openapi.yml)
- [JSON Schema — Transformation](json-schema/hookdeck-transformation-schema.json)
- [Naftiko Capability — Transformations](capabilities/hookdeck-transformations.yaml)
- [Naftiko Capability — Transformations author](capabilities/hookdeck-transformations-author.yaml)

### Hookdeck Bookmarks API
Save bookmarked events for quick replay and one-click testing during development. Bookmarks let your team capture canonical event payloads and trigger them on demand into any destination.

**Human URL:** [https://hookdeck.com/docs/bookmarks](https://hookdeck.com/docs/bookmarks)

- [OpenAPI](openapi/hookdeck-bookmarks-api-openapi.yml)
- [Naftiko Capability — Bookmarks](capabilities/hookdeck-bookmarks.yaml)
- [Naftiko Capability — Bookmarks snapshot](capabilities/hookdeck-bookmarks-snapshot.yaml)

### Hookdeck Bulk Operations API
Plan, schedule, and cancel bulk operations that retry or cancel many events, requests, or ignored events at once. Each bulk operation reports per-batch counts, total scope, and live progress, and can be cancelled mid-run.

**Human URL:** [https://hookdeck.com/docs/bulk-retries](https://hookdeck.com/docs/bulk-retries)

- [OpenAPI](openapi/hookdeck-bulk-operations-api-openapi.yml)
- [Naftiko Capability — Bulk retry events](capabilities/hookdeck-bulk-retry-events.yaml)
- [Naftiko Capability — Bulk retry ignored events](capabilities/hookdeck-bulk-retry-ignored-events.yaml)
- [Naftiko Capability — Bulk retry requests](capabilities/hookdeck-bulk-retry-requests.yaml)
- [Naftiko Capability — Bulk cancel events](capabilities/hookdeck-bulk-cancel-events.yaml)
- [Naftiko Capability — Bulk retry orchestrator](capabilities/hookdeck-bulk-retry-orchestrator.yaml)

### Hookdeck Issues API
Track issues that occur on events, requests, and backpressure, and manage the triggers (rules) that open and route issues to Slack, Email, Microsoft Teams, Discord, BetterUptime, and other channels.

**Human URL:** [https://hookdeck.com/docs/issues](https://hookdeck.com/docs/issues)

- [OpenAPI](openapi/hookdeck-issues-api-openapi.yml)
- [JSON Schema — Issue](json-schema/hookdeck-issue-schema.json)
- [Naftiko Capability — Issues](capabilities/hookdeck-issues.yaml)
- [Naftiko Capability — Issue triggers](capabilities/hookdeck-issue-triggers.yaml)
- [Naftiko Capability — Issues triage](capabilities/hookdeck-issues-triage.yaml)
- [Naftiko Capability — Issue trigger author](capabilities/hookdeck-issue-trigger-author.yaml)

### Hookdeck Metrics API
Query aggregated metrics for events, requests, and attempts — success counts, failure counts, response time, throughput, and SLA bands grouped by source, destination, or connection. Backs the dashboard analytics and downstream observability bridges.

**Human URL:** [https://hookdeck.com/docs/metrics](https://hookdeck.com/docs/metrics)

- [OpenAPI](openapi/hookdeck-metrics-api-openapi.yml)
- [Naftiko Capability — Metrics](capabilities/hookdeck-metrics.yaml)
- [Naftiko Capability — Metrics bridge](capabilities/hookdeck-metrics-bridge.yaml)

### Hookdeck Integrations API
Configure platform integrations that adapt Hookdeck behavior for specific source platforms — including signature verification, header normalization, allowed event types, and platform-aware retries (e.g., Stripe, GitHub, Twilio, Shopify, Linear).

**Human URL:** [https://hookdeck.com/docs/integrations](https://hookdeck.com/docs/integrations)

- [OpenAPI](openapi/hookdeck-integrations-api-openapi.yml)
- [Naftiko Capability — Integrations](capabilities/hookdeck-integrations.yaml)
- [Naftiko Capability — Integrations catalog](capabilities/hookdeck-integrations-catalog.yaml)

### Hookdeck Notifications API
Manage how your team is notified when issues occur — channel routing, mute windows, per-team subscriptions, and the templates rendered to Slack, Email, Microsoft Teams, and Discord.

**Human URL:** [https://hookdeck.com/docs/notifications](https://hookdeck.com/docs/notifications)

- [OpenAPI](openapi/hookdeck-notifications-api-openapi.yml)
- [Naftiko Capability — Notifications](capabilities/hookdeck-notifications.yaml)

## Common Properties

- [Documentation](https://hookdeck.com/docs)
- [API Reference](https://hookdeck.com/docs/api)
- [OpenAPI — live](https://api.hookdeck.com/2025-07-01/openapi)
- [Getting Started](https://hookdeck.com/docs/hookdeck-basics)
- [Authentication](https://hookdeck.com/docs/authentication)
- [Pricing](https://hookdeck.com/pricing)
- [Plans / Pricing](plans/hookdeck-plans-pricing.yml)
- [Rate Limits](rate-limits/hookdeck-rate-limits.yml)
- [FinOps Definition](finops/hookdeck-finops.yml)
- [JSON-LD Context](json-ld/hookdeck-context.jsonld)
- [Blog](https://hookdeck.com/blog)
- [Changelog](https://hookdeck.com/changelog)
- [CLI — docs](https://hookdeck.com/docs/cli)
- [CLI — repo](https://github.com/hookdeck/hookdeck-cli)
- [SDK — TypeScript](https://github.com/hookdeck/hookdeck-typescript-sdk)
- [SDK — Go](https://github.com/hookdeck/hookdeck-go-sdk)
- [SDK — Python](https://github.com/hookdeck/hookdeck-python-sdk)
- [SDK — .NET](https://github.com/hookdeck/hookdeck-dotnet-sdk)
- [SDK — npm](https://www.npmjs.com/package/@hookdeck/sdk)
- [Terraform Provider](https://registry.terraform.io/providers/hookdeck/hookdeck/latest/docs)
- [GitHub Organization](https://github.com/hookdeck)
- [GitHub Repository — API Schema](https://github.com/hookdeck/hookdeck-api-schema)
- [GitHub Repository — Outpost (OSS)](https://github.com/hookdeck/outpost)
- [Outpost (self-host)](https://hookdeck.com/outpost)
- [Agent Skills](https://github.com/hookdeck/webhook-skills)
- [Quickstart](https://hookdeck.com/docs/use-cases/receive-webhooks/quickstart)
- [Send Webhooks](https://hookdeck.com/docs/use-cases/send-webhooks)
- [Event Gateway](https://hookdeck.com/event-gateway)
- [Status Page](https://status.hookdeck.com/)
- [Sign Up](https://dashboard.hookdeck.com/signup)
- [Login](https://dashboard.hookdeck.com/signin)
- [Contact](https://hookdeck.com/contact)
- [About](https://hookdeck.com/company)
- [Customers](https://hookdeck.com/customers)
- [Careers](https://hookdeck.com/careers)
- [Terms of Service](https://hookdeck.com/terms)
- [Privacy Policy](https://hookdeck.com/privacy)
- [Security (Trust Center)](https://trust.hookdeck.com)
- [Data Processing Addendum](https://hookdeck.com/dpa)
- [X / Twitter](https://x.com/Hookdeck)
- [LinkedIn](https://www.linkedin.com/company/hookdeck)
- [Slack Community](https://join.slack.com/t/hookdeckdevelopers/shared_invite/zt-yw7hlyzp-EQuO3QvdiBlH9Tz2KZg5MQ)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Hookdeck Connections API](openapi/hookdeck-connections-api-openapi.yml)
- [Hookdeck Sources API](openapi/hookdeck-sources-api-openapi.yml)
- [Hookdeck Destinations API](openapi/hookdeck-destinations-api-openapi.yml)
- [Hookdeck Events API](openapi/hookdeck-events-api-openapi.yml)
- [Hookdeck Requests API](openapi/hookdeck-requests-api-openapi.yml)
- [Hookdeck Transformations API](openapi/hookdeck-transformations-api-openapi.yml)
- [Hookdeck Bookmarks API](openapi/hookdeck-bookmarks-api-openapi.yml)
- [Hookdeck Bulk Operations API](openapi/hookdeck-bulk-operations-api-openapi.yml)
- [Hookdeck Issues API](openapi/hookdeck-issues-api-openapi.yml)
- [Hookdeck Metrics API](openapi/hookdeck-metrics-api-openapi.yml)
- [Hookdeck Integrations API](openapi/hookdeck-integrations-api-openapi.yml)
- [Hookdeck Notifications API](openapi/hookdeck-notifications-api-openapi.yml)

### JSON Schema

- [Connection](json-schema/hookdeck-connection-schema.json)
- [Source](json-schema/hookdeck-source-schema.json)
- [Destination](json-schema/hookdeck-destination-schema.json)
- [Event](json-schema/hookdeck-event-schema.json)
- [Attempt](json-schema/hookdeck-attempt-schema.json)
- [Request](json-schema/hookdeck-request-schema.json)
- [Transformation](json-schema/hookdeck-transformation-schema.json)
- [Issue](json-schema/hookdeck-issue-schema.json)

### JSON-LD

- [Hookdeck Context](json-ld/hookdeck-context.jsonld)

### Capabilities (Naftiko)

- [Connections](capabilities/hookdeck-connections.yaml) — [topology](capabilities/hookdeck-connections-topology.yaml)
- [Sources](capabilities/hookdeck-sources.yaml) — [discovery](capabilities/hookdeck-sources-discovery.yaml)
- [Destinations](capabilities/hookdeck-destinations.yaml) — [registry](capabilities/hookdeck-destinations-registry.yaml) — [spec-driven](capabilities/hookdeck-spec-driven-destination.yaml)
- [Events](capabilities/hookdeck-events.yaml) — [replay](capabilities/hookdeck-events-replay.yaml)
- [Attempts](capabilities/hookdeck-attempts.yaml)
- [Requests](capabilities/hookdeck-requests.yaml)
- [Transformations](capabilities/hookdeck-transformations.yaml) — [author](capabilities/hookdeck-transformations-author.yaml)
- [Bookmarks](capabilities/hookdeck-bookmarks.yaml) — [snapshot](capabilities/hookdeck-bookmarks-snapshot.yaml)
- [Bulk retry events](capabilities/hookdeck-bulk-retry-events.yaml) — [ignored](capabilities/hookdeck-bulk-retry-ignored-events.yaml) — [requests](capabilities/hookdeck-bulk-retry-requests.yaml) — [cancel](capabilities/hookdeck-bulk-cancel-events.yaml) — [orchestrator](capabilities/hookdeck-bulk-retry-orchestrator.yaml)
- [Issues](capabilities/hookdeck-issues.yaml) — [triggers](capabilities/hookdeck-issue-triggers.yaml) — [triage](capabilities/hookdeck-issues-triage.yaml) — [trigger author](capabilities/hookdeck-issue-trigger-author.yaml)
- [Metrics](capabilities/hookdeck-metrics.yaml) — [bridge](capabilities/hookdeck-metrics-bridge.yaml)
- [Integrations](capabilities/hookdeck-integrations.yaml) — [catalog](capabilities/hookdeck-integrations-catalog.yaml)
- [Notifications](capabilities/hookdeck-notifications.yaml)

### Naftiko Integrations

Cross-provider integrations published under [integrations/](integrations/):

- [hookdeck × Anthropic](integrations/hookdeck-anthropic.yaml)
- [hookdeck × AWS SQS](integrations/hookdeck-aws-sqs.yaml)
- [hookdeck × Datadog](integrations/hookdeck-datadog.yaml)
- [hookdeck × GitHub](integrations/hookdeck-github.yaml)
- [hookdeck × Kafka](integrations/hookdeck-kafka.yaml)
- [hookdeck × Linear](integrations/hookdeck-linear.yaml)
- [hookdeck × PagerDuty](integrations/hookdeck-pagerduty.yaml)
- [hookdeck × SendGrid](integrations/hookdeck-sendgrid.yaml)
- [hookdeck × Shopify](integrations/hookdeck-shopify.yaml)
- [hookdeck × Slack](integrations/hookdeck-slack.yaml)
- [hookdeck × Stripe](integrations/hookdeck-stripe.yaml)
- [hookdeck × Twilio](integrations/hookdeck-twilio.yaml)

### Commercial artifacts

- [Plans / Pricing](plans/hookdeck-plans-pricing.yml)
- [Rate Limits](rate-limits/hookdeck-rate-limits.yml)
- [FinOps Definition](finops/hookdeck-finops.yml)

### Blogs

Hookdeck news and engineering posts mirrored under [blogs/](blogs/).

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
