---
name: project-conventions
description: Enforce the Flutter + Dart tech stack (Supabase, Cloudflare R2), feature-first folder structure, snake_case naming rules, and zero-cost storage/bandwidth architecture. Use whenever scaffolding features, writing database queries, handling file uploads, or creating widgets.
---

# Flutter Project Conventions

## 1. Locked Tech Stack
- **Framework:** Flutter (Dart)
- **Icons & Styling:** `iconoir_flutter` + custom monochrome neutral `ThemeData` (strictly follow the `minimalist-ui` skill)
- **Database, Auth & APIs:** Supabase (`supabase_flutter` + PostgreSQL + RLS)
- **Media & File Storage:** Cloudflare R2 (via short-lived presigned URLs)

## 2. Zero-Cost Storage & Bandwidth Architecture
- **Strict Storage Split:** Never upload images, videos, or binary files to Supabase Storage. Store all binary files exclusively in **Cloudflare R2** to keep egress bandwidth free.
- **Metadata in Supabase Postgres:** Store only file metadata (R2 public URL or object key, owner ID, original filename, MIME type, file size, and permissions) inside a regular Supabase Postgres table.
- **Direct Client-to-R2 Uploads:** Request a short-lived presigned upload URL from a lightweight endpoint/edge function and upload directly from the Flutter client to Cloudflare R2.
- **Atomic Cleanup:** Whenever a record or file is deleted, remove both the object in Cloudflare R2 and its metadata row in Supabase Postgres.
- **Lean Queries:** Select only explicit columns in Supabase queries (avoid `select(*)`) to keep mobile data payloads minimal.

## 3. Folder & Naming Conventions
- `lib/core/` - Theme, Supabase client initialization, constants, and shared utilities using `snake_case.dart`.
- `lib/features/<feature>/` - Feature-first modules (`data/`, `models/`, `screens/`, `widgets/`) using `snake_case.dart` filenames and `PascalCase` classes.
- `lib/shared/widgets/` - Reusable monochrome UI components using `snake_case.dart`.

## 4. Security & Environment Guardrails
- Enforce Row-Level Security (RLS) on every Supabase table, including file metadata tables.
- Never bundle `R2_SECRET_ACCESS_KEY` or `SUPABASE_SERVICE_ROLE_KEY` inside the Flutter app binary; load only public anon keys via `--dart-define` or `.env`.
