# ServiceTitan (servicetitan)

ServiceTitan is the operating system for the trades — all-in-one field service management software for residential and commercial contractors in HVAC, plumbing, electrical, roofing, garage door, pest control, refrigeration, fire & life safety, septic, landscape, and other service-based industries. The platform unifies CRM, dispatch, scheduling, job management, pricebook, mobile field execution, invoicing, payments, payroll, marketing attribution, memberships, service agreements, reporting, and Contact Center / Voice Agent capabilities behind a tenant-scoped V2 REST API surface accessed via OAuth 2.0 client credentials and a per-application App Key. ServiceTitan is the parent of FieldRoutes (pest), Aspire (landscape), and Convex (commercial sales), and ships Conduit as its integration platform.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/servicetitan/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Field Service Management, Trades, HVAC, Plumbing, Electrical, Construction, CRM, Dispatch, Accounting, Pricebook, Marketing, Memberships, Webhooks

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Authentication

OAuth 2.0 client-credentials plus a per-application App Key. Every request needs both an `Authorization: Bearer {token}` header and an `ST-App-Key: {app_key}` header, and the tenant ID is embedded in the URL path.

| Step | What | Where |
|---|---|---|
| 1 | Get Client ID and Client Secret | ServiceTitan tenant → Settings → Integrations → API Application Access |
| 2 | Create App and copy App Key | https://developer.servicetitan.io/ |
| 3 | Add tenant to your app, capture Tenant ID | Developer Portal app config |
| 4 | POST `grant_type=client_credentials` | Production: `https://auth.servicetitan.io/connect/token`<br/>Integration: `https://auth-integration.servicetitan.io/connect/token` |
| 5 | Call API | `https://api.servicetitan.io/{module}/v2/{tenant-id}/...` with `Authorization` + `ST-App-Key` |

## Environments

| | Production | Integration (Sandbox) |
|---|---|---|
| API base | `https://api.servicetitan.io/{module}/v2/{tenant-id}/` | `https://api-integration.servicetitan.io/{module}/v2/{tenant-id}/` |
| Auth | `https://auth.servicetitan.io/connect/token` | `https://auth-integration.servicetitan.io/connect/token` |
| App UI | `https://go.servicetitan.com/` | Cloned from production data for existing customers |

## Rate Limits

| Surface | Limit |
|---|---|
| All standard APIs | 60 requests/sec per (App Key, Tenant ID) pair |
| Reporting API | 1 of the same report per minute per tenant |

See `rate-limits/servicetitan-rate-limits.yml` for details.

## APIs

ServiceTitan exposes 24 tenant-scoped V2 modules. All paths follow the pattern `/{module}/v2/{tenant-id}/...`.

### ServiceTitan CRM API
Manage residential and commercial customer records, locations, contacts, leads, bookings, tags, and booking provider sessions. Primary entry point for customer-of-record data.
- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-crm-api-openapi.yml)
- [JSON Schema — Customer](json-schema/servicetitan-customer-schema.json)
- [JSON Schema — Location](json-schema/servicetitan-location-schema.json)
- [Naftiko Capability — Customers](capabilities/crm-customers.yaml)
- [Naftiko Capability — Locations](capabilities/crm-locations.yaml)
- [Naftiko Capability — Leads](capabilities/crm-leads.yaml)

### ServiceTitan Job Planning & Management API
Create, retrieve, update, hold, cancel, and reschedule jobs, projects, appointments, job types, call reasons, job cancel reasons, and job history. The operational core.
- [OpenAPI](openapi/servicetitan-jpm-api-openapi.yml)
- [JSON Schema — Job](json-schema/servicetitan-job-schema.json)
- [JSON Schema — Project](json-schema/servicetitan-project-schema.json)
- [JSON Schema — Appointment](json-schema/servicetitan-appointment-schema.json)
- [Naftiko Capability — Jobs](capabilities/jpm-jobs.yaml)
- [Naftiko Capability — Appointments](capabilities/jpm-appointments.yaml)
- [Naftiko Capability — Projects](capabilities/jpm-projects.yaml)

