# API Design

| | |
|---|---|
| **Status** | ⏳ Not started |
| **Phase** | 4 — Architecture & Design |
| **Depends on** | [System Design](../03-design/system-design.md) |

---

## Purpose

Define the contract between the frontend and backend (and any external consumers).

## Principles (proposed)

- **Contract first:** the API is specified (e.g. OpenAPI) before it is implemented.
- **Resource-oriented** URLs and standard HTTP methods and status codes.
- **Versioned** from day one (e.g. `/api/v1/...`).
- **Consistent error format** across all endpoints.
- **Paginated** list endpoints.

## Sections (to be completed)

1. Authentication and authorisation
2. Resource list and endpoints
3. Request / response schemas
4. Error model
5. Rate limiting
6. Versioning and deprecation policy

## Endpoint Inventory

| Method | Path | Purpose | Auth |
|---|---|---|---|
| *TBD* | | | |
