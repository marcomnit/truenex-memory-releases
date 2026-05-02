# truenex-memory-releases

Public release manifest and update metadata for Truenex Memory.

This repository intentionally contains only public metadata used by manual update checks.
It must not contain project memory, source code snapshots, secrets, telemetry data, or private release logic.

## Manifest

The CLI reads:

```text
https://raw.githubusercontent.com/marcomnit/truenex-memory-releases/main/version.json
```

Current manifest fields:

- `manifest_version`: manifest schema version.
- `version`: latest Truenex Memory application version.
- `channel`: `dev`, `beta`, or `stable`.
- `force_update`: if `true`, clients report an available update even for the same version.
- `update_full`: reserved for future installer behavior.
- `download_url`: optional release artifact URL.
- `release_notes_url`: optional release notes URL.
- `requires_migration`: whether the update requires a local DB migration.
- `min_supported_version`: oldest supported client version.

Truenex Memory does not auto-update silently. The client performs manual update checks and sends no project data.