### ServiceTitan Dispatch API
Technician shifts, appointment assignments, capacity windows, business hours, zones, arrival windows, and GPS pings.
- [OpenAPI](openapi/servicetitan-dispatch-api-openapi.yml)
- [Naftiko Capability — Assignments](capabilities/dispatch-assignments.yaml)
- [Naftiko Capability — Capacity](capabilities/dispatch-capacity.yaml)

### ServiceTitan Accounting API
Invoices, items, payments, journal entries, tax zones, GL accounts. Integrates with QuickBooks, Sage Intacct, Acumatica.
- [OpenAPI](openapi/servicetitan-accounting-api-openapi.yml)
- [JSON Schema — Invoice](json-schema/servicetitan-invoice-schema.json)
- [JSON Schema — Payment](json-schema/servicetitan-payment-schema.json)
- [Naftiko Capability — Invoices](capabilities/accounting-invoices.yaml)
- [Naftiko Capability — Payments](capabilities/accounting-payments.yaml)
- [Naftiko Capability — Journal](capabilities/accounting-journal.yaml)

### ServiceTitan Pricebook API
CRUD over the pricebook — categories, services, materials, equipment, discounts/fees, images. Powers Pricebook Pro.
- [OpenAPI](openapi/servicetitan-pricebook-api-openapi.yml)
- [JSON Schema — Service](json-schema/servicetitan-service-schema.json)
- [JSON Schema — Material](json-schema/servicetitan-material-schema.json)
- [Naftiko Capability — Services](capabilities/pricebook-services.yaml)
- [Naftiko Capability — Materials](capabilities/pricebook-materials.yaml)
- [Naftiko Capability — Equipment](capabilities/pricebook-equipment.yaml)

### ServiceTitan Inventory API
Purchase orders, types, transfers, returns, adjustments, receipts, warehouses, trucks, vendors, inventory bills. Backed by the open-source `request-middleware-templates` Liquid framework.
- [OpenAPI](openapi/servicetitan-inventory-api-openapi.yml)
- [Naftiko Capability — Purchase Orders](capabilities/inventory-purchase-orders.yaml)
- [Naftiko Capability — Warehouses](capabilities/inventory-warehouses.yaml)

### ServiceTitan Equipment Systems API
Installed equipment records per customer location — make, model, serial, install date, warranty terms, attachments, and history. The asset-of-record API.
- [OpenAPI](openapi/servicetitan-equipment-systems-api-openapi.yml)
- [Naftiko Capability — Installed Equipment](capabilities/equipmentsystems-installed-equipment.yaml)

### ServiceTitan Settings API
Business units, employees, technicians, user roles, tag types, tenant-wide settings.
- [OpenAPI](openapi/servicetitan-settings-api-openapi.yml)
- [Naftiko Capability — Business Units](capabilities/settings-business-units.yaml)
- [Naftiko Capability — Technicians](capabilities/settings-technicians.yaml)
- [Naftiko Capability — Employees](capabilities/settings-employees.yaml)

### ServiceTitan Marketing API
Campaigns, categories, suppression lists, attribution. Underpins Marketing Pro email/SMS.
- [Naftiko Capability — Campaigns](capabilities/marketing-campaigns.yaml)

### ServiceTitan Marketing Reputation API
Aggregated customer reviews and reputation metrics across Google, Facebook, Yelp, BBB.
- [Naftiko Capability — Reviews](capabilities/marketingreputation-reviews.yaml)

### ServiceTitan Memberships API
Membership types, customer memberships, membership invoice templates, recurring service types and events.
- [Naftiko Capability — Memberships](capabilities/memberships-memberships.yaml)
- [Naftiko Capability — Recurring Services](capabilities/memberships-recurring-services.yaml)

### ServiceTitan Service Agreements API
Commercial service agreements — contract terms, billed locations, line items, renewal cadence.
- [Naftiko Capability — Agreements](capabilities/serviceagreements-agreements.yaml)

### ServiceTitan Forms API
Form definitions and field-completed submissions — photos, signatures, checkboxes, free-text. Compliance, safety, and post-service surveys.
- [Naftiko Capability — Submissions](capabilities/forms-submissions.yaml)

