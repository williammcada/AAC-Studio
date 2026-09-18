# AAC Studio v0.4 — cumulative iteration audit

Status: All 24 full packets reviewed; 360 assigned contracts across G5–G7 V1–V8. G7 V4 coverage gap closed by the supplemental audit below. Repairs remain open.
Date: 18 September 2026.
Baseline declared by the supplied packets: Studio 0.4.0, Blueprint 4.8.0.
Assessment year: TEST YEAR (`aac-ebcc5f10-919e-4cad-993a-b0d75d2226d8`).

## Scope and conclusion

Current cumulative scope: **360 full assigned contracts from all 24 packets**, covering G5–G7 V1–V8. The supplemental G7 V4 audit closes the previous source gap. The register contains 18 issue categories: B1-01–10, B2-01–05 and B3-01–03; these include confirmed inconsistencies, risks and advisory concerns, not 18 proven runtime failures. Recurrences are consolidated under existing IDs. Earlier batch sections retain their original coverage statements as an audit history; the supplemental closure section supersedes statements that V4 is missing or unverified.

The main systemic priorities are consistent semantic quota classification, response-product/domain alignment, context and standard alignment, and task-specific validity rules. Applying the comparison classification already used in G6 V4/V6 makes G6 V2 exceed the comparison ceiling. Unit-bearing numeric answer requirements recur across grades. All checked source/excerpt records agree and no exact fingerprint collisions were found; those structural passes do not establish semantic clearance or release readiness. The final consolidated repair priorities and remaining coverage gap appear at the end of this record. No application or GitHub changes were made.

### Batch 1 conclusion

Reviewed all 120 assigned contracts in Grade 5 V1–V8, their embedded cyclic and paired-grade exclusions, generation instructions, machine schemas, conflict envelopes and response skeletons. This is a packet audit, not item generation or acceptance. No application, bank, historical form, GitHub repository or deployment was changed. IDs below remain stable for consolidation with the next two batches.

The packets are structurally consistent, but not semantically clean. Record four confirmed contract/documentation defects (B1-01–04), four generation/validation risks (B1-05–08), and two nonblocking quality concerns (B1-09–10). These are issue categories, not ten broken forms. No mathematically impossible Grade 5 assignment has been established by this audit; several assignments need clarification to avoid divergent implementations.

All eight packets report `PREFLIGHT FINDINGS []`. That result supports only the checks actually performed by Studio; it should not be presented as full semantic clearance.

## Batch 1 checks that passed

- Every form contains 15 assigned rows, questions 1–15, 30 cyclic adjacent rows and 15 paired Grade 6 rows.
- Cyclic exclusions match the supplied neighboring Grade 5 assignments field-for-field, including V8↔V1. No stale exclusion records were detected.
- No exact `comparisonSignature` collisions within a form, against either adjacent form, or against its embedded paired-grade list.
- All 120 proposed Surface Form IDs are unique; all 120 proposed Template IDs are unique in this batch and satisfy the exported identifier syntax/length limits.
- Skeleton question hashes, family IDs and proposed IDs agree with assignments. Result/conflict identity envelopes agree; eight distinct packet IDs were found.
- All forms have six DOK-1 and nine DOK-2 assignments. This verifies allocation counts, not cognitive validity.
- Allocated comparison counts, expression-answer counts, large-visual placement and combined G5/G6 coordinate-plane counts meet the stated ceilings, using the paired records embedded here.
- Required/prohibited visual metadata agrees with representation metadata. Six visuals in V6 is not itself a breach: only two are marked Large Visual.
- All Grade 5 rows are short answer. Zero MCQs satisfies a maximum of two; it is not an error simply because earlier forms used MCQs.

Exact signature agreement does not prove complete semantic nonredundancy. No additional definite adjacent-core collision was established from the present contracts. Fresh G6 packets are needed to verify the paired excerpts against their actual source packets.

| Form | Required visuals | Large visuals | Comparisons | Comparison calculations | Expression answers | Easy / Medium / Hard |
|---|---:|---:|---:|---:|---:|---|
| V1 | 2 | 2 | 2 | 0 | 0 | 0 / 15 / 0 |
| V2 | 3 | 2 | 2 | 0 | 0 | 1 / 13 / 1 |
| V3 | 2 | 1 | 2 | 0 | 0 | 0 / 15 / 0 |
| V4 | 4 | 1 | 2 | 1 | 0 | 1 / 13 / 1 |
| V5 | 4 | 2 | 2 | 0 | 0 | 1 / 14 / 0 |
| V6 | 6 | 2 | 2 | 0 | 1 | 1 / 14 / 0 |
| V7 | 2 | 1 | 2 | 0 | 0 | 1 / 14 / 0 |
| V8 | 4 | 2 | 2 | 0 | 0 | 1 / 13 / 1 |

## Batch 1 repair register

### B1-01 — Context classifications do not match binding task descriptions

**Confirmed metadata inconsistency; high priority.**

Explicit neutral situations are assigned `context: Pure mathematics` and a 20-word limit:

- V1 Q11 and V7 Q9, ADD-MISSING-PART: given requires a “concise neutral joining situation.”
- V2 Q9, SUBTRACT-TWICE: given explicitly requires a neutral context.
- V3 Q5, SUBTRACT-THEN-MULTIPLY: given explicitly requires a short neutral context.
- V3 Q8, CONVERT-TOTAL: given explicitly requires a short neutral situation.
- V3 Q10, ADD-TWO: requires a short joining situation.

Related claim/context mismatches: V1 Q14/V7 Q13 explicitly claim real-world multiplication; V3 Q11/V5 Q11/V7 Q10 explicitly claim real-world division, but all are Pure mathematics. V5 Q4/V8 Q3 claim fraction word problems. Their generation contracts need a consistent decision about context.

The reference paragraph says Pure mathematics *permits* prompts without a story; it does not expressly forbid every story. Therefore this is not a proof that every affected item is impossible. It is a genuine source-of-truth inconsistency that makes language budgeting and claim coverage unreliable.

**Repair:** derive context and word limit from the approved task contract. Neutral situations should receive Neutral context and 45 words; retain actual real-world requirements where the claim requires them. Do not mechanically relabel every measurement or geometric question as a story.

**Acceptance test:** reject explicit neutral-story requirements paired with Pure mathematics; verify the exported context and word limit agree after bank migration. Recheck all grades, not just these rows.

