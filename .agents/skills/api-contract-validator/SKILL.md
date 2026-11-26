---
name: api-contract-validator
description: Enforce strict input validation, predictable response shapes, and clean error handling on API routes and server actions. Use when creating or updating endpoints, forms, or webhooks.
---

# API Contract Validator

## Rules
1. **Validate at the Boundary:** Parse and validate all request bodies, query params, and headers using strict schemas before running business logic.
2. **Consistent Response Envelope:** Return uniform JSON structures and proper HTTP status codes (200, 201, 400, 401, 403, 404, 500).
3. **Safe Error Messages:** Return actionable, user-safe error messages without exposing internal stack traces, SQL errors, or environment details.
4. **Idempotency & Guardrails:** Handle duplicate submissions gracefully and reject oversized or malformed payloads early.
