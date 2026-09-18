# Project Brief — AAC Studio

**Brief version:** 0.4 — verified release baseline  
**Owner:** William McAda · **Credit:** A WILLIAM MCADA PRODUCT  
**Status:** AAC Studio v0.4.0 is the official verified baseline.  
**Repository:** `williammcada/AAC-Studio`, branch `main`.  
**Current running version:** v0.4.0 at `https://aac-studio-wm.wsm05.chatgpt.site`, verified during the v0.4 release workflow.  
**Source/baseline:** Complete v0.4 source synchronized from verified source commit `638cb0166ab5db37f4fe2fdc4df8bd4b971a99d5`. Portable release: `AAC_Studio_v0.4.html`, SHA-256 `c191704b7467a65b654ea3d9ab2ae2af614096b0d2ecaad76877285c822ee634`. The final canonical GitHub commit is recorded in `docs/MIGRATION-BASELINE.md`.  
**Previous baseline:** `AAC_Studio_v0.3.html` at source checkpoint `76d9c85f634025b3d75970fc4d827b8467f54ba1`; retained as history, not the active source.  
**Next work:** Begin any v0.5 work from the v0.4 verified baseline and a versioned accepted change specification.  

## 1. Purpose, audience and detailed scope

- Offline admissions assessment authoring/review application, not merely a question list. Grades 5–7, eight interchangeable forms per grade, 15 one-point questions each: 24 forms/360 slots.
- Printed, no calculators, ELL-friendly; numeric/symbolic/short-label/ordered-pair/MCQ answers, at most two MCQs per form. Avoid unnecessary US-specific cultural context.
- Dashboard → Generate → Review & Import → Finalize & Export. Preserve original blueprint/source provenance, packet identity, audit views, backups/history, drafts and immutable finalized forms.
- Forms 1–3 were recorded as finalized/locked; preserve their accepted item identities and content. Forms 4–8 require production preflight; allocation readiness is not proof all 360 designs are generation-ready.
- Maintain immutable historical catalogs/packets and a separate active catalog. Earlier repairs distinguish 4.4/4.5 historical catalogs from active 4.6. One effective record must drive allocation, validation, comparison, packet content and hash.
- Accepted-item fingerprints override stale planned kernels in overlap comparisons. AAC-specific interchangeability, adjacency/overlap and response-grammar rules remain local.
- Use one centralized response grammar/math parser, exact schema/version/design identity, export gates and deterministic repairs with manifests. Diagnostic export may be allowed when production export is blocked.
- Preserve figures, correctly stacked fractions, DOCX output and PDF/print workflow. Validate scoring/answer keys and print layout separately from import structure.
- Audit/repair tasks do not authorize fresh student-item generation or changes to locked accepted forms.

## 2. This release and boundaries

V0.4 implements the accepted A01–A16 contract and bank repairs, preserves the original year and locked forms, and makes the verified source, portable artifact, test evidence and repair specification recoverable from the canonical repository. It does not claim that arbitrary future AI-generated items are mathematically correct or that educator review can be automated away.

## 3. Standards and adoption

