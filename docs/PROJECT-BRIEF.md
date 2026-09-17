# Project Brief — AAC Studio

**Brief status:** Migration baseline / requires source verification where noted  
**Brief version:** 0.1  
**Last updated:** 18 September 2026  
**Owner:** William McAda  
**Product credit:** A WILLIAM MCADA PRODUCT  
**Handbook repository:** `williammcada/mcada-project-handbook`  
**Handbook baseline:** `6557a45aaa6d29d7d1abde808e6d0ac248b08820 (AI-START-HERE.md); UNIVERSAL-RULES.md @ aed6fe311aa2e88983f862a30a2d8f05d2ffc04d`  
**Repository:** `williammcada/AAC-Studio`  
**Canonical source status:** Latest discussed target/build is AAC Studio v0.4; canonical source artifact is TO ESTABLISH from the latest known-good local build.  
**Current project state:** Active admissions-assessment authoring application with recent packet/error repair work.

## 1. Purpose and audience

AAC Studio supports the Grade 5–7 admissions-assessment program: eight interchangeable forms per grade, tightly controlled item formats and overlap, and AI-assisted generation/validation of assessment packets.

**Primary audience / operator:** Admissions/assessment staff producing Grades 5–7 mathematics admissions forms.

## 2. Standards selection

**Universal baseline:** U-01 through U-08 where applicable.

**Conditional modules:** S-01 External AI Generation and Structured Import; S-02 Curriculum/Assessment/Evidence; S-04 Distribution/Deployment

Apply only the selected modules and project-local requirements. Do not import restrictions from unrelated projects.

## 3. Project-specific requirements

- Eight interchangeable forms per grade.
- 15 one-point items per form.
- Mostly constructed response, with no more than two MCQ per form.
- No calculators.
- ELL-friendly wording and avoidance of unnecessary US-specific contexts.
- Numeric/symbolic/short-label/ordered-pair/MCQ response contracts as approved.
- AAC overlap/interchangeability rules remain AAC-specific and must not propagate to unrelated assessments.
- Round-trip packets must be technically strong enough for a high-end AI model to return without repeated manual repair loops.

## 4. Preserve from the current accepted project

- Admissions-specific interchangeability and overlap controls.
- Eight-form/15-item structure and approved response formats.
- Packet identity/revision validation.
- Error checking rather than accidental item generation when the workflow is in audit mode.

## 5. Relationship to other projects

- Shares S-01 round-trip principles with TestForge and LogicForge.
- AAC-specific form restrictions remain local and must not become TestForge weekly/benchmark defaults.

A conceptual relationship is not proof of an implemented integration. Do not invent a shared API, data schema, identity layer, or deployment dependency without an explicit integration task.

## 6. Source and version discipline

The exact current source artifact or repository commit must be identified before a substantive build. If the field above says the source is not yet established, first locate the latest known-good local file/ZIP or existing repository state and record its exact identity here.

For substantial revisions use:

**DESIGN → CHANGE SPEC → IMPLEMENT → CHECKPOINT → VERIFY → VERIFIED CHECKPOINT → RELEASE → DEPLOY (when applicable)**

A packaging/export/deployment failure must not force reconstruction of an already verified build.

## 7. Definition of done

| # | Requirement / check | Result | Evidence / limitation |
| ---: | --- | --- | --- |
| 1 | All eight forms satisfy the AAC structural contract. | Not run | |
| 2 | Overlap/interchangeability checks pass for the intended program rules. | Not run | |
| 3 | Valid generation packets round trip through external AI and reimport cleanly. | Not run | |
| 4 | Malformed/stale/mismatched packets fail with actionable errors. | Not run | |
| 5 | Item wording and representations remain ELL-friendly and calculator-free. | Not run | |

Allowed results: **Passed / Failed / Not run / Not applicable**. A "Passed" result requires an actual check against the identified candidate.

## 8. Known issues and migration notes

Before further v0.4 work, place the exact latest AAC Studio source and the consolidated repair specification in this repository.

## 9. Handoff files

A substantive AI implementation task should retrieve or receive:

1. `AI-START-HERE.md`;
2. `UNIVERSAL-RULES.md`;
3. the relevant sections of `CONDITIONAL-STANDARDS.md`;
4. this project brief;
5. the exact current source artifact/commit;
6. the approved version-specific change specification;
7. applicable assets and deployment configuration.

Do not reconstruct the current implementation from a historical chat summary when the actual source should be available.

## 10. Ownership

**William McAda**  
**A WILLIAM MCADA PRODUCT**
