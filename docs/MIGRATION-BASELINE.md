# Migration Baseline — AAC Studio

**Recorded:** 18 September 2026  
**Repository:** `williammcada/AAC-Studio`  
**Branch:** `main`  
**Source-preservation checkpoint:** `76d9c85f634025b3d75970fc4d827b8467f54ba1`  
**Record status:** Current source identity. This is not by itself a functional-test, release, or deployment claim.

## Canonical source identity

| Field | Value |
| --- | --- |
| Canonical source path | `AAC_Studio_v0.3.html` |
| Git blob SHA | `3bf9020d0e080c8188f93b787d4e970f26b2f264` |
| Version represented | v0.3 source baseline; v0.4 is not established as implemented |
| Repository source checkpoint | `76d9c85f634025b3d75970fc4d827b8467f54ba1` |

The checkpoint above identifies the application/planning source immediately before this normalization record was committed. Later documentation-only commits do not change the preserved application bytes.

## Verification status

| Check | Result | Evidence / limitation |
| --- | --- | --- |
| Source exists in the default branch | Passed | Repository paths and Git object identities were read directly on 18 September 2026. |
| Byte-preservation comparison | Passed | Passed — the Git blob matched the preserved Library `AAC_Studio_v0.3.html` during the 18 September 2026 audit. |
| Functional workflow | Not run | Source preservation does not establish that imports, gameplay, reports, storage or exports work. |
| Hosted/running application | Not run | Not verified; this normalization did not run or deploy the application. |

## Documentation authority

- [`PROJECT-BRIEF.md`](PROJECT-BRIEF.md) records purpose, scope, must-retain behavior and verification requirements.
- [`change-specs/INDEX.md`](change-specs/INDEX.md) identifies approved or directional change records.
- [`MIGRATION-NOTE.md`](MIGRATION-NOTE.md) is retained as historical migration context but its pre-upload source-status language is superseded by this baseline.
- This file controls current source identity when an older brief or note says the source was unknown or “TO ESTABLISH.”

## Next gate

Use the committed v0.3 source as the preservation baseline. Reconcile any future v0.4 implementation against the approved v0.4 specification before changing the app.

Do not label a future commit a verified release until the exact candidate has passed the project brief’s required verification and that evidence is preserved.
