# ServiceTitan (servicetitan)

ServiceTitan is the operating system for the trades — all-in-one field service management software for residential and commercial contractors in HVAC, plumbing, electrical, roofing, garage door, pest control, refrigeration, fire & life safety, septic, landscape, and other service-based industries. The platform unifies CRM, dispatch, scheduling, job management, pricebook, mobile field execution, invoicing, payments, payroll, marketing attribution, memberships, service agreements, reporting, and Contact Center / Voice Agent capabilities behind a tenant-scoped V2 REST API surface accessed via OAuth 2.0 client credentials and a per-application App Key. ServiceTitan is the parent of FieldRoutes (pest), Aspire (landscape), and Convex (commercial sales), and ships Conduit as its integration platform.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/servicetitan/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/servicetitan/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Field Service Management
- Trades
- HVAC
- Plumbing
- Electrical
- Construction
- CRM
- Dispatch
- Accounting
- Pricebook
- Marketing
- Memberships
- Webhooks

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### ServiceTitan CRM API

Manage residential and commercial customer records, locations, contacts, leads, bookings, tags, and booking provider sessions. The CRM API is the primary entry point for customer-of-record data, address geocoding, and lead-to-customer conversion flows in ServiceTitan.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/crm/v2/{tenant}/`

#### Tags

- CRM
- Customers
- Leads
- Bookings
- Field Service

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-crm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/servicetitan-customer-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/servicetitan-location-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/servicetitan-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### ServiceTitan Job Planning & Management API

Create, retrieve, update, hold, cancel, and reschedule jobs, projects, appointments, job types, call reasons, job cancel reasons, and job history. JPM is the operational core of ServiceTitan — every work order and recurring service rolls through this surface.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/jpm/v2/{tenant}/`

#### Tags

