# System Design

| | |
|---|---|
| **Status** | ⏳ Not started |
| **Phase** | 4 — Architecture & Design |
| **Depends on** | [Architecture](architecture.md) |

---

## Purpose

Describe how the system works internally: components, data flow, and how it behaves under load and failure.

## Sections (to be completed)

1. **Components and responsibilities**
2. **Request flow** for each core user flow (sequence diagrams)
3. **AI / verification pipeline** — inputs, processing steps, outputs, confidence and explanation
4. **Scalability** — expected load and how the design handles growth
5. **Reliability** — failure modes and fallbacks (e.g. AI provider unavailable)
6. **Security and privacy** — handling of user-uploaded images and personal data
7. **Cost model** — main cost drivers for the MVP

## Key Design Questions

- What happens when the AI is uncertain? *(The system must be able to say "we don't know".)*
- Which work must be synchronous, and which can run in the background?
- What data must be stored, and for how long?
