# intent_token (v0.1)

**Purpose:** Document provenance of AI-generated commerce intent.

## Requirements
- MUST NOT include user identifiers or PII.
- SHOULD be short-lived (TTL ≤ 15 minutes).
- MUST be cryptographically signed to prevent tampering.

## Suggested fields
- `ai_surface_id` (required)
- `publisher_id` (optional)
- `product_ref` (required)
- `context` (optional, freeform)
- `timestamp` (required)
- `signature` (required)
