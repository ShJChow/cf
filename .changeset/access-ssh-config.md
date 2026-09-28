---
"cf": minor
---

Add `cf access ssh-config`

Print cloudflared-backed SSH configuration, including short-lived certificate
configuration when requested.
The generated configuration invokes `cloudflared access ssh-gen` for
certificate renewal.
