# P01: Database Design and Table Relationships

| | |
|---|---|
| **Status** | 🚧 In progress |
| **Started** | 2026-10-04 |
| **Completed** | - |
| **Branch** | `feature/p01-database-design` |
| **Pull request** | [PRs by deadyiss](https://github.com/mirzayogy/laravel5d/pulls?q=is%3Apr+author%3Adeadyiss) |

## Goal
Design and implement the database of the **Flagboard** CTF competition management platform, focusing on table relationships with Eloquent: One-to-One, One-to-Many, Many-to-Many (with pivot data), and Has-Many-Through.

## Jobs

| Code | Job | Status | Completed | Proof |
|---|---|---|---|---|
| J1 | Project README with ERD diagram | ✅ Done | 2026-10-04 | [commit 30a4b18](https://github.com/deadyiss/laravel5d/commit/30a4b18a709a39b514f7c7a994f0b2eba92fff1c) |
| J2 | ERD documentation and README sync | ✅ Done | 2026-10-25 | [erd.md](../database/erd.md), [branch commits](https://github.com/deadyiss/laravel5d/commits/feature/p01-database-design) |
| J3 | Progress report | ✅ Done | 2026-10-25 | [branch commits](https://github.com/deadyiss/laravel5d/commits/feature/p01-database-design) |
| J4 | Migrations | ⏳ Planned | - | - |
| J5 | Models and relationships | ⏳ Planned | - | - |
| J6 | Factories and seeders | ⏳ Planned | - | - |

**Status legend:** ⏳ Planned · 🚧 In progress · ✅ Done · ⛔ Blocked

---

### J1: Project README with ERD diagram
- **Status:** ✅ Done, 2026-10-04
- **What:** English root README with project description, features, ERD diagram in Mermaid, relationship table, business rules, setup steps, and roadmap.
- **Proof:** [`README.md`](../../README.md), [commit 30a4b18](https://github.com/deadyiss/laravel5d/commit/30a4b18a709a39b514f7c7a994f0b2eba92fff1c)
- **Verified:** the Mermaid diagram renders on the GitHub page of `README.md`.

### J2: ERD documentation and README sync
- **Status:** ✅ Done, 2026-10-25
- **What:** `docs/database/erd.md` with the full ERD of 13 tables, the Eloquent relationship summary, the seeded categories, and design notes. Three pivot tables carry extra data: `competition_team` (`registered_at`), `hint_unlocks` (`unlocked_at`), and `submissions` (`is_correct`, `submitted_at`). Flags are stored as hashes only. The README diagram was updated to match `erd.md`, and the clone URL in the README was filled in.
- **Proof:** [`docs/database/erd.md`](../database/erd.md), [`README.md`](../../README.md), [branch commits](https://github.com/deadyiss/laravel5d/commits/feature/p01-database-design)
- **Not done:** migrations and models for these tables.

### J3: Progress report
- **Status:** ✅ Done, 2026-10-25
- **What:** This file, recording phase P01 with its jobs, status, and proof.
- **Proof:** [`docs/progress/P01-database-design.md`](P01-database-design.md), [branch commits](https://github.com/deadyiss/laravel5d/commits/feature/p01-database-design)

### J4: Migrations
- **Status:** ⏳ Planned
- **What:** Table migrations for the 13 tables, with foreign keys, cascade and restrict rules, and unique constraints as described in the ERD design notes.

### J5: Models and relationships
- **Status:** ⏳ Planned
- **What:** Eloquent models with `hasOne`, `hasMany`, `belongsTo`, `belongsToMany` (with `withPivot`), and `hasManyThrough`.

### J6: Factories and seeders
- **Status:** ⏳ Planned
- **What:** Factories for all models, a category seeder (6 categories), and a database seeder with sample competitions, teams, challenges, and submissions.

---

## Next
Finish J4 to J6, then update this file and the PR description. Later phases get their own file in this folder, for example `P02-authentication-and-teams.md`, each with its own jobs (J1, J2, ...).

Reference jobs in commit messages, for example `P01-J4: add challenges migration`.