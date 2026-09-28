---
"cf": patch
---

Allow prebuilt Build Output with a recorded mode to deploy without `--mode`

Validate the recorded build mode when a command explicitly requests a mode. This lets `cf deploy --prebuilt` use output from Vite and other builders that record their default mode without requiring the user to repeat it. Use the account ID and compliance region recorded in Build Output without reevaluating source config. When the output omits an account ID, use environment or profile account selection in the built region.
