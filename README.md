# DeepSO package repository

Packages live under `packages/<id>.dsoplug`. Configure DeepSO with `pkg repo Deep-sea-lab/deepso-pkg/main`, then install by ID.

## Packages

- `welcome`: lifecycle-safe metadata starter; no executable code.
- `fortune`: lifecycle-safe metadata starter; no executable code.
- `hi`: enter `hi` in the shell; DeepSO shows a `☺ hi` speech bubble. The package waits for `DSO_PROC_START` to open and for `DSO_BOOTED` to become 1, registers its opcode in the shared compiler lists, then asks the kernel recompiler to link the command.

## Manifest contract

Each package uses `format: dsoplug`, `version: 1`, an `id` matching its filename, a `roles` array, an `executorBlocks` Scratch block map, and `executorTargetIndex: 1` for the Stage.

The `hi` package is a Scratch executor-block plugin and relies on the current DeepSO Stage globals and compiler lists. Install it only in a compatible DeepSO project.
