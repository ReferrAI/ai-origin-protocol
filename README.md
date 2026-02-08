# AI Origin Protocol (AIOP)

> **Maintained by the ReferrAI open-source community**

The **AI Origin Protocol (AIOP)** is a lightweight, privacy-safe specification for documenting **where AI-driven outcomes originate** — with an initial focus on **AI-driven commerce intent**.

As AI systems increasingly influence how people discover products, content, and services, the ecosystem lacks a neutral, standards-grade way to answer a simple question:

> *Where did this AI-driven outcome come from?*

AIOP provides a minimal, verifiable answer — **without tracking users, creating identity systems, or defining economics**.

---

## About ReferrAI

**ReferrAI** is an open-source community stewarding **neutral infrastructure for AI origin and referral transparency**.

ReferrAI:
- Is **not a company**
- Does **not** operate a commercial product
- Does **not** monetize the protocol
- Exists to steward open specifications, documentation, and reference materials

All development happens in public GitHub repositories.

---

## What the AI Origin Protocol Is

**AIOP is an origin signal — not a tracking system.**

It enables downstream systems to understand **which AI experience or surface originated an outcome**, such as:
- A product recommendation
- A commerce referral
- A disclosed AI influence

### Core principles
- 🚫 **No user identity** (zero PII by design)
- ⏱ **Short-lived tokens** (no persistence)
- 🔍 **Verifiable, not behavioral**
- 🔌 **Optional and interoperable**
- 🧱 **Boring by design**

---

## What AIOP Is Not (Non-Goals)

The AI Origin Protocol explicitly does **not** aim to:

- Track users or sessions
- Create, resolve, or persist identity
- Perform attribution or influence scoring
- Guarantee deterministic credit
- Define payments, revenue sharing, or “vig” models
- Replace affiliate networks, RMNs, or ad platforms
- Orchestrate media buying or optimization workflows

These boundaries are foundational to trust and adoption.

---

## Mental Model

**AIOP is a modern successor to the HTTP `Referer`, designed for AI systems.**

- Cookies → being deprecated  
- UTMs → brittle and forgeable  
- Identity graphs → privacy-sensitive  

AIOP provides a **cryptographically verifiable origin signal** that documents *where an AI-driven outcome originated* — nothing more.

---

## How It Works (High Level)

1. An AI experience generates an outcome (e.g., a product recommendation)
2. A short-lived, signed **origin token** is issued
3. The token is passed to a downstream system (e.g., retailer, platform)
4. The token is validated and origin is logged
5. Optional, **aggregate** outcome signals may be produced

At no point does the protocol identify a user.

---

## Core Primitive

### `intent_token` (v0.1)

> *Note: The token name remains `intent_token` for stability in v0.1.  
> Future versions may generalize naming as the protocol evolves.*

```json
{
  "from_ai": {
    "ai_surface_id": "chatgpt",
    "publisher_id": "example_publisher",
    "product_ref": {
      "merchant": "amazon",
      "sku": "B0D12345W"
    },
    "context": "holiday_gift_guide",
    "timestamp": "2025-11-10T15:02:00Z",
    "signature": "ed25519..."
  }
}