### ServiceTitan Payroll API
Payroll adjustments, gross-pay items, job splits, timesheet codes, activity codes, non-job timesheets, payroll settings.
- [Naftiko Capability — Timesheets](capabilities/payroll-timesheets.yaml)
- [Naftiko Capability — Adjustments](capabilities/payroll-adjustments.yaml)

### ServiceTitan Timesheets API
Timesheet entries, activity codes, shift segments. Feeds Payroll.
- [Naftiko Capability — Entries](capabilities/timesheets-entries.yaml)

### ServiceTitan Reporting API
Run published custom reports with parameters; retrieve dynamic value sets. **1 same-report call per minute per tenant.**
- [Naftiko Capability — Reports](capabilities/reporting-reports.yaml)

### ServiceTitan Sales & Estimates API
Create and retrieve estimates and proposal templates. Backs Proposal Builder.
- [Naftiko Capability — Estimates](capabilities/sales-estimates.yaml)

### ServiceTitan Customer Interactions API
Post-service technician ratings and customer feedback.
- [Naftiko Capability — Ratings](capabilities/customerinteractions-ratings.yaml)

### ServiceTitan Task Management API
Internal tasks, statuses, sub-tasks. Office-to-field handoffs and escalations.
- [Naftiko Capability — Tasks](capabilities/taskmanagement-tasks.yaml)

### ServiceTitan Telecom API
Call records, recordings, analytics, call reasons. Powers Contact Center Pro and Voice Agent.
- [Naftiko Capability — Calls](capabilities/telecom-calls.yaml)

### ServiceTitan Scheduling Pro API
Online booking widgets, scheduler configurations, booking sessions.
- [Naftiko Capability — Sessions](capabilities/schedulingpro-sessions.yaml)

### ServiceTitan Job Booking & Capacity API (JBCE)
Call reasons, capacity-aware booking windows, slot suggestions. Bridges Telecom with JPM.
- [Naftiko Capability — Call Reasons](capabilities/jbce-call-reasons.yaml)

### ServiceTitan Webhooks API
Webhook subscription management. **V1 is closed to new subscriptions**; recommended interim pattern is `modifiedOnOrAfter` polling.
- [Naftiko Capability — Subscriptions](capabilities/webhooks-subscriptions.yaml)

## Artifacts

- [Spectral Rules](rules/servicetitan-rules.yml)
- [Vocabulary](vocabulary/servicetitan-vocabulary.yml)
- [JSON-LD Context](json-ld/servicetitan-context.jsonld)
- [Plans & Pricing (API Commons 0.1)](plans/servicetitan-plans-pricing.yml)
- [Rate Limits (API Commons 0.1)](rate-limits/servicetitan-rate-limits.yml)
- [FinOps (FOCUS 1.3 aligned)](finops/servicetitan-finops.yml)
- [Example: Create Customer](examples/servicetitan-customer-create-example.json)
- [Example: Create Job](examples/servicetitan-job-create-example.json)
- [Example: List Invoices](examples/servicetitan-invoice-list-example.json)

## Products

| Product | What it is |
|---|---|
| ServiceTitan | All-in-one core platform |
| FieldRoutes | Pest control vertical |
| Aspire | Landscape / cleaning vertical |
| Convex | Commercial property intelligence + sales |
| Conduit | Integration / workflow platform |
| Marketing Pro | Email + SMS campaigns |
| Dispatch Pro | ML-assisted automated dispatching |
| Scheduling Pro | Online booking (powered by Schedule Engine) |
| Pricebook Pro | Dynamic pricing + curated pricebook content |
| Fleet Pro | GPS / telematics integration |
| Contact Center Pro | Omnichannel contact center |
| Field Pro (formerly Sales Pro) | In-field sales enablement |
| Voice Agent | AI-powered voice handling |
| Atlas | Data platform |

## Open Source

- [`servicetitan/request-middleware-templates`](https://github.com/servicetitan/request-middleware-templates) — Liquid templates and scripts for connecting supply-chain partners to ServiceTitan.
- [`servicetitan/Stl.Fusion`](https://github.com/servicetitan/Stl.Fusion) — Real-time .NET / Blazor framework (MIT).

## Maintainers

- [Kin Lane](https://apievangelist.com) — info@apievangelist.com — `@apievangelist`
