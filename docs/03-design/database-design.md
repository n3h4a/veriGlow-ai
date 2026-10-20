# Database Design

| | |
|---|---|
| **Status** | ⏳ Not started |
| **Phase** | 4 — Architecture & Design |
| **Depends on** | [PRD](../02-product/PRD.md), [System Design](system-design.md) |

---

## Purpose

Define the data model, storage choices, and data lifecycle for VeriGlow-ai.

## Sections (to be completed)

1. **Entities and relationships** — ER diagram (Mermaid `erDiagram`)
2. **Schema** — tables, keys, constraints, indexes
3. **Storage choice** — with a linked ADR
4. **Data retention and deletion** — especially for user-uploaded images
5. **Migrations strategy**
6. **Seed and test data**

## Candidate Entities (hypotheses — will change after the PRD)

| Entity | Description |
|---|---|
| Product | A specific beauty product (brand, name, variant) |
| Listing | A product offered by a seller on a marketplace |
| Seller | The party selling a listing |
| Verification | A single trust check and its result |
| Evidence | Signals and reasons supporting a verification result |