- Jobs
- Projects
- Appointments
- Field Service
- Dispatch

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-jpm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/servicetitan-job-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/servicetitan-project-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/servicetitan-appointment-schema.json) — [JSON Schema](https://json-schema.org/specification)

### ServiceTitan Dispatch API

Manage technician shifts, appointment assignments, capacity windows, business hours, zones, arrival windows, and gps pings. Drives the dispatch board and integrates with Dispatch Pro automation.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/dispatch/v2/{tenant}/`

#### Tags

- Dispatch
- Scheduling
- Capacity
- Zones
- Field Service

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-dispatch-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Accounting API

Read and write invoices, invoice items, AP credits, payments, payment terms, payment types, journal entries, journal entry details, tax zones, and GL accounts. Integrates with QuickBooks Online, QuickBooks Desktop, Sage Intacct, and Acumatica exports.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/accounting/v2/{tenant}/`

#### Tags

- Accounting
- Invoices
- Payments
- Journal Entries
- Tax Zones

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-accounting-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/servicetitan-invoice-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/servicetitan-payment-schema.json) — [JSON Schema](https://json-schema.org/specification)

### ServiceTitan Pricebook API

CRUD over the pricebook — categories, services, materials, equipment, discounts and fees, images, and pricebook bulk operations. Powers Pricebook Pro dynamic pricing and technician-facing flat-rate presentations.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/pricebook/v2/{tenant}/`

#### Tags

- Pricebook
- Services
- Materials
- Equipment
- Pricing

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-pricebook-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/servicetitan-service-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/servicetitan-material-schema.json) — [JSON Schema](https://json-schema.org/specification)

### ServiceTitan Inventory API

Manage purchase orders, purchase order types, transfers, returns, adjustments, receipts, warehouses, trucks, vendors, and inventory bills. Backed by ServiceTitan's request-middleware-templates Liquid framework for supply-chain partner integrations.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/inventory/v2/{tenant}/`

#### Tags

- Inventory
- Purchase Orders
- Warehouses
- Trucks
- Supply Chain

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-inventory-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Marketing API

Manage marketing campaigns, campaign categories, suppression lists, and attribution data that powers cost-per-lead and cost-per-booked-job reporting. Underpins Marketing Pro email and SMS campaigns.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/marketing/v2/{tenant}/`

#### Tags

- Marketing
- Campaigns
- Attribution
- Categories
- Suppression

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Marketing Reputation API

Retrieve aggregated customer reviews and reputation metrics across Google, Facebook, Yelp, BBB, and other connected review providers. Read-only API surfacing review text, ratings, sentiment, and response state.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/marketingreputation/v2/{tenant}/`

#### Tags

- Marketing
- Reputation
- Reviews
- Sentiment

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Memberships API

Manage membership types, customer memberships, membership invoice templates, recurring service types, and recurring service events. Drives the recurring revenue surface — maintenance agreements, club memberships, and annual tune-up plans.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/memberships/v2/{tenant}/`

#### Tags

- Memberships
- Recurring Services
- Contracts
- Subscriptions

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Service Agreements API

Manage commercial service agreements — contract terms, billed locations, line items, renewal cadence, and invoice generation rules. Used by commercial trades for multi-site recurring service contracts.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/serviceagreements/v2/{tenant}/`

#### Tags

- Service Agreements
- Contracts
- Commercial
- Renewals

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Equipment Systems API

Read and write installed equipment records per customer location — make, model, serial, install date, warranty terms, attachments, and equipment history. The asset-of-record API for HVAC, plumbing, electrical, and refrigeration trades.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/equipmentsystems/v2/{tenant}/`

#### Tags

- Equipment
- Installed Equipment
- Assets
- Field Service

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-equipment-systems-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Forms API

Retrieve form definitions and field-completed form submissions including photos, signatures, checkbox values, and free-text responses. Used for safety checklists, equipment commissioning, compliance audits, and post-service surveys.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/forms/v2/{tenant}/`

#### Tags

- Forms
- Submissions
- Compliance
- Field Capture

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Payroll API

Manage payroll adjustments, gross-pay items, job splits, timesheet codes, activity codes, non-job timesheets, and payroll settings. Exports to ADP, Paychex, Gusto, Paylocity, and other downstream payroll providers.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/payroll/v2/{tenant}/`

#### Tags

- Payroll
- Timesheets
- Adjustments
- Compensation

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Timesheets API

Read and write timesheet entries, activity codes, and shift segments tying technician time to jobs, non-job activities, paid time off, and travel. Feeds the Payroll API and FieldRoutes reconciliation.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/timesheets/v2/{tenant}/`

#### Tags

- Timesheets
- Time Tracking
- Activity
- Payroll

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Reporting API

Run published custom reports with parameters and retrieve dynamic value sets used by report inputs. Lower rate limit than other surfaces — 1 of the same report per minute per tenant. Replaces fragile UI exports for BI pipelines.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/reporting/v2/{tenant}/`

#### Tags

- Reporting
- Analytics
- Custom Reports
- Beta

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Sales & Estimates API

Create and retrieve estimates, estimate items, and proposal templates. Backs the Proposal Builder feature used to convert leads into approved scopes of work — including good / better / best presentations from technicians in the field.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/sales/v2/{tenant}/`

#### Tags

- Sales
- Estimates
- Quotes
- Proposals

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Customer Interactions API

Submit and retrieve post-service technician ratings and customer feedback. Powers the "How did we do?" SMS / email flow that aggregates into Marketing Reputation.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/customerinteractions/v2/{tenant}/`

#### Tags

- Customer Feedback
- Technician Ratings
- NPS
- Surveys

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Settings API

Manage business units, employees, technicians, user roles, employee permissions, tag types, and tenant-wide settings. The tenant configuration surface for every other API in the platform.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/settings/v2/{tenant}/`

#### Tags

- Settings
- Business Units
- Technicians
- User Roles
- Tenants

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [OpenAPI](openapi/servicetitan-settings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Task Management API

Create, update, and resolve internal tasks, task types, sub-tasks, and task statuses. Used for office-to-field handoffs, escalations, and back-office workflows that aren't customer jobs.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/taskmanagement/v2/{tenant}/`

#### Tags

- Tasks
- Workflow
- Internal Tickets

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Telecom API

Retrieve inbound and outbound call records, call recordings, call analytics, and call reasons. Powers Contact Center Pro reporting and Voice Agent transcript analysis.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/telecom/v3/{tenant}/`

#### Tags

- Telecom
- Calls
- Voice
- Contact Center

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Scheduling Pro API

Power online booking widgets — list configured schedulers, retrieve scheduler availability, create and update booking sessions. Backed by the Schedule Engine acquisition; required for customer-facing self-service scheduling.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/schedulingpro/v2/{tenant}/`

#### Tags

- Scheduling Pro
- Online Booking
- Schedulers
- Sessions

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Job Booking & Capacity API

Retrieve call reasons, job booking call reason metadata, capacity-aware booking windows, and recommended slot suggestions. Bridges Telecom call intake with JPM job creation.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/jbce/v2/{tenant}/`

#### Tags

- Job Booking
- Call Reasons
- Capacity Estimation
- Field Service

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ServiceTitan Webhooks API

Manage webhook subscriptions for customer, job, appointment, invoice, payment, and membership lifecycle events. V1 is closed to new subscriptions; V2 webhooks are in development. Polling-based change-tracking via `modifiedOnOrAfter` filters is the recommended interim pattern.

- **Human URL:** [https://developer.servicetitan.io/api-details/](https://developer.servicetitan.io/api-details/)
- **Base URL:** `https://api.servicetitan.io/webhooks/v1/{tenant}/`

#### Tags

- Webhooks
- Events
- Integration

#### Properties

- [Documentation](https://developer.servicetitan.io/api-details/)
- [Postman Collection](collections/servicetitan-accounting-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-accounting-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-crm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-crm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-dispatch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-dispatch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-equipment-systems-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-equipment-systems-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-jpm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-jpm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-pricebook-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-pricebook-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/servicetitan-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/servicetitan-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/servicetitan)
- [GitHub Organization](https://github.com/servicetitan)
- [Portal](https://developer.servicetitan.io/)
- [Getting Started](https://developer.servicetitan.io/docs/welcome/)
- [Documentation](https://developer.servicetitan.io/docs/apis)
- [Documentation](https://developer.servicetitan.io/api-details/)
- [Documentation](https://developer.servicetitan.io/docs/get-going-environments/)
- [Documentation](https://developer.servicetitan.io/docs/faqs-apis-app-keys-client-keys/)
- [Portal](https://partnerapis.servicetitan.io/apis/)
- [Getting Started](https://help.servicetitan.com/how-to/get-started-with-apidev-portal-v2)
- [Rate Limits](https://help.servicetitan.com/problem-solution/what-are-the-default-api-rate-limits-in-servicetitan-for-regular-apis-and)
- [Status Page](https://status.servicetitan.com/)
- [Portal](https://www.servicetitan.com/)
- [Documentation](https://www.servicetitan.com/products)
- [Blog](https://www.servicetitan.com/blog)
- [Blog](https://www.servicetitan.com/news)
- [About Us](https://www.servicetitan.com/about-us)
- [Case Studies](https://www.servicetitan.com/customer-stories)
- [Careers](https://www.servicetitan.com/careers)
- [Forum](https://community.servicetitan.com/)
- [Privacy Policy](https://www.servicetitan.com/legal/privacy-policy)
- [Terms of Service](https://www.servicetitan.com/legal/terms-of-service)
- [Trust Center](https://www.servicetitan.com/trust)
- [Pricing](https://www.servicetitan.com/pricing)
- [Contact Info](https://www.servicetitan.com/contact)
- [Partners](https://www.servicetitan.com/partners)
- [Sign In](https://app.servicetitan.com/)
- [Tool](https://github.com/servicetitan/request-middleware-templates)
- [Tool](https://github.com/servicetitan/Stl.Fusion)
- [Documentation](https://www.postman.com/api-evangelist/servicetitan)
- [Marketplace](https://www.servicetitan.com/products/integrations)
- [Documentation](https://www.servicetitan.com/products/conduit)
- [Documentation](https://www.servicetitan.com/products/fieldroutes)
- [Documentation](https://www.servicetitan.com/products/aspire)
- [Documentation](https://www.servicetitan.com/products/convex)
- [Documentation](https://www.servicetitan.com/products/atlas)
- [Plans](plans/servicetitan-plans-pricing.yml)
- [Rate Limits](rate-limits/servicetitan-rate-limits.yml)
- [Fin Ops](finops/servicetitan-finops.yml)
- [Vocabulary](vocabulary/servicetitan-vocabulary.yml)
- [Spectral Rules](rules/servicetitan-rules.yml)
- [Authentication](undefined)
- [Environments](undefined)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
