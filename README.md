# AAC Studio v0.5.0

**A WILLIAM MCADA PRODUCT** · Blueprint 4.9.0 · exchange contract v5.

[Download AAC Studio v0.5](https://github.com/williammcada/AAC-Studio/raw/refs/heads/main/AAC_Studio_v0.5.html). Save the file and open it in Chrome or Edge. This repository contains the portable application and complete recoverable source. The separately hosted Site has not been redeployed by this revision.

## What changed

The complete [v0.4 iteration audit](docs/audits/AAC_v0.4_Iteration_Audit_Batches_1-3.md) now drives permanent repairs to the task catalog, allocation, generation packets and import validation. See the [v0.5 specification](docs/change-specs/v0.5-AUDIT-REPAIRS.md) and [verification record](docs/releases/0.5-release.md).

- Context labels and word budgets agree with required situations. Mathematical domains are tied to operations, with counts distinguished from sums and exact grouping distinguished from complete-group floor tasks.
- Rate answers omit units; units remain in the question. Decimal classification has its own claim. Required decimal, ratio, expression, equation and inequality forms have narrower validation.
- Comparison quotas derive from canonical task cores. One allocation changes: G6 V2 Q5 becomes INEQUALITY-DERIVE-FROM-TOTAL. All cyclic and paired exclusions are rechecked.
- A coordinate plane means one Cartesian axes panel, including proportional graphs. The graph MCQ uses four labeled curves on shared axes.
- Difficulty deviations, visual workload and educator-review requirements appear as nonblocking warnings. Supporting calculations no longer imply direct evidence of an entire external standard.
- Selected high-risk tasks carry numerical validation data. Import checks the declared values and answer; teachers still check that those values match the wording and figure.

There are 360 allocations and 124 claims. The additional claim separates decimal classification from decimal conversion; the approved Grade 7 mean-to-total prerequisite is retained.

## Daily workflow and existing work

1. Open an unlocked form and download a **fresh v0.5 generation packet**.
2. Give the complete packet to an AI and import its returned JSON or TXT result.
3. Check questions, figures, solutions and validation values. Accept each item, complete the whole-form review, and finalize.
4. Export the five-part Word package or use Print / Save PDF. Fractions use native editable Word equations.

Original-year Forms 1–3 remain locked. New assessment/test years permit all eight forms per grade. Finalized content is immutable. Existing v0.4 backups can be restored without rewriting their packets or accepted records. Earlier drafts remain available but require a fresh packet for new imports; do not relabel an old response as v0.5.

The offline application saves in IndexedDB. **Save HTML copy** carries current work into another standalone file; JSON backups preserve all assessment years. Detailed revision history stays in the browser that recorded it. Offline files do not automatically synchronize with the hosted Site.

## Source and verification

The v0.5 source snapshot is `AAC_Studio_v0.5_source.zip`. Extract it into a development directory. The previous `AAC_Studio_v0.4.html`, `AAC_Studio_v0.4_verified_source.zip`, v0.3 file and historical catalogs remain preserved.

The release candidate passed TypeScript checking, retained regression suites, 3,958 new audit-specific assertions, and all 24 isolated packet/import/review/finalization/backup workflows. All 24 Word packages were generated; representative fraction/graph/distribution pages were rendered and visually inspected. The HTML has no external dependencies and its embedded JavaScript passes syntax checking.

**Limit:** desktop browser interaction testing remains unverified because the runtime lacks Chromium and its download timed out. Microsoft Word desktop and physical printing were not tested. This is a tested release candidate, not a fully verified browser release. The [release record](docs/releases/0.5-release.md) identifies exact bytes and remaining checks.

In the extracted source:

```sh
pnpm install --frozen-lockfile
pnpm exec tsc --noEmit
node scripts/test-aac.mjs
node scripts/build-offline.mjs
```

`python scripts/repair-bank-v05.py` deterministically regenerates the active bank from preserved v0.4 inputs (NumPy/SciPy required). `python scripts/fixtures-v05.py` generates isolated test fixtures; these never become school assessments. Older compiler scripts are historical tools, not the v0.5 build entry point.

No AI API key or paid service is required for the portable application. Production remains a single-file offline workflow; the source also retains the previous hosted React/TypeScript application and persistence implementation.
