---
"cf": minor
---

Choose the `cf migrate` bundler from the project

`cf migrate` now uses the Vite bundler only when `@cloudflare/vite-plugin` is declared next to the Wrangler configuration, and uses the Wrangler bundler otherwise. Previously, every project defaulted to Vite, so migrations of non-Vite Workers reported Vite-only follow-ups even though `cf build` would continue to use Wrangler. Pass `--bundler vite` or `--bundler wrangler` to choose explicitly.
