---
"cf": patch
---

Only list delegated environment overrides when `DEBUG` is set

`cf dev` and `cf build` still announce the framework command they delegate to,
but the registry and build-output environment variables passed to it are now
printed only when `DEBUG` is set.
