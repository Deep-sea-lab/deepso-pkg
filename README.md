# DeepSO package repository

Packages live under packages/<id>.dsoplug. Configure DeepSO with `pkg repo Deep-sea-lab/deepso-pkg/main`, then install by ID with `pkg install welcome` or `pkg install fortune`.

## Package contract

Each manifest uses format `dsoplug`, version 1, an `id` matching the filename, `roles` as an array of sprite data-URI entries, `executorBlocks` as a Scratch block map, and `executorTargetIndex: 1` for the Stage target.

The two initial packages are safe, metadata-only starter manifests: they intentionally contain no role scripts or executor blocks, so they do not start code from a green flag. Add runtime behavior only after the package manager can provision and dispatch a dedicated per-process global variable through the shared startup gate.
