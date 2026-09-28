---
"cf": minor
---

Add `--worker` to Build Output deploy workflows

`cf deploy`, `cf previews deploy`, `cf workers versions create`, `cf workers triggers deploy`, and `cf workers check` now accept `--worker <name>` to use a named Worker from the Build Output instead of the default Worker. The name matches the Worker's configured name. An unknown name fails before any API request and lists the available Workers.