The real-world emphasis is supported by the official [Grade 5 fraction standards](https://www.thecorestandards.org/Math/Content/5/NF/), particularly 5.NF.A.2, 5.NF.B.6 and 5.NF.B.7.c.

### B1-02 — Grouping contract both supplies and appears to derive the total

**Confirmed given/unknown ambiguity; high priority.**

V2 Q4, V5 Q5 and V7 Q4, WHOLE-QUOTIENT-ROW-GROUPS, begin with “A multidigit whole-number total and a two-digit group size,” then supply row count and items per row. Their canonical core is MULTIPLY-THEN-DIVIDE.

If the total is supplied directly, multiplication is unnecessary and the task can collapse into ordinary division. If it is not supplied, the opening description is misleading. These rows also request a count of complete groups but declare Unitless rather than Count and provide no explicit exact-divisibility rule.

**Repair:** state that only row count, objects per row and new group size are supplied; the total is unknown. Require positive integer givens and an exact integer quotient, or explicitly authorize floor/remainder interpretation as a different contract. Use Count as the response domain.

**Acceptance test:** a directly supplied total fails this core; nondivisible values fail unless an explicitly approved remainder policy applies. Reject noninteger group counts.

### B1-03 — Domain rules are attached by answer type instead of mathematical operation

**Confirmed irrelevant binding text; medium priority.**

V2 Q15, QUAD-COUNT-CLASSES, and V5 Q9, PLOT-FREQUENCY, inherit requirements for positive “divisor/group/portion sizes” and “exactly divisible quantities,” although neither task divides quantities. V3 Q5 similarly receives division boilerplate for a fraction-of-a-collection task; the intended integer-product constraint should be stated directly.

These clauses also occur in embedded Grade 6 counting records; confirm their source contracts in batch 2. Treat absent divisors as not applicable rather than inventing them.

**Repair:** separate result-domain constraints from operation-specific preconditions. A counting task needs a nonnegative integer result and the appropriate count range, not generic division rules.

**Acceptance test:** frequency/class/term counts contain no division requirements; actual portion-division tasks retain positive denominators and exact-count guards.

### B1-04 — A residual internal-method prohibition remains

**Confirmed instruction inconsistency; medium priority.**

V8 Q8, EXPRESSION-RELATION, says “do not evaluate either,” while asking for a numerical multiplicative factor. This controls the student's internal method, unlike V6 Q8 where an unevaluated expression is the required output product.

**Repair:** require the factor only and describe the relationship being assessed; remove the ban on evaluating internally. Preserve unevaluated-output requirements for genuine expression-answer tasks.

**Acceptance test:** distinguish forbidden internal-method language from valid response-format constraints rather than deleting all occurrences of “evaluate.”

### B1-05 — Task-specific domains and grade boundaries remain incomplete

**Confirmed omissions; generation risk, not proof of an invalid item. High priority.**

Examples:

- V1 Q3/V6 Q4, derived rectangle width: explicitly require positive length L and reduction d with 0 < d < L. `domainRules` is empty.
- V2 Q13/V7 Q12, composite missing volume: ensure total volume exceeds the known component and the diagram describes feasible nonoverlapping prisms. Positive dimensions and appropriate whole-number edge constraints are not explicit.
- V2 Q7/V6 Q9, PLOT-TOTAL: require measurement increments in halves, fourths or eighths. Unlike PLOT-FREQUENCY, these givens merely say “fractional.”
- V2 Q4/V5 Q5/V7 Q4 and V3 Q3/V8 Q2: bound whole-number dividends to the assigned standard's intended range rather than only “multidigit.”
- V1 Q10, decimal division: the claim limits decimals to hundredths, but the given/domain fields should carry the same operand precision explicitly.

**Repair:** serialize positive geometric domains, operand ranges, precision and permitted denominators from canonical task definitions. Do not rely solely on a standard code, a generic scope label or generator common sense.

**Acceptance test:** reject negative/zero inferred dimensions, unsupported plot increments and out-of-bound operands before acceptance. Positive/negative fixtures must test both packet wording and item validation where machine-checkable.

For line-plot increments and whole-number-edge prism expectations, see the official [Grade 5 measurement standards](https://www.thecorestandards.org/Math/Content/5/MD/).

### B1-06 — Numeric candidate-selection tasks lack an explicit delivery convention

**Contract ambiguity; medium priority. Not a demonstrated MCQ-cap violation.**

SCALING-SELECT-FACTOR (V1 Q7, V3 Q6, V7 Q5), ESTIMATE-SUM (V3 Q4, V5 Q3), and ESTIMATE-REASONABLE (V6 Q11, V8 Q10) require supplied candidates but use shortAnswer. The skeleton includes `choices`, while the general rules discuss four-option A–D MCQs. The packet does not clearly tell the generator where candidates belong for these numeric-response tasks.

**Repair:** explicitly allow a numeric candidate bank in the stem with `choices: []` and a numeric answer, or reallocate as MCQ if that is the intended policy. Do not change modes silently. Define how these tasks count for response-mode and comparison limits.

**Acceptance test:** round-trip an approved candidate-bank fixture; reject A–D answers on numeric-response rows and reject populated MCQ choices if shortAnswer forbids them. Check the 20-word budget including any candidate-bank text.

### B1-07 — Exported answer grammar is broader than some task products

**Confirmed documentation breadth; validator behavior untested. Medium priority.**

- V2 Q1/V7 Q1 claim comparison using <, > or =, but `answerGrammar` also advertises ≤ and ≥. A non-strict symbol can be true without being the intended comparison classification.
- V6 Q8 requires a numerical expression, but its generic grammar advertises defined variables. No variable is supplied by this task.
- Count grammars begin “One nonnegative integer” and then list general number encodings, including rational multiples of pi and radicals. Some such expressions could evaluate to integers; the distinction between encoding and value-domain validation should be explicit.

**Repair:** export task-specific restrictions separately from general parser capabilities. Tighten comparison-symbol enums, require variable-free numerical expressions for this task, and state that every count encoding must evaluate to an integer.

**Acceptance test:** parser acceptance alone cannot establish task compliance; test each narrowed task grammar and its accepted equivalents. This audit does not establish that Studio currently accepts the invalid examples.

### B1-08 — Fraction-label instructions need a tested visual recipe

**Integration risk; medium priority. No export failure reproduced.**

Required fraction plots/models coexist with the rule that fractional labels must be native Word equations outside SVG/raster images. This can work with lettered tick marks and a linked equation key, but packets provide no concrete supported layout convention. V2 Q7, V5 Q9 and V6 Q9 are useful regression fixtures.

**Repair:** document and test a linked-label convention that preserves actual fractional measurement information, necessary visual evidence, readable ordering and accessible alternatives. Do not permit slash fractions in diagrams as a workaround.

**Acceptance test:** import and export a fractional line plot with equation labels; inspect rendered Word/PDF output and confirm labels, tick mapping and word counting. Do not describe this as tested until actually run.

### B1-09 — DOK allocations need task-level evidence, not just exact counts

**Pedagogical review concern; medium priority. Not an automatic downgrade.**

All forms meet 6 DOK-1 / 9 DOK-2 numerically. Review V1 Q5 (combine then share), V1 Q6/V5 Q7 (routine scaling comparison), V1 Q8/V7 Q6 (generate terms then subtract), and V1 Q15/V4 Q15 (subcategory from one familiar property). Their descriptions do not by themselves guarantee DOK 2; adding arithmetic steps or a story is insufficient under the packet's own rule.

**Repair:** record task-specific cognitive evidence, have an educator classify the repaired tasks, then reallocate if necessary. Never manufacture extra constraints simply to preserve a quota. Retest exclusions after any replacement.

### B1-10 — Difficulty and visual workload remain unbalanced

**Nonblocking planning concern.**

The stated 3 easy / 9 medium / 3 hard planning target is not met by any form; V1 and V3 are entirely Medium. V6 has six required visuals, versus two in V1/V3/V7. These are not failures of the current hard limits. Nevertheless, the export should disclose target deviations as advisory information rather than leaving an undifferentiated empty preflight list.

**Repair:** distinguish blocking errors, advisory deviations and unverified teacher-review dimensions. Track visual footprint and realistic workload without relabeling everything to force the target.

## Gates recorded after batch 1

1. Add the next two batches to this document; retain these issue IDs and distinguish recurrence from new causes.
2. Compare incoming Grade 6 source contracts against the paired excerpts recorded here. In particular, review TEST-EQUATION-AND-INEQUALITY's requirement for two equation solutions; assess it against its actual standard and allowed equation family before declaring it unworkable.
3. Review the full G5–G7 V1–V8 matrix after repairs, including all cyclic and paired exclusions. Do not repair individual packets in isolation.
4. Add deterministic contract tests for B1-01–07 and rendered integration tests for B1-08. Retain human cognitive/workload review for B1-09–10.
5. No new release number, application repair, import, finalization or GitHub action is authorized by this audit.

## Evidence manifest

Files were read from the supplied attachments, not inferred from earlier versions. Q references above identify assigned rows; their repeated exclusion copies are corroboration, not additional affected items.

| Form | Exact attachment | SHA-256 |
|---|---|---|
| V1 | AAC_TEST-YEAR_G5_V1_Generation_Packet(1).txt | e1d78afbf460d1e15d20d4cbf63de9f6805b8711ef6c1a16fa7ccb4037d7dac5 |
| V2 | AAC_TEST-YEAR_G5_V2_Generation_Packet(2).txt | f629c80eda78ffc54bc088e8acd260a15ea84ff1f8a55ddba9e553ec19efd455 |
| V3 | AAC_TEST-YEAR_G5_V3_Generation_Packet(1).txt | f4c6c85dfb9dc03880b06a6f5d28a39c3cb7428f192cc3426b0b8bb8267d3954 |
| V4 | AAC_TEST-YEAR_G5_V4_Generation_Packet(1).txt | 41462b9516ce8afc6049d60743ae59f8d16ef17da65bd9842520a3a6250474f8 |
| V5 | AAC_TEST-YEAR_G5_V5_Generation_Packet(1).txt | ed9d88e1ef84fe9162f9d42783f760559a4575586bd054f42c6f9b65e44f5acd |
| V6 | AAC_TEST-YEAR_G5_V6_Generation_Packet(1).txt | ca1af741e7eb59af6bb40640da38271f31dc2a4b1fb871005239a4727d9e4382 |
| V7 | AAC_TEST-YEAR_G5_V7_Generation_Packet(1).txt | e2f1a59f1baf283680704e83dae0676735246cd0f60a883e8ddfa74f6f32142e |
| V8 | AAC_TEST-YEAR_G5_V8_Generation_Packet(1).txt | f2f5a1c9c5554a251674a7b10de9d61423cf6a1ad478de717199a3f5f7b02598 |

Limitations: no student items authored; no importer, renderer, browser, application source or live release exercised. Standard checks used the official sources linked above. Content judgments are distinguished from mechanically verified packet consistency. Full standard coverage, cross-grade source synchronization and release readiness remain open until the other batches and appropriate implementation tests are complete.

---

## Batch 2 — Grade 6 V1–V8

Reviewed 120 additional assigned contracts from the eight attached Grade 6 packets. All declare Studio 0.4.0 / Blueprint 4.8.0, the same TEST YEAR ID as batch 1, and empty preflight findings. The filename suffixes differ from batch 1's embedded references, but the compared content is synchronized; suffixes alone are not a version mismatch.

### Verified packet consistency

- Every G6 packet contains 15 assigned rows, 30 cyclic exclusions, **30 paired-grade exclusions** (15 G5 and 15 G7), and 15 skeleton items. G6's 30 paired exclusions are correct; G5 had 15.
- All 240 G6 cyclic excerpt records match their supplied G6 source assignments field-for-field, including V8↔V1.
- All 120 G6 rows embedded in the G5 packets match these G6 sources. All 120 G5 rows embedded in these G6 packets match batch 1. Together with the 240 G5 cyclic records already checked, this is 720 matching source/excerpt comparisons across the two batches.
- No exact canonical-fingerprint collisions were found within a G6 form, across its adjacent forms, or against its embedded G5/G7 exclusions. The G7 source packets are still needed to verify the 120 G7 excerpt records.
- Across both batches, 240 Surface Form IDs and 240 proposed Template IDs are unique and within exported syntax/length limits; 16 packet IDs are distinct. Skeleton IDs, family IDs and specification hashes match the assignments. Result/conflict identity fields agree.
- Required/prohibited visual policy and representation fields agree. Large visuals occupy allowed positions. G6 uses no coordinate-plane visual, so the combined G5/G6 plane ceiling is met.
- Every G6 form has six DOK-1 and nine DOK-2 assignments and one expression-answer item. Statistics vocabulary/selection rows use MCQ; numeric statistics rows use short answer. Allocated MCQs never exceed two.
- Raw comparison booleans satisfy the limits, but **those booleans are inconsistent for one shared core**. This is not a semantic quota pass; see B2-02.

| G6 form | Required visuals | Large visuals | Recorded comparisons | Comparison calculations | MCQs | Easy / Medium / Hard |
|---|---:|---:|---:|---:|---:|---|
| V1 | 4 | 2 | 1 | 1 | 2 | 1 / 14 / 0 |
| V2 | 3 | 0 | 2* | 1 | 0 | 0 / 15 / 0 |
| V3 | 6 | 2 | 1 | 1 | 1 | 1 / 13 / 1 |
| V4 | 4 | 2 | 2 | 0 | 1 | 1 / 13 / 1 |
| V5 | 4 | 2 | 2 | 1 | 2 | 1 / 14 / 0 |
| V6 | 5 | 2 | 1 | 0 | 1 | 1 / 14 / 0 |
| V7 | 5 | 2 | 2 | 1 | 1 | 1 / 14 / 0 |
| V8 | 3 | 1 | 2 | 1 | 2 | 2 / 13 / 0 |

*V2 becomes three comparisons if the canonical classification already used in V4/V6 is applied consistently.

### New findings

#### B2-01 — Rate contracts require units in an answer that forbids units

**Confirmed response-contract conflict; high priority.**

Affected: G6 V2 Q6, V5 Q7, V8 Q6; UNIT-RATE-DIFFERENCE.

`requiredResult` asks for the difference “with compound units,” and the binding boundary explicitly says to return that result with compound units. However, `answerObject` is Number, `responseProduct` is one number in the Rate domain, and both the permanent rules and `answerGrammar` require unit words in the prompt, not the answer. These are not unit-identification tasks.

The task is mathematically feasible; its serialized instructions disagree about the exact response. A generator should not have to decide which binding instruction to override.

**Repair:** retain the Rate quantity dimension, but change the response requirement to the numerical difference in the unit specified by the stem. Put compound units in the stem, never in `answer` or numerical accepted equivalents. Also specify whether the result is the nonnegative difference or an explicitly ordered subtraction. “Difference” alone does not choose between those conventions.

**Acceptance tests:** export all three contracts and assert that no numeric-answer instruction demands attached units; reject a unit-bearing numerical answer while accepting the correct unit-free number. Test both rate orderings under the chosen difference convention. These are proposed tests, not tests run in this packet audit.

#### B2-02 — One shared core has inconsistent comparison classification

**Confirmed bank-metadata inconsistency with a quota consequence; high priority.**

| Row | Structure code | Canonical comparison signature | `comparison` |
|---|---|---|---|
| G6 V2 Q5 | TEST-TWO-CONDITIONS | TEST-EQUATION-AND-INEQUALITY | false |
| G6 V4 Q6 | TEST-EQUATION-AND-INEQUALITY | TEST-EQUATION-AND-INEQUALITY | true |
| G6 V6 Q7 | TEST-EQUATION-AND-INEQUALITY | TEST-EQUATION-AND-INEQUALITY | true |

All three contracts require selecting a candidate satisfying an equation and an inequality, with two candidates satisfying the equation and exactly one surviving the inequality. Their underlying action and given/unknown structure do not justify different comparison counts.

G6 V2 already marks Q6 UNIT-RATE-DIFFERENCE and Q13 ABS-CONSTRAINED-NUMBER as comparisons. Counting Q5 as V4/V6 do yields **three**, against the maximum of two. `PREFLIGHT FINDINGS []` misses this because the inconsistent boolean keeps the recorded total at two.

**Repair:** define comparison classification once for each semantic task core and derive row flags and quota totals from it. If the current V4/V6 classification is retained, reallocate a V2 task and rerun every exclusion check. If policy instead excludes this type, document and apply that policy everywhere; do not choose classifications per form to make its counts pass.

**Acceptance tests:** aliases with the same action/core must have the same quota semantics. A V2 fixture using the current canonical true classification must report three comparisons and block clean preflight. Any replacement must pass cyclic V1/V3 and paired G5/G7 exclusions.

#### B2-03 — Standard mapping is broader than the assessed task in a repaired statistics row

**Confirmed task/standard alignment gap; high priority for coverage claims.**

G6 V4 Q13 is mapped to **6.SP.B.4**, but its required representation is a frequency table (Statistical Organizer), its only action is calculating one missing frequency, and its only response is that number. It neither constructs nor selects a plot on a number line. The current broad claim, “Read, complete, or select a numerical data display,” obscures that difference. A frequency table can support later plotting, but this task alone is not direct evidence of the plotting action in the assigned standard.

**Repair:** approve either a standard/claim mapping that actually reflects frequency reasoning, or a revised task that directly assesses the intended plotting construct while preserving objective responses. Do not merely switch the visual tag to Statistical Graph while still rendering a table. Preserve a record of supporting versus directly assessed standards, and rerun coverage and overlap checks after any reassignment.

Related mapping review: V5 Q12's median calculation is assigned 6.SP.A.2; V7 Q12's median calculation is assigned 6.SP.A.3. These conceptual standards concern distributions and what measures summarize; 6.SP.B.5.c is the more direct quantitative-center reference. These are mapping-review flags, not declarations that median calculation is outside Grade 6.

Also normalize the exported substandard spelling: V2 Q9, V6 Q9 and V8 Q8 use `6.SP.B.5c`; the official identifier is `6.SP.B.5.c`. The intent is clear, so this is not a mathematical error. Add an explicit alias if the importer accepts both; do not assume downstream standard lookups do.

**Acceptance tests:** an approved standard-action matrix prevents a table-only missing-frequency task from satisfying direct plotting coverage. Standard aliases round-trip to one canonical ID without losing claims or allocations.

Source: official [Grade 6 Statistics & Probability standards](https://www.thecorestandards.org/Math/Content/6/SP/). The mapping assessment above is an audit judgment based on those standards and the actual task fields.

#### B2-04 — Two-solution candidate task is feasible, but needs explicit complexity limits

**Generation risk; medium priority. Resolves the open batch-1 question.**

Affected: G6 V2 Q5, V4 Q6, V6 Q7.

Do **not** mark these tasks mathematically impossible solely because two nonnegative candidates satisfy the equation. A nontrivial one-step linear equation cannot have two distinct solutions, but these rows are assigned 6.EE.B.5, which permits evaluating supplied candidates by substitution. A suitably bounded equation with a nonlinear expression can have two qualifying candidates without requiring a student to solve a quadratic symbolically.

The missing specification is the approved equation family and workload. Current wording could produce anything from accessible substitution to an unnecessarily advanced expression. An identity can also make the equation redundant if every supplied candidate satisfies it. Nonnegative candidates are specified, but their distinctness and a candidate that fails the equation are not explicit in every version.

**Repair:** define manageable supported operations, numerical ranges and candidate count; require distinct candidates, exactly two equation matches, at least one equation nonmatch, and one joint match. State that the equation is nontrivial. Keep the response numerical and do not impose a student method. Implement the candidate-delivery convention from B1-06.

**Acceptance tests:** verify both truth sets and their one-element intersection; reject identity/no-filter cases and unsupported complexity. Do not introduce an unnecessary one-step-linear restriction that would make the two-solution requirement impossible.

Source: official [Grade 6 Expressions & Equations standards](https://www.thecorestandards.org/Math/Content/6/EE/), especially 6.EE.B.5. This is a feasibility analysis of the contract, not a student-facing item.

#### B2-05 — Median action still describes an unsorted input after changing to a dot plot

**Confirmed stale action metadata; medium priority.**

G6 V7 Q12: `action` says “Find the median of an unsorted data set,” while `given` requires six integer observations supplied as a necessary dot plot. A conventional dot plot locates observations on an ordered numerical scale; the original unsorted-list presentation no longer describes the assigned input. The structure code MEDIAN-SORTED-DATA is also a legacy name, but the name alone is not a mathematical failure. The canonical signature DISTRIBUTION-MEDIAN is already appropriate.

**Repair:** make the action “Find the median from a dot plot.” Keep the required graph and canonical core. If a display-oriented alias is introduced, migrate identifiers deliberately rather than changing issued IDs silently. Do not add an unsorted list that makes the required plot redundant just to satisfy stale wording.

**Acceptance test:** row action, given representation, boundary and teacher-review guidance describe the same task after a representation repair. Re-exported paired/adjacent excerpts must carry the revised action consistently.

### Recurrences and extensions of batch-1 findings

These remain under their original issue IDs rather than being counted again as new bugs.

| Existing ID | Grade 6 evidence and additional repair detail |
|---|---|
| B1-01 Context classification | **20 rows** explicitly require a neutral context/statement/situation while assigned Pure mathematics: V1 Q3/Q4/Q6/Q9; V2 Q3; V3 Q3/Q5; V4 Q3/Q4/Q5/Q15; V5 Q4/Q9/Q11; V6 Q4; V7 Q3/Q4/Q5; V8 Q3/Q11. Their 20-word limits follow the wrong context label. The semantic problem is the same as batch 1; Pure mathematics does not itself make a short story impossible. |
| B1-03 Irrelevant domain clauses | Division/exact-divisibility boilerplate recurs in V2 Q14 interval count, V4 Q13 missing frequency, V6 Q3/V8 Q2 term count, and V6 Q13 observation count. V4 Q1/V8 Q1 LCM also inherit portion-size language. V7 Q5 asks for a coefficient in a model but inherits “the unique solution is nonnegative”; specify which unknown that refers to instead of adding generic equation-solving conditions. |
| B1-04 Method restrictions | V1 Q15 says “calculate both rates before comparing,” despite the permanent prohibition on prescribed student methods. Specify the two given rate relationships and comparison output; do not require a particular internal sequence. Required unevaluated expression output and counting outermost terms in the expression as written are legitimate product definitions, not the same defect. |
| B1-05 Missing explicit domains | V4 Q1/V8 Q1 LCM still say “within the assigned standard boundary” without stating that each input is at most 12. V5 Q1's distributive-factor task omits the standard's 1–100 addend range. V2 Q3 needs a positive, nonzero percentage for a determined whole; V4 Q4/V8 Q3 need a valid used-percentage range. V3 Q15/V6 Q15/V8 Q15 need positive ratio-table reference quantities so the missing input is uniquely determined. These omissions permit bad choices; they do not establish that an actual generated item is invalid. |
| B1-05 Rate/geometric domains | V2 Q12/V5 Q10/V7 Q10 overall-rate tasks need compatible numerator/time units, positive durations and consecutive/nonoverlapping intervals before summing. V1 Q13/V6 Q12 need positive fractional edges and a positive extension. V7 Q13's existing triangle-inequality, perpendicular-altitude and matching-edge rules are useful; include numerical compatibility of any supplied altitude with the three side lengths, not merely perpendicularity. |
| B1-06 Candidate delivery | V2 Q5/Q13, V3 Q8, V4 Q6/Q14, V6 Q7, V7 Q7/Q11 use numeric candidate selection without an explicit stem-versus-choices convention. These are not automatically illegal MCQs; clarify where their candidates are serialized and how they count. |
| B1-07 Broad answer grammar | V1 Q9/V3 Q10/V5 Q9/V8 Q10 require strict inequalities but advertise a generic grammar allowing ≤ and ≥. Numeric-expression task V7 Q2 advertises variables in the generic grammar although its assigned product is numerical. Object-count ratio tasks V1 Q3/V4 Q7/V6 Q8/V7 Q3 advertise signed rational ratio terms; narrow their task domains and specify positive, simplest-form ratio terms. Actual importer enforcement has not been exercised. |
| B1-08 Visual equation labels | Fractional-edge prism diagrams V1 Q13/V6 Q12 and the rational number line V2 Q8 are additional cases for testing linked native-equation labels outside SVG/raster visuals. Packet inspection is not a Word-rendering test. |
| B1-09 DOK evidence | Review V4 Q7/V6 Q8 part-to-whole ratios and routine signed-reference/overall-rate tasks for actual DOK-2 demand. V2 Q8 number-line interpolation involves an inferred scale but is DOK 1; review the rationale consistently. Do not automatically change any DOK solely because of step count. |
| B1-10 Workload/difficulty | No G6 form reaches the nonblocking 3/9/3 difficulty target; V2 is all Medium. Required visuals range from three to six. Preserve these as advisory deviations rather than claiming a hard-rule violation. |

For explicit number bounds, see the official [Grade 6 Number System standards](https://www.thecorestandards.org/Math/Content/6/NS/), particularly 6.NS.B.4. These are source-derived boundary checks, not new AAC policy.

### What is not established by this audit

- No import rejection, Word rendering failure, browser defect, wrong generated answer or actual multi-answer MCQ was reproduced. No student-facing items were generated.
- No new exact adjacent/paired fingerprint collision was found. That does not prove arbitrary future wording will preserve the assigned core.
- The generic machine schema is permissive about task-specific answer grammar, required choices and visuals. The application may enforce these in a second validation layer; test that layer during implementation before describing a runtime bug.
- Numeric counterexample responses in V3 Q8/V7 Q7 do not, by themselves, violate the prohibition on written explanations or error analysis; the required response is just a number.
- A frequency table remains a table even when encoded as SVG. B2-03 is a coverage/standard issue, not permission to override the assigned Visual Policy during generation.
- Incoming G7 source records and full-cycle G7 consistency remain pending batch 3.

### Batch 2 evidence manifest

| Form | Exact attachment | SHA-256 |
|---|---|---|
| V1 | AAC_TEST-YEAR_G6_V1_Generation_Packet(2).txt | 3b80bd3ace74d7fb9d206bab015f554b1704f915af042a15c90633db6def8ada |
| V2 | AAC_TEST-YEAR_G6_V2_Generation_Packet(2).txt | a3f2574730dabb23a4de99f6663f95428d5428cf518a0f200329ef1c71c57de0 |
| V3 | AAC_TEST-YEAR_G6_V3_Generation_Packet(3).txt | 2f812c136c87edc5cbfc24e47b66745f998484d7f449accffa90c1fe0bf78ca2 |
| V4 | AAC_TEST-YEAR_G6_V4_Generation_Packet(2).txt | 64787c51cd816aa3f1aa62d449affa03e018215844e87e3504c07e9b7917d788 |
| V5 | AAC_TEST-YEAR_G6_V5_Generation_Packet(2).txt | d427d6856a7b062b20a79cb6f8fb6505340ec4219f66f26698e7dbe188b24b3d |
| V6 | AAC_TEST-YEAR_G6_V6_Generation_Packet(2).txt | 031d7bb1f96c19a27da3b6829398dace73127546e5ea23547a27f833452e557b |
| V7 | AAC_TEST-YEAR_G6_V7_Generation_Packet(2).txt | e70de6d50349d2c9b482bc85ff86e0ae990883cf0f770993e01ff5a21eb449f1 |
| V8 | AAC_TEST-YEAR_G6_V8_Generation_Packet(2).txt | 4e23f5c73eea7ba73aa7f19a53a35eaf965d195d7e7e70ace1dc51d59ed78330 |

### Cumulative next step

Audit batch 3, compare its Grade 6 paired excerpts against these sources, and consolidate shared causes before proposing implementation. Priority order so far: consistent quota classification/reallocation; internally consistent response products; context and domain normalization; standards-to-task alignment; then representation/action cleanup and integration tests. This document records proposed repairs only. Studio v0.4 and its verified source baseline remain unchanged.

---

## Batch 3 — Grade 7, seven supplied packets

Reviewed G7 V1, V2, V3, V5, V6, V7 and V8: 105 full assigned contracts. Each declares Studio 0.4.0 / Blueprint 4.8.0, the same TEST YEAR ID as batches 1–2, and empty preflight findings. No G7 V4 source packet was attached. This is a coverage limitation, not evidence that Studio failed to export it.

### Consistency checks and scope limits

- Every supplied G7 packet has 15 assigned rows, 30 cyclic adjacent exclusions, 15 paired G6 exclusions and 15 skeleton items.
- All 105 G7 source rows match their excerpts in the corresponding G6 packets. All 105 G6 excerpts in these G7 packets match the G6 sources.
- All G7 cyclic excerpts for which a full source is available match their source fields, including V8↔V1. Across all three batches, **1,110 source/excerpt comparisons match**. The remaining 45 excerpt records are three copies of G7 V4's 15 rows.
- Those three V4 copies, embedded in G6 V4, G7 V3 and G7 V5, agree with one another. This establishes reference consistency, not agreement with an unseen V4 source packet.
- No exact canonical-fingerprint collisions were detected within supplied forms or against their adjacent/paired exclusions. V4's excerpted cores allow its overlaps to be inspected, but not its full allocation and response metadata.
- All 345 proposed Template IDs and 345 Surface Form IDs are unique within the supplied batch set and satisfy the exported identifier syntax/length limits. The 23 packet IDs are distinct. Skeleton IDs, hashes and family IDs agree with assignments; result/conflict identities agree. This does not verify ID uniqueness against unseen years or banks.
- All seven supplied G7 forms have six DOK-1 and nine DOK-2 rows. Recorded MCQ, comparison-calculation and large-visual counts satisfy their limits. DOK validity still requires task review. Coordinate-plane compliance has the ambiguity in B3-02.
- None has an Expression answer object. Equation-answer tasks are separate under the current schema; two Equation answers in V8 are not automatically a breach of the stated expression-answer ceiling.
- Statistics procedure selection uses MCQ; numerical statistics uses short answer. Required/prohibited visual metadata agrees with representation metadata.

| G7 form | Required visuals | Large visuals | Recorded comparisons | Comparison calculations | MCQs | Easy / Medium / Hard |
|---|---:|---:|---:|---:|---:|---|
| V1 | 3 | 2 | 1 | 1 | 2 | 0 / 15 / 0 |
| V2 | 2 | 1 | 0 | 0 | 0 | 1 / 14 / 0 |
| V3 | 4 | 3 | 1 | 1 | 2 | 0 / 15 / 0 |
| V4 | 3 | 1 | 1 | 1 | 0 | 0 / 15 / 0 |
| V5 | 3 | 2 | 1 | 1 | 0 | 0 / 15 / 0 |
| V6 | 4 | 0 | 0 | 0 | 0 | 0 / 15 / 0 |
| V7 | 1 | 1 | 1 | 1 | 1 | 0 / 15 / 0 |
| V8 | 2 | 1 | 1 | 1 | 0 | 2 / 13 / 0 |

### New findings

#### B3-01 — Mean-to-total task confuses the number of observations with the sum

**Confirmed overrestrictive result-domain metadata; medium priority.**

G7 V2 Q11, MEAN-TO-TOTAL, supplies a mean and a positive integer observation count and asks for the total sum. It declares `quantity` and `quantityDimension` as Count; the grammar requires a nonnegative integer and the domain rules add irrelevant exact-divisibility instructions.

The observation count must be an integer, but the sum of the observed values need not be. The contract does not state that observations count indivisible objects or that their sum is a count. Integer-total instances remain feasible, so this is **not an impossible task**. It is an unjustified restriction on the general mean-to-total claim, and a likely source of rejected valid numeric instances if the count validator is enforced.

**Repair:** model observation-count and total-value domains separately. For the existing general prerequisite task, use a suitable numerical result domain and remove portion/division boilerplate. If integer totals are intentionally required, make that a specific approved task boundary instead of inferring it from the integer sample size.

**Acceptance tests:** preserve positive integer observation counts; permit a valid noninteger total for the general task; reject malformed/nonpositive observation counts. Do not automatically require a positive mean for an abstract signed data set.

The row is explicitly `Approved Prerequisite Review` with a Prerequisite cluster. Its prerequisite label and historical-looking claim ID are not themselves errors; do not silently replace them with an invented Grade 7 standard.

#### B3-02 — Four-graph MCQs and the one-plane quota use an undefined counting unit

**Confirmed specification ambiguity; high priority before a visual-compliance pass.**

G7 V1 Q13 and V3 Q12 each require four compact graphs for an MCQ and label the representation Proportional Graph. The global rule says G7 allows one coordinate plane. A conventional four-panel rendering uses four Cartesian planes, although it may occupy one visual object or one question. The packet does not say whether the limit counts items, SVG objects, axes panels or mathematical planes; it also does not require a shared-plane rendering.

Consequently, a tag-based or item-based quota can appear to pass while a literal four-panel rendering conflicts with the text. This audit did not run the application's visual counter, and does not establish a runtime bypass. A carefully specified shared-axis presentation may be possible, so this is not a proof that every rendering is unworkable.

**Repair:** define the quota unit explicitly and count coordinate axes semantically across representation categories. If the policy is one plane, approve a legible one-plane task/rendering or reallocate the task. If it is one coordinate-graph item with up to four panels, that is a policy clarification requiring explicit acceptance—not an exception for generators to invent. Define A–D panel/curve labels and their connection to the choice strings.

**Acceptance tests:** distinguish a single graph, a four-panel SVG, and a shared-axis multi-curve visual; none may evade the chosen quota because the representation is named Proportional Graph rather than Coordinate Plane. Render the approved case at the intended print size and verify four distinct, readable choices.

#### B3-03 — Decimal classification is recorded under a conversion claim

**Confirmed claim/action/output mismatch; medium priority.**

G7 V8 Q15 has claim “Convert a rational number to a terminating or repeating decimal,” but its action is classification and its required response is a short label. A classification label is not a converted decimal. Students may choose to convert internally, but that is neither required nor evidenced by the accepted response.

**Repair:** give the classification task a matching approved claim while preserving its intended family and short-label product, or deliberately reallocate to a conversion task if conversion evidence is required. Keep G7 V3 Q1's actual decimal-conversion task separate. Do not silently change the generated response type to satisfy a stale claim.

Also define the two intended classifications as terminating and nonterminating repeating, with approved short aliases. This is a clarity improvement: terminating decimals have equivalent trailing-zero/repeating representations, so the intended classroom convention should be unambiguous. This does not make ordinary classroom use of “terminating or repeating” inherently invalid.

**Acceptance tests:** claim/action/output validation distinguishes conversion from classification. Classification labels and numeric decimal answers cannot substitute for one another solely because they refer to the same rational value.

### Recurrences and extensions

| Existing ID | Grade 7 evidence and repair detail |
|---|---|
| B2-01 Rate units | G7 V1 Q4 and V7 Q5 explicitly demand a rate difference “with compound units,” contradicting their unit-free Number grammar. G7 V4 Q3 has the same conflict in all three available excerpts, but its full packet remains missing. This brings confirmed full-row occurrences across G6/G7 to five, plus one excerpt-only occurrence. Specify subtraction direction or nonnegative gap consistently. |
| B1-01 Context | Explicit neutral situations have Pure mathematics labels at G7 V1 Q2/Q6, V6 Q10, V7 Q3/Q13/Q15 and V3 Q15. Contextual-expression requirements also appear at V2 Q10, V3 Q11, V5 Q14, V7 Q11 and V8 Q11; review whether these require an actual situation and assign matching context/word limits. V6 Q7 is a travel situation despite its Pure mathematics label. Excerpt-only V4 Q8 explicitly requires a neutral percent-change context. |
| B1-03 Operation-specific domains | G7 V8 Q8 outcome counting inherits irrelevant division/exact-divisibility rules; excerpt-only V4 Q9 repeats it. B3-01 is the stronger consequence of the same mechanism: a total sum is typed as a count. Do not remove the deliberately exact-integer prediction policy from V3 Q3/V6 Q14 merely because those tasks also mention counts; separate their valid product constraints from generic boilerplate. |
| B1-05 Angle validity | G7 V3 Q8/V6 Q11 supply adjacent angles ax+b and cx+d on a straight line but have no explicit domain rules. Require a+c ≠ 0 for a unique x, both evaluated angles strictly between 0 and 180 degrees, and a diagram consistent with their sum. Do not let a visually plausible sketch conceal inconsistent equations. |
| B1-05 Percent/interest domains | V2 Q14 needs a nonzero remaining multiplier when recovering an original amount after a decrease. V5 Q11/V8 Q10 need a strictly positive rate and time for a determined principal; “whole-number time” alone allows zero. V3 Q15/V7 Q15 need a valid reduction range. These are underconstrained givens, not established numerical failures. |
| B1-05 Physical rates | V3 Q6/V6 Q8 need positive durations, compatible volume/time units and a defined combined output. V6 Q7 needs positive speeds and distance and compatible units. V2 Q6/V5 Q5/V8 Q6 need a positive denominator quantity and an explicit conversion direction. V1 Q9/V3 Q10/V5 Q10/V7 Q9 allow a rational “count or measure”; use whole counts for indivisible objects or explicitly measured fractional quantities. |
| B1-05 Probability data | V2 Q2/V5 Q15 need nonnegative integer frequencies, a positive trial total and a complete, nonoverlapping outcome partition. V3 Q3/V6 Q14 need observed counts within sample/trial totals, positive denominators and predictions within the target population/trial size; exact integer estimates remain the assigned policy. V6 Q5's explicit equally-likely condition is useful and should be retained. |
| B1-07 Response shape | V3 Q1 requires a terminating decimal but advertises the generic Number grammar that also permits a fraction. V6 Q9 requires a solved strict inequality but advertises generic inequalities, including non-strict signs and unsolved expressions. V2 Q5/V7 Q6 and V8 Q3 require y=kx; generic Equation syntax alone does not enforce the requested variable direction. Add task-specific output validation without confusing algebraic equivalence with compliance with an explicitly required form. No importer behavior was tested. |
| B1-08 Fraction visuals | G7 V2 Q12/V8 Q12 prism nets have rational dimensions; they extend the native-equation-label rendering test matrix. Preserve geometric labels and shared-edge consistency when using linked labels outside the image. |
| B2-03 Standards evidence | G7 V3 Q13/V5 Q13 ask for a difference between means, and V8 Q14 asks for a difference between medians, under 7.SP.B.4. The contracts do not require random samples, variability or a comparative inference; V3/V5 even call the means population means. Record these as narrower calculation evidence or revise the approved claim/task to reflect the intended inferential construct. Do not require a written inference contrary to AAC response rules. |
| B1-09 DOK | Review routine affine-total and percent-change tasks such as V1 Q5/Q6 for specific DOK-2 evidence. Preserve valid structural reasoning in V6 Q2/V8 Q1's pairwise-sum recovery; do not downgrade solely because its final computation is short. |
| B1-10 Balance | Five of the seven supplied forms are entirely Medium, and none has a Hard assignment. Required visuals range from one to four. These are planning deviations, not violations of the explicitly nonblocking difficulty target. |

The standards-alignment observation for comparative statistics is based on the official [Grade 7 Statistics & Probability standards](https://www.thecorestandards.org/Math/Content/7/SP/): 7.SP.B.4 combines center and variability from random samples to support population comparisons. It is an audit judgment about the evidence elicited, not a claim that calculating means is outside Grade 7.

### Safeguards already present that should be retained

- V1 Q3/V7 Q4 require a nonempty bounded integer solution set whose maximum comes from the inequality, not merely the supplied domain ceiling.
- V3 Q7/V5 Q6/V7 Q7 explicitly authorize the maximum-complete-groups floor interpretation and require it to be stated in the stem. Do not apply an exact-divisibility guard to these tasks.
- V3 Q9/V6 Q12 require dividend, quotient and recovered divisor all to be nonzero.
- V6 Q3 requires f=ac in its coefficient identity; this prevents inconsistent constant terms. Excerpt-only V4 Q2 contains the same safeguard.
- V6 Q15/V8 Q13 deliberately permit invalid angle sums so students can classify construction as unique or impossible. Do not globally force every triangle-classification input to form a valid triangle. Likewise, V1 Q8 must retain possible SSS impossibility cases. The official [Grade 7 geometry standard](https://www.thecorestandards.org/Math/Content/7/G/) explicitly includes conditions producing no triangle.
- Classification of triangle construction is geometry, not statistics vocabulary; short labels do not violate the statistics-MCQ rule. Distinguish representative sampling procedures from a guarantee that any realized random sample perfectly mirrors its population.

### G7 V4: excerpt-only review

All 15 reduced rows are available consistently in G6 V4's paired list and G7 V3/V5's adjacent lists. Their action/core, givens, result, standard, context, visual policy and representation were inspected. In addition to the rate-unit/context/domain recurrences noted above:

- Q12 supplies both centers and the common variability measure while calling its two distribution visuals necessary. Ensure essential information is carried by those displays, rather than restating every required number in a stem that makes them redundant. This is a generation risk, not a proven unusable visual.
- Q14 permits symbolic pi or a supplied approximation. The eventual stem must select the intended accuracy convention; the answer key must not treat an arbitrary approximation as exactly equivalent to the symbolic answer.

The excerpts omit DOK, difficulty, response-mode flags, full answer grammar, domainRules arrays, footprint, specification hashes, proposed IDs and the packet's identity/schema/skeleton. Therefore V4's full generation/import contract and allocation quotas remain **unverified**. Do not construct a replacement packet from these excerpts or call the complete 24-form audit closed.

### Batch 3 evidence manifest

| Form | Exact attachment | SHA-256 |
|---|---|---|
| V1 | AAC_TEST-YEAR_G7_V1_Generation_Packet(3).txt | 89d49c4224fe5fa0b530a2eb9432c6bf9f3ab81717995c6d65b5fd39a0da6193 |
| V2 | AAC_TEST-YEAR_G7_V2_Generation_Packet(4).txt | c09b6b16927d0c431686361383b7d520a9ad132943a55a716bf31f712c70e6c0 |
| V3 | AAC_TEST-YEAR_G7_V3_Generation_Packet(3).txt | 56914dc869636c2d58424594a50875727b3099a3215e16f50da3b37a5052593e |
| V4 | AAC_TEST-YEAR_G7_V4_Generation_Packet.txt | 6b94dff1a4ec9123b84a5bd70cd88dfc260bacff7b9d863d93e86a7d2c29c907 |
| V5 | AAC_TEST-YEAR_G7_V5_Generation_Packet(2).txt | e36cf01f354da4dae271bb3539955fbb2cbaf86529f3516ffe76846034b12fc8 |
| V6 | AAC_TEST-YEAR_G7_V6_Generation_Packet(2).txt | 7048a44288e7e6d6661642c156b0b016d1a617db880324f55e611ada1b98859c |
| V7 | AAC_TEST-YEAR_G7_V7_Generation_Packet(2).txt | b499bc1f3ec1f3bf8eba847ab68281ffe98ec159419474bd9d6b6db5944a86ce |
| V8 | AAC_TEST-YEAR_G7_V8_Generation_Packet(2).txt | 1d836ee99b9eeb909109a6be977e1fdbfdd5aa3d14ec6e508dc1a6226e4bbdcf |

## Consolidated repair priorities after the three submitted batches

This is a proposed repair backlog, not an implementation approval or a verified new release. Original finding IDs remain stable.

| Priority | System-level repair | Findings | Required evidence before closure |
|---|---|---|---|
| 1 | Derive quotas from approved semantic classifications and explicit visual counting units | B2-02, B3-02 | Consistent alias classification; G6 V2 reallocation or documented uniform policy; multi-panel graph quota tests; all cyclic/paired checks rerun |
| 1 | Unify exact response product, answer domain, unit handling and required output form | B2-01, B3-01, B1-07 | Numeric units remain in stems; total sums are not accidentally counts; task-specific decimal/equation/inequality tests |
| 1 | Repair claim/context/standard mismatches before regenerating prose | B1-01, B2-03, B3-03 | One authoritative task record; correct word limits; approved direct/supporting/prerequisite mappings |
| 1 | Make givens/unknowns and task validity explicit | B1-02, B1-03, B1-05, B2-04 | Derived totals truly withheld; relevant typed domain rules; candidate truth-set checks; valid geometry; preserve intended impossible-triangle and floor-count cases |
| 2 | Align instructions, action metadata and candidate/visual delivery | B1-04, B1-06, B1-08, B2-05 | No method restrictions; clear candidate serialization; synchronized task descriptions; rendered equation-label/graph-choice checks |
| 2 | Separate hard preflight errors from review advisories | B1-09, B1-10 | Teacher-reviewed DOK/workload evidence; transparent difficulty deviations; no unsupported claim of full semantic clearance |
| Completion gate — closed | Full G7 V4 export received and audited | Coverage gap resolved; no new defect ID | All 24 packet identities and 1,200 source/excerpt comparisons checked; see supplemental closure |

Recommended implementation order: normalize canonical task records first, then derive packet prose/grammar/quota metadata from those records, then repair allocations and run the full matrix checks. Add targeted import/export and rendering regression cases only after the repaired contracts are approved. Keep the 23 supplied packets and their hashes as regression evidence; do not patch them and treat that as repairing the bank.

No student-facing items were generated. No imports, finalizations, application edits, GitHub writes or deployments occurred in this audit round. Packet consistency is verified to the scope stated above; actual runtime/import/export behavior and the missing G7 V4 source are not verified.

## Supplemental closure — full G7 V4 packet received

The supplied `AAC_TEST-YEAR_G7_V4_Generation_Packet.txt`, issued 2026-09-18T06:26:42.822Z, declares Studio 0.4.0 / Blueprint 4.8.0 and the same TEST YEAR ID. Its full-source SHA-256 is recorded in the updated manifest above. This section supersedes all earlier missing-V4 limitations; it does not close the repair findings.

### Full-matrix checks completed

- All 24 full packets are now available and all 360 assigned rows have been reviewed.
- All **1,200** embedded adjacent/paired records match their source rows field-for-field. This includes the 45 previously excerpt-only V4 records and V4's own 45 exclusion records. V8↔V1 checks are included.
- No exact canonical-fingerprint collisions were found within forms or against their exported adjacent/paired exclusions. Semantic task validity and future generated-item nonredundancy remain separate review requirements.
- All 360 proposed Template IDs and 360 Surface Form IDs are unique within this audit set and meet exported identifier syntax/length limits. All 24 packet IDs are distinct. Skeleton IDs, specification hashes and family IDs agree with assignments; result/conflict identity envelopes agree.
- V4 contains 15 assigned rows, 30 cyclic exclusions, 15 paired G6 exclusions and 15 skeleton items. It has six DOK-1 and nine DOK-2 assignments, 15 short-answer items, no Expression answers, one Equation answer, one comparison calculation and one recorded comparison task. All 15 difficulty labels are Medium.
- V4 has three required visuals: Q1 Number Line and Q9 Statistical Organizer are Standard Visual; Q12 Statistical Graph is the sole Large Visual. Required/prohibited metadata and representation agree; large-visual placement is allowed. No coordinate-plane visual is assigned in V4.
- The packet reports `PREFLIGHT FINDINGS []`; the recurring semantic issues below explain why that is not equivalent to full clearance.

### Findings confirmed or extended under existing IDs

| Existing issue | G7 V4 evidence and repair implications |
|---|---|
| B2-01 — units | Q3 explicitly requires a unit rate with compound units, while its Number answer grammar prohibits unit words. This is now confirmed from the full row, bringing the G6/G7 total to **six full-row occurrences**. Keep units in the stem and make the required answer numerical. |
| B1-01 — context | Q8 explicitly requires a short neutral percent-change context but has Pure mathematics and a 20-word limit. Q6 is a travel application under the same label; Q13 requires a contextual expression. Align context and word limits with the approved task rather than forcing a story into the wrong metadata. |
| B1-03 — irrelevant rules | Q9 counts favorable outcomes but includes divisor/portion-size and exact-divisibility boilerplate. Use event-count constraints, not division preconditions. |
| B1-05 — mathematical domains | Q3 needs a positive denominator quantity; Q6 needs positive speeds/distance and consistent units; Q11 needs positive scales with explicit scale direction and compatible length units; Q14 needs a positive radius. Q15's two uses must not exceed the starting physical amount if the required result is an amount remaining. These are explicit-boundary improvements, not proof that every possible instance is invalid. |
| B1-05 — center/spread validity | Q12 requires a common nonzero variability measure. Specify which measure, require it to be positive, and ensure both plotted distributions actually possess the stated centers and common spread. Define the center gap as nonnegative or state an ordered subtraction. Do not merely label two incompatible plots with the same spread. |
| B1-07 — response form/precision | Q7 requires y=kx but advertises only generic equation syntax. Q14 allows symbolic pi or an approximation; the eventual prompt must select the precision convention, and scoring must distinguish approximate answers from exact equivalents. No importer rejection or tolerance behavior was tested. |
| B1-08 — essential visuals | Q12's plot must carry information needed for the task; avoid supplying every necessary value independently of the display and then calling it necessary. This remains a generation/visual-review risk, not a demonstrated rendering failure. |
| B1-10 — planning balance | All 15 V4 tasks are labeled Medium. Across all eight G7 forms, six are entirely Medium and none has a Hard assignment. The difficulty target remains explicitly nonblocking. |

Q2's f=ac identity condition and Q5's nonempty, inequality-bounded integer maximum are intact and should be retained during repairs. No new independent defect category was needed for this supplemental packet: its findings extend the existing register.

**Audit coverage is now complete. Software repair and verification are not.** The consolidated priorities above are ready to inform an approved implementation specification. No student items were generated and no Studio, bank, GitHub or deployment state was changed. Runtime validation and rendered export behavior remain untested in this audit round.
