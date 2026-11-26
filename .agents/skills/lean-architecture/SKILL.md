---
name: lean-architecture
description: Design lean, cost-efficient backend schemas, API routes, and serverless deployments. Use when designing database tables, API endpoints, auth flows, or hosting setups.
---

# Lean Architecture & Resource Efficiency

## Principles
1. **Flat, Normalized Schemas:** Keep database tables straightforward with clear foreign keys and indexes. Avoid premature sharding, complex event buses, or unnecessary caching layers.
2. **Free-Tier Friendly:** Optimize queries, payload sizes, and storage retention so the system runs reliably within serverless and free-tier quotas.
3. **Thin Endpoints:** Keep controllers/routes thin - validate input at the boundary, execute the query or mutation cleanly, and return consistent status codes.
4. **Security by Default:** Never hardcode secrets, always enforce row-level or role-based access checks on mutations, and sanitize external inputs.
