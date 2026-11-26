---
name: db-schema-rls
description: Enforce clean database schema design, fast query patterns, and strict access policies. Use when creating tables, writing migrations, optimizing queries, or setting up Row-Level Security (RLS).
---

# Database Schema & Access Control

## Rules
1. **Explicit Relations & Indexes:** Define clear primary/foreign keys, NOT NULL constraints, and indexes on columns used in WHERE, JOIN, and ORDER BY clauses.
2. **Lean Queries:** Never use SELECT * in production paths. Fetch only required columns and batch related reads to prevent N+1 query waterfalls.
3. **Least-Privilege Access:** Enable RLS or explicit role/ownership checks on every table and mutation so users can only read or modify authorized records.
4. **Safe Migrations:** Make schema changes additive and reversible whenever possible.
