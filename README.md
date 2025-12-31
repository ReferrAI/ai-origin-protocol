# AI Intent Provenance Protocol (AIPP)

> **Maintained by the ReferrAI open-source community**

The **AI Intent Provenance Protocol (AIPP)** is a lightweight, privacy-safe specification for documenting **where AI-generated commerce intent originated**.

As AI assistants become a primary discovery surface for products, retailers and publishers lack a standard way to understand **which AI experiences influenced intent** — without tracking users, relying on cookies, or introducing new identity systems.

AIPP solves this by defining a simple, cryptographically signed **intent token** that can travel from an AI experience to a retailer and be validated at the moment of engagement or conversion.

---

## About ReferrAI

**ReferrAI** is an open-source community focused on building **neutral infrastructure for AI referral and intent provenance**.

ReferrAI is **not a company** and does not operate a commercial product.  
It exists to steward open specifications, documentation, and reference tooling that enable transparency in AI-driven experiences.

---

## What This Protocol Is

**AIPP is an intent provenance signal — not a tracking system.**

It provides a standardized way for downstream systems to answer one simple question:

> *“Which AI experience influenced this intent?”*

### Core principles
- **No user identity** — zero PII by design  
- **Short-lived tokens** — no persistence or cross-site tracking  
- **Provenance, not attribution graphs**  
- **Optional and interoperable** — adopters choose how to use the signal  

---

## What This Protocol Is Not (Non-Goals)

The AI Intent Provenance Protocol explicitly does **not** aim to:

- ❌ Track users across sites or sessions  
- ❌ Create, resolve, or persist identity  
- ❌ Replace affiliate networks, RMNs, or ad platforms  
- ❌ Guarantee deterministic attribution  
- ❌ Act as a payments, settlement, or revenue-sharing system  
- ❌ Compete with AdCP, OpenRTB, or clean room frameworks  

These are deliberate non-goals to ensure privacy safety, platform compatibility, and ease of adoption.

---

## Mental Model

**AIPP is a modern, cryptographically verifiable successor to the HTTP `Referer`, purpose-built for AI-driven commerce.**

- HTTP Referer → broke under privacy pressure  
- Cookies → being deprecated  
- UTMs → forgeable and brittle  

AIPP provides a **verifiable, privacy-preserving signal** that documents *where AI intent came from* — nothing more.

---

## How It Works (High Level)

1. **AI experience generates intent**  
2. **Intent token is issued**  
3. **Retailer resolves the token**  
4. **Optional aggregate outcomes**  

At no point does the protocol identify a user.

---

## Core Primitive

### `intent_token` (v0.1)

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
```

**Key properties**
- TTL ≤ 15 minutes  
- No user identifiers  
- Cryptographically signed to prevent forgery or replay  

---

## Relationship to Other Standards

- **AdCP**: ad workflow orchestration  
- **AIPP**: AI commerce intent provenance  

AIPP sits upstream of measurement and activation.

---

## Why This Matters

- Retailers: visibility into AI-driven demand without privacy risk  
- Publishers: acknowledgment when their content informs AI intent  
- AI platforms: neutral disclosure mechanism  
- Regulators: clearer provenance without new tracking vectors  

Documented intent provenance may support downstream uses such as analytics, disclosures, or publisher compensation policies — without the protocol defining those mechanisms.

---

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

---

> **No identity. No tracking. Just provenance.**
