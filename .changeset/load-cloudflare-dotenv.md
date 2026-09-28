---
"cf": minor
---

Allow `cf` commands to use these variables from `.env` files:

- `CLOUDFLARE_ACCESS_CLIENT_ID`
- `CLOUDFLARE_ACCESS_CLIENT_SECRET`
- `CLOUDFLARE_ACCOUNT_ID`
- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_COMPLIANCE_REGION`
- `CLOUDFLARE_ZONE_ID`
- `WRANGLER_API_ENVIRONMENT` (legacy)

The allowlist is intentional: other variables, such as
`CLOUDFLARE_API_BASE_URL`, are not loaded from project files. Files are merged
from lowest to highest precedence: `.env`, `.env.local`, then, when `--mode` is
set, `.env.<mode>` and `.env.<mode>.local`. Values already present in the
process environment override every file.

File values are applied only while the relevant part of `cf` is running and
are removed afterward. Mixed commands such as `deploy` run their delegated
build before loading the values, then make their API calls with the values
available. When a cloudflared-backed command needs file values, it makes them
available only while `cf` resolves configuration or makes API calls, then
restores them before starting cloudflared.
