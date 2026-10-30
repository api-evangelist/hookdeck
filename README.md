# Hookdeck

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Hookdeck is a Toronto-based webhook and event-infrastructure platform. The Hookdeck Event Gateway sits between webhook senders and your services to receive, verify, queue, retry, transform, filter, route, and observe events reliably at scale. Hookdeck exposes a fully versioned REST Admin API, a CLI for local development, language SDKs (TypeScript, Go, Python, .NET), a Terraform provider, and the open-source Outpost project for self-hostable outbound webhook delivery.

**Areas:** Webhook · Event Gateways · Gateways · Event · Event Infrastructure · Event-Driven · Messaging · Queues · Retries · Transformation · Observability

## Hookdeck on APIs.io

Everything profiled for Hookdeck is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/hookdeck/](https://apis.io/providers/hookdeck/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [Hookdeck Connections API](https://apis.io/apis/hookdeck/hookdeck-connections-api/) — Create, update, list, archive, pause, and unpause connections. A connection routes events from a Source to a Destination and may carry rules (retry, alert,…
- [Hookdeck Sources API](https://apis.io/apis/hookdeck/hookdeck-sources-api/) — Manage sources — the upstream endpoints (webhook senders or push channels) that ingest events into Hookdeck. Sources support platform-specific verification…
- [Hookdeck Destinations API](https://apis.io/apis/hookdeck/hookdeck-destinations-api/) — Manage destinations — the downstream targets (HTTP endpoints, AWS SQS, Azure Service Bus, GCP Pub/Sub, Kafka, RabbitMQ, MongoDB, and more) where Hookdeck…
- [Hookdeck Events API](https://apis.io/apis/hookdeck/hookdeck-events-api/) — List, retrieve, retry, mute, and inspect events and their delivery attempts. An event is any request Hookdeck received from a source; an attempt is each…
- [Hookdeck Requests API](https://apis.io/apis/hookdeck/hookdeck-requests-api/) — List and inspect raw requests received by Hookdeck. A request precedes events and is what gets accepted at the gateway boundary before verification,…
- [Hookdeck Transformations API](https://apis.io/apis/hookdeck/hookdeck-transformations-api/) — Manage transformations — sandboxed JavaScript executed against events to mutate headers, body, path, or query string before delivery. Also includes a…
- [Hookdeck Bookmarks API](https://apis.io/apis/hookdeck/hookdeck-bookmarks-api/) — Save bookmarked events for quick replay and one-click testing during development. Bookmarks let your team capture canonical event payloads and trigger them…
- [Hookdeck Issues API](https://apis.io/apis/hookdeck/hookdeck-issues-api/) — Track issues that occur on events, requests, and backpressure, and manage the triggers (rules) that open and route issues to Slack, Email, Microsoft Teams,…
- [Hookdeck Metrics API](https://apis.io/apis/hookdeck/hookdeck-metrics-api/) — Query aggregated metrics for events, requests, and attempts — success counts, failure counts, response time, throughput, and SLA bands grouped by source,…
- [Hookdeck Integrations API](https://apis.io/apis/hookdeck/hookdeck-integrations-api/) — Configure platform integrations that adapt Hookdeck behavior for specific source platforms — including signature verification, header normalization, allowed…
- [Hookdeck Notifications API](https://apis.io/apis/hookdeck/hookdeck-notifications-api/) — Manage how your team is notified when issues occur — channel routing, mute windows, per-team subscriptions, and the templates rendered to Slack, Email,…
- [Hookdeck Attempts API](https://apis.io/apis/hookdeck/hookdeck-attempts-api/) — An attempt is any request that Hookdeck makes on behalf of an event.
- [Hookdeck Bulk cancel events API](https://apis.io/apis/hookdeck/hookdeck-bulk-cancel-events-api/) — Bulk cancel operations allow you to cancel multiple pending events at once.
- [Hookdeck Bulk retry events API](https://apis.io/apis/hookdeck/hookdeck-bulk-retry-events-api/) — Bulk retry operations allow you to retry many events at once. A bulk retry is first estimated, then created, then processed asynchronously.
- [Hookdeck Bulk retry ignored events API](https://apis.io/apis/hookdeck/hookdeck-bulk-retry-ignored-events-api/) — Bulk retry ignored events allow you to retry many events that were previously ignored (for instance due to filter rules) at once.
- [Hookdeck Bulk retry requests API](https://apis.io/apis/hookdeck/hookdeck-bulk-retry-requests-api/) — Bulk retry requests allow you to re-ingest many previously received requests at once.
- [Hookdeck Issue Triggers API](https://apis.io/apis/hookdeck/hookdeck-issue-triggers-api/) — Issue Triggers lets you setup rules that trigger issues when certain conditions are met.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (14)

Multi-step workflows that chain operations into a business task.

- [Hookdeck Attach an Integration to a New Source](https://apis.io/arazzos/hookdeck/hookdeck-attach-integration-to-source-workflow/)
- [Hookdeck Author and Verify a Transformation](https://apis.io/arazzos/hookdeck/hookdeck-author-transformation-workflow/)
- [Hookdeck Bookmark and Replay an Event](https://apis.io/arazzos/hookdeck/hookdeck-bookmark-and-replay-event-workflow/)
- [Hookdeck Bulk Retry Failed Events](https://apis.io/arazzos/hookdeck/hookdeck-bulk-retry-failed-events-workflow/)
- [Hookdeck Cancel a Pending Event](https://apis.io/arazzos/hookdeck/hookdeck-cancel-pending-event-workflow/)
- [Hookdeck Decommission a Source](https://apis.io/arazzos/hookdeck/hookdeck-decommission-source-workflow/)
- [Hookdeck Create an Inline Connection](https://apis.io/arazzos/hookdeck/hookdeck-inline-connection-workflow/)
- [Hookdeck Investigate Event Delivery Attempts](https://apis.io/arazzos/hookdeck/hookdeck-investigate-event-attempts-workflow/)
- [Hookdeck Pause and Resume a Connection](https://apis.io/arazzos/hookdeck/hookdeck-pause-resume-connection-workflow/)
- [Hookdeck Provision a Connection](https://apis.io/arazzos/hookdeck/hookdeck-provision-connection-workflow/)
- [Hookdeck Replay an Inbound Request](https://apis.io/arazzos/hookdeck/hookdeck-replay-request-workflow/)
- [Hookdeck Retry a Failed Event](https://apis.io/arazzos/hookdeck/hookdeck-retry-failed-event-workflow/)
- [Hookdeck Test Then Update a Transformation](https://apis.io/arazzos/hookdeck/hookdeck-update-transformation-workflow/)
- [Hookdeck Upsert a Connection by Name](https://apis.io/arazzos/hookdeck/hookdeck-upsert-connection-workflow/)

#### Agent skills (39)

Agent skills built on the API.

- [chargebee-webhooks](https://apis.io/agent-skills/hookdeck/chargebee-webhooks/)
- [claude-managed-agents-webhooks](https://apis.io/agent-skills/hookdeck/claude-managed-agents-webhooks/)
- [clerk-webhooks](https://apis.io/agent-skills/hookdeck/clerk-webhooks/)
- [cursor-webhooks](https://apis.io/agent-skills/hookdeck/cursor-webhooks/)
- [deepgram-webhooks](https://apis.io/agent-skills/hookdeck/deepgram-webhooks/)
- [discord-webhooks](https://apis.io/agent-skills/hookdeck/discord-webhooks/)
- [elevenlabs-webhooks](https://apis.io/agent-skills/hookdeck/elevenlabs-webhooks/)
- [fusionauth-webhooks](https://apis.io/agent-skills/hookdeck/fusionauth-webhooks/)
- [gemini-webhooks](https://apis.io/agent-skills/hookdeck/gemini-webhooks/)
- [github-webhooks](https://apis.io/agent-skills/hookdeck/github-webhooks/)
- [gitlab-webhooks](https://apis.io/agent-skills/hookdeck/gitlab-webhooks/)
- [hookdeck-event-gateway](https://apis.io/agent-skills/hookdeck/hookdeck-event-gateway/)
- [hookdeck-event-gateway-webhooks](https://apis.io/agent-skills/hookdeck/hookdeck-event-gateway-webhooks/)
- [hubspot-webhooks](https://apis.io/agent-skills/hookdeck/hubspot-webhooks/)
- [huggingface-webhooks](https://apis.io/agent-skills/hookdeck/huggingface-webhooks/)
- [intercom-webhooks](https://apis.io/agent-skills/hookdeck/intercom-webhooks/)
- [knock-webhooks](https://apis.io/agent-skills/hookdeck/knock-webhooks/)
- [linear-webhooks](https://apis.io/agent-skills/hookdeck/linear-webhooks/)
- [mailgun-webhooks](https://apis.io/agent-skills/hookdeck/mailgun-webhooks/)
- [notion-webhooks](https://apis.io/agent-skills/hookdeck/notion-webhooks/)
- [openai-webhooks](https://apis.io/agent-skills/hookdeck/openai-webhooks/)
- [openclaw-webhooks](https://apis.io/agent-skills/hookdeck/openclaw-webhooks/)
- [orb-webhooks](https://apis.io/agent-skills/hookdeck/orb-webhooks/)
- [outpost](https://apis.io/agent-skills/hookdeck/outpost/)
- [paddle-webhooks](https://apis.io/agent-skills/hookdeck/paddle-webhooks/)
- …and 14 more published on APIs.io

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Hookdeck Agentic Access](https://apis.io/agentic-access/hookdeck/hookdeck-agentic-access/)

#### JSON Schema (8)

The data models the API reads and writes.

- [Hookdeck EventAttempt](https://apis.io/schemas/hookdeck/hookdeck-attempt/)
- [Hookdeck Connection](https://apis.io/schemas/hookdeck/hookdeck-connection/)
- [Hookdeck Destination](https://apis.io/schemas/hookdeck/hookdeck-destination/)
- [Hookdeck Event](https://apis.io/schemas/hookdeck/hookdeck-event/)
- [Hookdeck Issue](https://apis.io/schemas/hookdeck/hookdeck-issue/)
- [Hookdeck Request](https://apis.io/schemas/hookdeck/hookdeck-request/)
- [Hookdeck Source](https://apis.io/schemas/hookdeck/hookdeck-source/)
- [Hookdeck Transformation](https://apis.io/schemas/hookdeck/hookdeck-transformation/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Hookdeck Context](https://apis.io/jsonld/hookdeck/hookdeck-context/)

#### Collections (30)

Postman and Open Collection request collections.

- [Hookdeck Bookmarks Attempts API](https://apis.io/collections/hookdeck/open-hookdeck-attempts-api/)
- [Hookdeck Attempts Bookmarks API](https://apis.io/collections/hookdeck/open-hookdeck-bookmarks-api/)
- [Hookdeck Bookmarks Attempts Bulk cancel events API](https://apis.io/collections/hookdeck/open-hookdeck-bulk-cancel-events-api/)
- [Hookdeck Bulk Operations API](https://apis.io/collections/hookdeck/open-hookdeck-bulk-operations-api/)
- [Hookdeck Bookmarks Attempts Bulk retry events API](https://apis.io/collections/hookdeck/open-hookdeck-bulk-retry-events-api/)
- [Hookdeck Bookmarks Attempts Bulk retry ignored events API](https://apis.io/collections/hookdeck/open-hookdeck-bulk-retry-ignored-events-api/)
- [Hookdeck Bookmarks Attempts Bulk retry requests API](https://apis.io/collections/hookdeck/open-hookdeck-bulk-retry-requests-api/)
- [Hookdeck Bookmarks Attempts Connections API](https://apis.io/collections/hookdeck/open-hookdeck-connections-api/)
- [Hookdeck Bookmarks Attempts Destinations API](https://apis.io/collections/hookdeck/open-hookdeck-destinations-api/)
- [Hookdeck Bookmarks Attempts Events API](https://apis.io/collections/hookdeck/open-hookdeck-events-api/)
- [Hookdeck Bookmarks Attempts Integrations API](https://apis.io/collections/hookdeck/open-hookdeck-integrations-api/)
- [Hookdeck Bookmarks Attempts Issue Triggers API](https://apis.io/collections/hookdeck/open-hookdeck-issue-triggers-api/)
- [Hookdeck Bookmarks Attempts Issues API](https://apis.io/collections/hookdeck/open-hookdeck-issues-api/)
- [Hookdeck Bookmarks Attempts Metrics API](https://apis.io/collections/hookdeck/open-hookdeck-metrics-api/)
- [Hookdeck Bookmarks Attempts Notifications API](https://apis.io/collections/hookdeck/open-hookdeck-notifications-api/)
- [Hookdeck Bookmarks Attempts Requests API](https://apis.io/collections/hookdeck/open-hookdeck-requests-api/)
- [Hookdeck Bookmarks Attempts Sources API](https://apis.io/collections/hookdeck/open-hookdeck-sources-api/)
- [Hookdeck Bookmarks Attempts Transformations API](https://apis.io/collections/hookdeck/open-hookdeck-transformations-api/)
- [Hookdeck Bookmarks API](https://apis.io/collections/hookdeck/postman-hookdeck-bookmarks-api/)
- [Hookdeck Bulk Operations API](https://apis.io/collections/hookdeck/postman-hookdeck-bulk-operations-api/)
- [Hookdeck Connections API](https://apis.io/collections/hookdeck/postman-hookdeck-connections-api/)
- [Hookdeck Destinations API](https://apis.io/collections/hookdeck/postman-hookdeck-destinations-api/)
- [Hookdeck Events API](https://apis.io/collections/hookdeck/postman-hookdeck-events-api/)
- [Hookdeck Integrations API](https://apis.io/collections/hookdeck/postman-hookdeck-integrations-api/)
- [Hookdeck Issues API](https://apis.io/collections/hookdeck/postman-hookdeck-issues-api/)
- …and 5 more published on APIs.io

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Hookdeck — jsonschema rules](https://apis.io/rules/hookdeck/hookdeck-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Hookdeck Authentication](https://apis.io/security/hookdeck/hookdeck-authentication/)
- [Hookdeck Domain Security](https://apis.io/security/hookdeck/hookdeck-domain-security/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Hookdeck Plans Pricing](https://apis.io/plans/hookdeck/hookdeck-plans-pricing/)
- [Hookdeck Price Estimates](https://apis.io/plans/hookdeck/hookdeck-price-estimates/)

#### Rate limits (1)

Published request limits.

- [Hookdeck Rate Limits](https://apis.io/rate-limits/hookdeck/hookdeck-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Hookdeck Finops](https://apis.io/finops/hookdeck/hookdeck-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.hookdeck.com/)
- [Documentation](https://hookdeck.com/docs)
- [Getting started](https://hookdeck.com/docs/hookdeck-basics)
- [API reference](https://hookdeck.com/docs/api)
- [Pricing](https://hookdeck.com/pricing)
- [Changelog](https://hookdeck.com/changelog)
- [Blog](https://hookdeck.com/blog)
- [Security](https://trust.hookdeck.com)
- [Terms of service](https://hookdeck.com/terms)
- [Privacy policy](https://hookdeck.com/privacy)
- [GitHub](https://github.com/hookdeck)
- [Status](https://status.hookdeck.com/)

## API Evangelist rating

**Kin Score 59.4** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 68.4 |
| Contract governance | 9.8 |
| Operational transparency | 31.6 |
| Developer ergonomics | 79.0 |
| Access clarity | 69.7 |

**Agent readiness 31.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/hookdeck/](https://apis.io/providers/hookdeck/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Hookdeck: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/hookdeck/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
