---
"cf": minor
---

Add `cf tunnels tail`

Stream structured logs from remote cloudflared connectors, with filters for
connectors, events, levels, and sampling.
Management tokens can be supplied through `TUNNEL_MANAGEMENT_TOKEN` so they do
not appear in the long-lived cf process arguments.
