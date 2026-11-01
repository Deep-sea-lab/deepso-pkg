# DeepSO package repository

Packages live under `packages/<id>.dsoplug`. Configure DeepSO with `pkg repo Deep-sea-lab/deepso-pkg/main`, then install by ID.

## Packages

- `welcome`: lifecycle-safe metadata starter; no executable code.
- `fortune`: lifecycle-safe metadata starter; no executable code.
- `hi`: enter the exact shell command `hi` to show a smiling `☺ hi` speech bubble for three seconds. The process waits for the shared `DSO_PROC_START` gate to be zero before watching `DSO_LINE`, and waits for the next command before re-arming.

## Manifest contract

Each package uses `format: dsoplug`, `version: 1`, an `id` matching its filename, a `roles` array, an `executorBlocks` Scratch block map, and `executorTargetIndex: 1` for the Stage.

The `hi` package is a Scratch executor-block plugin. It relies on the current DeepSO Stage globals `DSO_PROC_START` and `DSO_LINE`; install it only in a compatible DeepSO project.