[Canonical handbook](https://github.com/williammcada/mcada-project-handbook). File blob revisions consulted: AI-START-HERE.md 6557a45aaa6d29d7d1abde808e6d0ac248b08820; UNIVERSAL-RULES.md aed6fe311aa2e88983f862a30a2d8f05d2ffc04d; CONDITIONAL-STANDARDS.md dad2d3a05ca0f18260196ea51ac6351bffffdc1c; PROJECT-TEMPLATE.md 574f4c6fcf19ecc2f9e27582fd856fb08123e8da. These are file blobs, not repository commit SHAs.

Relevant rules: U-01 identity, U-02 help, U-03 input validation, U-04 unambiguous math/text where applicable, U-05 reader/device, U-06 preservation, U-07 verification, U-08 local scope. Conditional selection: S-01, S-02, S-04.
Baseline adoption: selected for this documentation task within existing user instructions. Handbook still labels shared scope/modules seeded/draft; no new global rule ratification is inferred. Project-specific approved decisions control their own scope.

## 4. Must-retain behavior

The detailed scope above is the feature-preservation inventory. Preserve existing settings, data, accepted content, assets, exports and compatibility confirmed in source. Distinguish implemented behavior, accepted pending changes and historical requests during intake. A missing entry in this brief is not authorization to remove working behavior. Preserve valid user work during migrations and failures.

## 5. Source, release and deployment discipline

Canonical active source: the complete recoverable source snapshot `AAC_Studio_v0.4_verified_source.zip`. Verified source provenance: `638cb0166ab5db37f4fe2fdc4df8bd4b971a99d5`. Canonical GitHub verified-release commit: `acf7945e7142a7df1cbd5a1ef54b7967513a6fc0`. Exact portable artifact: `AAC_Studio_v0.4.html`, SHA-256 `c191704b7467a65b654ea3d9ab2ae2af614096b0d2ecaad76877285c822ee634`.

See [`MIGRATION-BASELINE.md`](MIGRATION-BASELINE.md) for the authoritative source manifest and the checks actually performed.

DESIGN → CHANGE SPEC → IMPLEMENT → CHECKPOINT → VERIFY → VERIFIED CHECKPOINT → RELEASE → DEPLOY.

Use “implementation checkpoint” or “release candidate” before verification. Preserve candidate bytes and logs before packaging; recover that checkpoint after a ZIP/upload failure. Do not rebuild a verified implementation to fix delivery. Repository upload and website deployment are different operations.

## 6. Known issues, conflicts and open evidence

The consolidated A01–A16 implementation defects are repaired and regression-covered. The remaining limits are judgment boundaries, not hidden packet-contract defects: actual item mathematics, visual meaning, DOK, workload, redundancy and ELL accessibility still require educator review.

| Conflict or risk | Required handling |
| --- | --- |
| Historical claim versus current source | The v0.4 release record and migration baseline control current identity; earlier records remain historical. |
| Proposed next scope versus working baseline | Start from the v0.4 verified commit and use an approved version-specific specification. |
| Other project rules | Do not import AAC quotas, other-game retry counts, or a shared backend without explicit scope. |
| Handbook proposals | No additional exception or proposal is adopted by this brief. |

## 7. Verification contract

Validate all 24 forms, immutable finals, effective-record/hash agreement, invalid/mismatched import recovery and production gates; render representative fractions/figures and teacher/student exports.

| Evidence required | Result in this task |
| --- | --- |
| Exact source candidate/commit identified and preserved | Passed — full source, artifact hash and verified source provenance are recorded. |
| Project-specific checks above, with inputs and expected/actual results | Passed — all 24 G5–G7/V1–V8 forms and 360 allocation identities were exercised; see `docs/releases/0.4-release.md`. |
| Save/import/export and malformed-input regression | Passed — packet/import/review/finalization/Word/backup workflows plus invalid and stale cases. |
| Intended devices and real deployment path, where applicable | Passed with stated limits — Chrome preview and hosted v0.4 verified; Microsoft Word desktop and physical printing were not tested. |
| Version, release notes and delivered bytes agree | Passed — v0.4.0 / Blueprint 4.8.0 / contract v4 and the portable artifact hash agree. |

The next build report must name the candidate, environment and test results; historical reports of passing tests do not transfer to a changed candidate.

## 8. Handoff and provenance

Current source identity is recorded in [`MIGRATION-BASELINE.md`](MIGRATION-BASELINE.md). That manifest supersedes the v0.3-only baseline while preserving it as history.

Required project records: committed `AAC_Studio_v0.3.html`; committed `AAC_Studio_v0.4.html`; `AAC_Studio_V0.4_Consolidated_Repair_Specification.md`; complete source; release reports; locked finals, catalogs, packets, repair manifests and blueprint history.

Provenance: previous migration brief and project-history audit in this conversation; directly read dossier/proposal where explicitly stated above. Records not explicitly marked read here are retrieval targets, not claims of fresh inspection. No current app code was tested for this brief.

Before substantive implementation retrieve these records, the current source, approved change spec and applicable handbook. If an indispensable spec is inaccessible, report the gap instead of filling it with invented details. Do not delete unique historical chats/assets until their contents are independently preserved.

## 9. Ecosystem boundary

Shared principles do not establish shared code, accounts or interfaces. MathQuest is engagement, TestForge assessment design, GradePal learner-level evidence, and DataDiver institutional analytics. Integration remains separately specified unless confirmed in source. Other projects remain independent unless their brief explicitly says otherwise.
