---
"cf": minor
---

Add `cf migrate` for Wrangler projects

Convert a Wrangler JSON, JSONC, or TOML configuration to `cloudflare.config.ts` using `@cloudflare/codemods`. The command supports Vite and Wrangler bundlers, dry runs, clean-worktree protection, and reports any manual follow-up work left by the migration. Pass `--no-install` to skip installing `cf` in the migrated project.
