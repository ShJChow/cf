---
"cf": minor
---

Add `cf pages deploy` with Pages deployment guidance

Direct existing legacy Pages projects to `wrangler pages deploy` when a Wrangler
Pages cache exists. Direct new projects to `cf deploy` for Pages on Workers
without attempting a deployment.
