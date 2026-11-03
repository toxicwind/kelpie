# AGENTS.md — Kelpie (`pens/kelpie`)

> Part of the estate's pens family. A pens repo is a **thin coordinator**, not a
> product monorepo. It owns only its own metadata, `bin/`, and `docs/`. Products
> are peer standalone checkouts, referenced-not-owned. Pattern: geode/olympus.

## The pack (products are peer repos)

- `products/estate-shell` — **the flagship**: shell SSOT (dots, env doctrine,
  pure-TS deploy engine, env doctor). This is the platform axis — none of the
  public quickshell rices (Panacea, Serashell, Shizuka) have engine/doctor.
- (next) `products/estate-end4` — quickshell ii dots lineage (visual axis).
- (next) the DP3/keeper surface.

## Rules

1. **Never** `git submodule add`, never a gitlink. `*` ignores everything;
   product checkouts auto-ignored.
2. A product is a peer clone with its own remote + history.
3. Pen git status stays clean regardless of what products do.
4. `bin/` symlinked into `~/.local/bin`, pinned by estate-ops manifest.
5. Runtime: Bun/TypeScript. Secrets: secretsmith keyring only.

## Comparison anchor (2026-11-02)

Public quickshell rices own the *visual* axis (shell.qml, widgets, lockscreens).
Husky owns the *platform* axis (env doctrine, deploy, doctor) — that is the
estate's differentiator; the visual surface is the catch-up product.
