# Migration Baseline — AAC Studio

**Recorded:** 18 September 2026  
**Repository:** `williammcada/AAC-Studio`  
**Branch:** `main`  
**Active release:** AAC Studio v0.4.0 · Blueprint 4.8.0 · `aac.contract.v4`  
**Record status:** Official verified source and portable-release baseline.

## Canonical source identity

| Field | Value |
| --- | --- |
| Canonical source | `AAC_Studio_v0.4_verified_source.zip` (complete source snapshot) |
| Source snapshot SHA-256 | `00af7e39d1571f5ec221757002b245f171d9b13206b4728fd6254df733d1628a` |
| Verified source provenance | Sites source commit `638cb0166ab5db37f4fe2fdc4df8bd4b971a99d5` |
| Portable release | `AAC_Studio_v0.4.html` |
| Portable release SHA-256 | `c191704b7467a65b654ea3d9ab2ae2af614096b0d2ecaad76877285c822ee634` |
| Canonical GitHub verified-release commit | `acf7945e7142a7df1cbd5a1ef54b7967513a6fc0` |
| Hosted release | `https://aac-studio-wm.wsm05.chatgpt.site` |

The previous v0.3 source baseline remains preserved as `AAC_Studio_v0.3.html` at checkpoint `76d9c85f634025b3d75970fc4d827b8467f54ba1`. It is historical and is not the current implementation baseline.

## Verification status

| Check | Result | Evidence / limitation |
| --- | --- | --- |
| Complete source and portable release preserved | Passed | Full recoverable source snapshot and the exact delivered HTML are committed together at `acf7945e7142a7df1cbd5a1ef54b7967513a6fc0`. |
| Release regression | Passed | 46 domain/workflow assertions, 1,711 v0.2 release assertions, 18,444 retained v0.3 bank/compatibility assertions, and 1,633 v0.4 assertions. |
| All 24 form workflows | Passed | Packet export, valid import, review, finalization, Word package and backup restoration for G5–G7/V1–V8. |
| Type and production build | Passed | TypeScript check and Vinext production build rerun from the synchronized canonical tree. |
| Offline artifact | Passed | Exact verified HTML preserved; build has zero external dependencies. |
| Hosted/running application | Passed | v0.4.0 / Blueprint 4.8.0 verified in Chrome at the hosted URL during release. |
| Microsoft Word desktop and physical printing | Not run | Representative packages were rendered and inspected with LibreOffice; this limitation remains explicit. |

## Documentation authority

- [`PROJECT-BRIEF.md`](PROJECT-BRIEF.md) records permanent project-local scope and verification requirements.
- [`change-specs/AAC_Studio_V0.4_Consolidated_Repair_Specification.md`](change-specs/AAC_Studio_V0.4_Consolidated_Repair_Specification.md) is the implemented v0.4 repair specification.
- [`releases/0.4-release.md`](releases/0.4-release.md) records changes, tests and limits.
- [`MIGRATION-NOTE.md`](MIGRATION-NOTE.md) and the v0.3 baseline remain historical context.

## Next gate

Begin v0.5 only from this verified baseline. Create and approve a versioned change specification before implementation; preserve an implementation checkpoint before extended testing; then record the exact verified candidate before release and deployment.

## V0.5 successor — 2026-09-18

This section supersedes the earlier active-source designation; earlier entries remain historical. Current deliverable: `AAC_Studio_v0.5.html`, Studio 0.5.0 / Blueprint 4.9.0 / contract v5. Complete source: `AAC_Studio_v0.5_source.zip`. Status: **tested release candidate**, not browser-verified release. Consult [the release record](releases/0.5-release.md) for exact hashes and evidence.

Baseline retrieved from canonical commit `c4c4acf57b73a1e10fe75b53b86e4c4a0cf3ea84`. The archived v0.4 source and portable file remain unchanged. The migration preserves Blueprint 4.8 as an immutable snapshot, adds explicit v0.4 backup restoration, and requires new packets for modified contracts. No hosted deployment occurred.
