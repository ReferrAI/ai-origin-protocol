# Standards Submission: AI Origin Protocol (AIOP)

**Submitted by:** ReferrAI (open-source community)  
**Specification:** AI Origin Protocol (AIOP), Draft v0.1  
**License:** Apache License 2.0  
**Status:** Informational / Early Draft  
**Submission Type:** Proposal for review and discussion  

---

## Overview

The ReferrAI open-source community respectfully submits the **AI Origin Protocol (AIOP)** for consideration and discussion as an early-stage, informational specification.

AIOP defines a **minimal, privacy-safe mechanism for documenting where AI-driven outcomes originate**, with an initial focus on AI-driven commerce intent. The protocol is designed to enable AI platforms to communicate **origin, intent, and aggregate efficacy signals** to downstream participants — such as retailers and publishers — without introducing user tracking, identity systems, or economic semantics.

---

## Motivation

AI systems are rapidly becoming a primary interface for discovery, recommendation, and decision-making. However, the ecosystem currently lacks a neutral, interoperable primitive to answer a foundational question:

> **Where did this AI-driven outcome originate?**

Existing mechanisms (cookies, redirects, UTMs, affiliate links, identity graphs) were not designed for AI-mediated interactions and increasingly conflict with modern privacy expectations and regulatory constraints.

AIOP is proposed as a **narrow, origin-only layer** that provides transparency without recreating the privacy failures of prior tracking-based approaches.

---

## Scope and Intent

AIOP is intentionally limited in scope. It defines:

- A short-lived, cryptographically verifiable **origin signal**
- No user identifiers or persistent state
- No requirements for adoption or enforcement
- No prescribed economic or attribution outcomes

The protocol is intended to sit **upstream of measurement, attribution, and monetization**, serving as a neutral input to downstream policy decisions rather than encoding those decisions itself.

---

## Explicit Non-Goals

To avoid ambiguity, AIOP explicitly does **not** aim to:

- Track users or sessions
- Create, resolve, or persist identity
- Assign credit or influence scores
- Guarantee deterministic attribution
- Define payments, compensation, or revenue sharing
- Replace existing advertising, affiliate, or retail media systems
- Orchestrate media buying or optimization workflows

These constraints are foundational to the protocol’s design and are treated as normative.

---

## Relationship to Existing Standards

AIOP is designed to **complement**, not compete with, existing and emerging standards, including but not limited to:

- Advertising workflow orchestration frameworks (e.g., AdCP)
- Retail Media Network APIs
- Content provenance initiatives (e.g., C2PA)

The protocol focuses specifically on **AI-driven outcome origin**, leaving activation, optimization, and economics to other layers.

---

## Current Status

The submitted draft represents:

- An initial, implementable **v0.1** specification
- JSON-based schemas and supporting documentation
- Open governance under an Apache-2.0 license
- Active development and discussion in public repositories

The ReferrAI community is seeking:

- Technical feedback
- Scope validation
- Interoperability guidance
- Input on potential standardization pathways

---

## Participation and Governance

ReferrAI is an open-source community and does not operate a commercial product. All work is conducted in public repositories, with decisions guided by a strong emphasis on privacy, minimalism, and interoperability.

If the protocol matures and demonstrates ecosystem value, ReferrAI is open to transitioning stewardship to an appropriate neutral standards body.

---

## Closing

The AI Origin Protocol is submitted in the spirit of early collaboration and open review. Its goal is not to prescribe outcomes, but to contribute a narrowly scoped, privacy-safe primitive that helps the ecosystem navigate the transition to AI-mediated experiences responsibly.

The ReferrAI community welcomes critical feedback and looks forward to constructive discussion.

---

**Repository:**  
ReferrAI GitHub Organization  
AI Origin Protocol Repository
