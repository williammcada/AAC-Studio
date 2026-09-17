# Project Brief — AAC Studio

**Brief version:** 0.2 — audited documentation revision  
**Owner:** William McAda · **Credit:** A WILLIAM MCADA PRODUCT  
**Status:** Revised record for owner review; not an application release or fresh feature approval.  
**Repository destination:** williammcada/AAC-Studio (verify existence/current branch before source edits).  
**Current running version:** Not independently verified in this documentation task.  
**Source/baseline:** Recorded latest target is v0.4; exact source must be matched to AAC_Studio_V0.4_Consolidated_Repair_Specification.md. Earlier v0.2 superseded a 1.2.1 label: filename ordering alone is unsafe.  
**Next work:** Recover latest Studio HTML and preserve consolidated repair scope before further generation.

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

## 2. This task and boundaries

This revision repairs documentation only. It does not implement features, run application tests, upload source, deploy a site, or alter a repository. Retain the exact current source before implementation. Historical reported functionality is a preservation checklist to reconcile against that source, not permission to recreate the program from prose.

## 3. Standards and adoption

[Canonical handbook](https://github.com/williammcada/mcada-project-handbook). File blob revisions consulted: AI-START-HERE.md 6557a45aaa6d29d7d1abde808e6d0ac248b08820; UNIVERSAL-RULES.md aed6fe311aa2e88983f862a30a2d8f05d2ffc04d; CONDITIONAL-STANDARDS.md dad2d3a05ca0f18260196ea51ac6351bffffdc1c; PROJECT-TEMPLATE.md 574f4c6fcf19ecc2f9e27582fd856fb08123e8da. These are file blobs, not repository commit SHAs.

Relevant rules: U-01 identity, U-02 help, U-03 input validation, U-04 unambiguous math/text where applicable, U-05 reader/device, U-06 preservation, U-07 verification, U-08 local scope. Conditional selection: S-01, S-02, S-04.
Baseline adoption: selected for this documentation task within existing user instructions. Handbook still labels shared scope/modules seeded/draft; no new global rule ratification is inferred. Project-specific approved decisions control their own scope.

## 4. Must-retain behavior

The detailed scope above is the feature-preservation inventory. Preserve existing settings, data, accepted content, assets, exports and compatibility confirmed in source. Distinguish implemented behavior, accepted pending changes and historical requests during intake. A missing entry in this brief is not authorization to remove working behavior. Preserve valid user work during migrations and failures.

## 5. Source, release and deployment discipline

Recorded latest target is v0.4; exact source must be matched to AAC_Studio_V0.4_Consolidated_Repair_Specification.md. Earlier v0.2 superseded a 1.2.1 label: filename ordering alone is unsafe.

Record exact selected source filename/hash and repository commit when importing it; record live URL/version only after actually opening it. Unknown commit does not mean the product is unbuilt.

DESIGN → CHANGE SPEC → IMPLEMENT → CHECKPOINT → VERIFY → VERIFIED CHECKPOINT → RELEASE → DEPLOY.

Use “implementation checkpoint” or “release candidate” before verification. Preserve candidate bytes and logs before packaging; recover that checkpoint after a ZIP/upload failure. Do not rebuild a verified implementation to fix delivery. Repository upload and website deployment are different operations; existing automatic deployments may run when main changes.

## 6. Known issues, conflicts and open evidence

Known historical source discrepancies and 45-finding repair tracking need reconciliation with v0.4, not assumption they are all resolved. Consolidated specification is required; this brief is not its replacement.

| Conflict or risk | Required handling |
| --- | --- |
| Historical claim versus current source | Inspect exact source; keep historical claim labeled until verified. |
| Proposed next scope versus working baseline | Use the approved version-specific specification; do not silently promote proposals. |
| Other project rules | Do not import AAC quotas, other-game retry counts, or a shared backend without explicit scope. |
| Handbook proposals | No additional exception or proposal is adopted by this brief. |

## 7. Verification contract

Validate all 24 forms, immutable finals, effective-record/hash agreement, invalid/mismatched import recovery and production gates; render representative fractions/figures and teacher/student exports.

| Evidence required | Result in this task |
| --- | --- |
| Exact source candidate/commit identified and preserved | Not run — documentation revision only |
| Project-specific checks above, with inputs and expected/actual results | Not run |
| Save/import/export and malformed-input regression | Not run |
| Intended devices and real deployment path, where applicable | Not run |
| Version, release notes and delivered bytes agree | Not run |

The next build report must name the candidate, environment and test results; historical reports of passing tests do not transfer to a changed candidate.

## 8. Handoff and provenance

Required project records: AAC_Studio_V0.4_Consolidated_Repair_Specification.md; latest Studio HTML; locked finals, catalogs, packets, repair manifests and blueprint history.

Provenance: previous migration brief and project-history audit in this conversation; directly read dossier/proposal where explicitly stated above. Records not explicitly marked read here are retrieval targets, not claims of fresh inspection. No current app code was tested for this brief.

Before substantive implementation retrieve these records, the current source, approved change spec and applicable handbook. If an indispensable spec is inaccessible, report the gap instead of filling it with invented details. Do not delete unique historical chats/assets until their contents are independently preserved.

## 9. Ecosystem boundary

Shared principles do not establish shared code, accounts or interfaces. MathQuest is engagement, TestForge assessment design, GradePal learner-level evidence, and DataDiver institutional analytics. Integration remains separately specified unless confirmed in source. Other projects remain independent unless their brief explicitly says otherwise.

