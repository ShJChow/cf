---
"cf": minor
---

Add `cf init` for creating and setting up projects

`cf init [directory]` creates a hello-world Worker in a new or empty directory (a `.git` directory is allowed) using the `@cloudflare/vite-plugin` v2 beta, then installs dependencies with the package manager you pick. After installing, it generates `.cloudflare/types/index.d.ts` with the same generator as `cf workers types`; with `--no-install`, `cf dev` or the new project's `typecheck` script (`cf workers types && tsc`) generates them later. Directories that already contain files are configured with autoconfig instead. If you leave out the directory, cf asks which one to use, and it shows the target before making changes. When it finishes, cf lists the next steps, starting with `cf dev`. `cf init workers [directory]` is the default initializer and currently behaves the same way, leaving room for other product initializers.

```sh
cf init my-worker
```
