# Documentation project instructions

## About this project

This is the Rightcharge developer documentation portal, built on [Mintlify](https://mintlify.com).

**Product:** Rightcharge — infrastructure that enables fleet platforms, CPMS providers, charger manufacturers, leasing companies, energy suppliers, vehicle OEMs and mobility providers to launch fleet home-charging products.

**Tagline:** "Integrate once. Deploy fleet home charging."

Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.

## Site structure

Two tabs:

- **Documentation** — Start Here, Platform, Solutions, Modules, Partner Blueprints, Guides
- **API Reference** — API Conventions, Core Resources, Webhooks, Errors and Lifecycle, Supported Integrations, Changelog

## Terminology

- **Company** — the fleet or business entity (top-level Rightcharge resource)
- **Driver** — an individual belonging to a company
- **Session** — a charging session recorded for a driver
- **Reimbursement** — the calculated amount owed to a driver or supplier for one or more sessions
- **Module** — an individual Rightcharge capability (e.g. Tariff Engine, Session Ingestion)
- **Solution** — an outcome a partner launches (e.g. Home Charging Reimbursement)
- **Blueprint** — an architectural reference showing how Rightcharge combines with a specific partner type
- Use "partner" not "customer" for organisations integrating Rightcharge
- Use "driver" not "user" or "end user" for the fleet employees charging at home
- Use "fleet operator" for the businesses whose employees are the drivers

## Style preferences

- British English throughout
- Active voice and second person ("you")
- Lead with outcomes, not implementation details
- One idea per sentence
- Title Case for navigation labels and headings
- Bold for UI element names and important terms
- Code formatting for field names, endpoint paths, header names and environment variables

## Accuracy rules

Do NOT invent:

- Endpoint paths or field names
- Authentication methods or scopes
- Webhook event names
- Status values or error codes
- Supported charger manufacturers, CPMS providers or energy suppliers
- Country or currency availability
- Base URLs or SDK names

When information is missing, use a clearly labelled `[PLACEHOLDER: what engineering or product must provide]`.

Distinguish clearly between: production, limited availability, planned functionality, and future concepts (Grid Flex, V2G).

## Content boundaries

Document for product managers, architects and developers integrating Rightcharge. Do not document internal Rightcharge infrastructure, deployment, or admin tooling.

## OpenAPI

When `openapi/rightcharge.yaml` is added and validates, add it to the API Reference tab using Mintlify's `openapi` property on the Core Resources group. Until then, the hand-written resource pages in `api-reference/` serve as provisional contract reference — clearly labelled as such.
