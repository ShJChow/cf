---
"cf": minor
---

Add `cf access curl`

Make authenticated curl requests to Access applications while preserving curl
arguments after `--` and cloudflared's optional unauthenticated fallback.
The fallback accepts cloudflared's `--allow-request` and `-ar` spellings.
