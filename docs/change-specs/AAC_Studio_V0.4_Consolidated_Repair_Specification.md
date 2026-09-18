# AAC Studio V0.4 — consolidated audit and repair specification

Prepared September 17, 2026. Audited release: Studio 0.3.0 / Blueprint 4.7.0, source commit `ad82068`. Target application release: **V0.4**. This is an implementation specification, not a claim that V0.4 has been built.

## Executive decision

**Repair the shared bank, task contracts, packet writer and validators before the next release.** Both batches have intact identities and comparison records, but their empty preflight lists miss substantive conflicts. This document consolidates the previous A01–A12 backlog, adds four new root findings A13–A16, and expands the affected locations and domain failures under existing findings. Do not count repeated instances as separate fixes.

No student items were generated, imported, accepted or finalized. Production source, released HTML, assessment-year state and historical records are unchanged. Diagnostic fixtures and existing QA examples were used only to exercise validators.

## Coverage and limits

| Coverage | Forms | Assigned rows |
|---|---:|---:|
| Batch 1: G5/G6/G7 V1–V3 | 9 | 135 |
| Batch 2: G5/G6 V4–V8 | 10 | 150 |
| Direct packet audit, combined | **19** | **285** |
| G7 V4–V8: present as paired comparison records, no standalone packets supplied in these batches | 5 | 75 comparison-only |

Thus G5 and G6 each have all eight standalone packets checked. G7 has V1–V3 standalone checks and V4–V8 comparison-record visibility. Do not report 24/24 newly audited standalone packets. Before V0.4 release, locally export and test all 24 current packets, including G7 V4–V8; no user reupload is necessary if the source bank is available.

All 19 supplied packets parse; all 285 assigned hashes and all 19 design revisions match the released bank. Each has 15 unique questions, all 30 cyclic adjacent records, the correct paired-grade records, and matching result-skeleton identities. Current preflight is empty for every supplied form. These facts establish mechanical consistency, not content validity.

| Form | DOK 1 / 2 as allocated | MCQ | Adjacent / paired records |
|---|---:|---:|---:|
| G5 V1 | 6 / 9 | 0 | 30 / 15 |
| G5 V2 | 5 / 10 | 0 | 30 / 15 |
| G5 V3 | 6 / 9 | 0 | 30 / 15 |
| G5 V4 | 6 / 9 | 0 | 30 / 15 |
| G5 V5 | 6 / 9 | 0 | 30 / 15 |
| G5 V6 | 5 / 10 | 0 | 30 / 15 |
| G5 V7 | 6 / 9 | 0 | 30 / 15 |
| G5 V8 | 6 / 9 | 0 | 30 / 15 |
| G6 V1 | 6 / 9 | 2 | 30 / 30 |
| G6 V2 | 6 / 9 | 0 | 30 / 30 |
| G6 V3 | 6 / 9 | 1 | 30 / 30 |
| G6 V4 | 6 / 9 | 1 | 30 / 30 |
| G6 V5 | 6 / 9 | 2 | 30 / 30 |
| G6 V6 | 6 / 9 | 1 | 30 / 30 |
| G6 V7 | 6 / 9 | 1 | 30 / 30 |
| G6 V8 | 6 / 9 | 2 | 30 / 30 |
| G7 V1 | 6 / 9 | 2 | 30 / 15 |
| G7 V2 | 6 / 9 | 0 | 30 / 15 |
| G7 V3 | 6 / 9 | 2 | 30 / 15 |

Zero MCQs is permitted; the cap is two. Nonadjacent repetition is not automatically a violation. As a positive control, G6 V5 Q12 and V7 Q12 have different structure codes but correctly share the normalized DISTRIBUTION-MEDIAN identity; they are nonadjacent and should not be forced apart solely because of repetition. Preserve the explicitly approved G7 prerequisite mean/total claim.

## Consolidated findings


P1 = repair before calling the next release clean. P2 = harden or explicitly resolve before broad generation. Review judgments are distinguished from reproduced parser failures.

### A01 — Display-dependent claim versus prohibited display [P1; confirmed field conflict]

**Locations:** G6 V1 Q11, V3 Q11, V5 Q14, V7 Q14 and V8 Q13, claim G6-040. The last three are directly confirmed in batch 2.

The binding claim says “Select an appropriate measure of center or variability for a displayed data set.” The assigned givens require a short text description, explicitly no graph/table or no visual; Visual Policy is Prohibited. The two tasks can be sensible text-only MCQs, but they do not fulfill the displayed-data claim as written. Treating a qualitative description as a displayed data set silently changes the claim requirement.

**Repair:** explicitly distinguish the text-description and displayed-data task variants. Either authorize a revised claim that permits both, or retain the displayed-data claim and allocate the required display. Do not let the generator choose which field to ignore. Preserve historical wording separately.

**Regression:** preflight must flag a displayed-data requirement paired with a text-only, visual-prohibited contract unless an explicit approved interpretation resolves it. This is an internal claim conflict, not a claim that the full external standard always requires a graph: [6.SP.B.5.d](https://www.thecorestandards.org/Math/Content/6/SP/) permits choosing measures in relation to distribution shape and context.

### A02 — Method restrictions contradict the permanent no-prescribed-method rule [P1; confirmed]

**Locations:** G5 V1 Q6 and V5 Q7 (“without calculating the product”) and G5 V2 Q13 (“do not calculate the exact scale factor”). Related comparison records contain similar restrictions.

These instructions are binding, while the permanent rules forbid prescribed methods. The objective answer cannot establish whether a student computed an intermediate quantity. The current language validator also allows both “Do not calculate the product” and “Do not calculate the exact factor”; diagnostic copies of existing QA examples produced no issues.

**Repair:** keep scaling reasoning in teacher-facing design intent, not a student prohibition. State the required comparison or factor classification, but accept any valid method. Review DOK independently; banning computation does not establish cognitive demand. Extend validation to catch explicit method bans without incorrectly rejecting legitimate requests for an estimate.

**Refinement for V0.4:** do not implement a blanket ban on the words “do not evaluate” or “without expanding.” In G5 V6 Q8 and G6 V4/V7 Q2, requesting an unevaluated expression defines the required output. In G6 V6 Q3 and V8 Q2, counting outermost terms defines the expression being inspected. Those are not equivalent to policing a student’s internal solution method. Ask for the required form and allow any valid route to it.

**Regression:** actual method bans must be flagged; expression-form requirements, term-count targets, ordinary comparison tasks and intentionally specified estimation tasks must remain allowed.

### A03 — Different semantic keys can conceal the same core relationship [P1; mathematical review finding]

**Adjacent pair:** G5 V3 Q8 versus G5 V4 Q8, formerly seen in V3 exclusions and now directly confirmed in the supplied V4 packet.

V3 combines two lengths in compatible units and finds their total. V4 supplies a remaining length and a removed length in different units and finds the original length. Both require unit conversion and addition of two known components to recover a total. Calling the total “original length” and giving a removal story does not, in this case, supply a different mathematical given/unknown relationship. The current keys are `CONVERT-TOTAL` and `CONVERT-THEN-RESTORE`, so the equality-based exclusion test misses the overlap.

**Paired-grade candidate needing explicit adjudication:** G6 V2 Q15 versus G7 V2 Q7. The first solves `y=ax+b` for x; the second finds a per-group amount from a total, fixed amount and group count. Both can be represented as `total = fixed + known factor × unknown factor`, with the missing factor `(total−fixed)/known factor`. The keys `AFFINE-MISSING-COUNT` and `AFFINE-MISSING-RATE` distinguish roles that the generic G6 input does not actually constrain. A contextual interpretation alone is insufficient under the current strict overlap rule.

**Repair:** record a canonical relation, known roles, unknown role, necessary transformations and any mathematically material domain distinctions. Review the first pair as an exclusion collision; explicitly resolve the second rather than treating distinct strings as proof of distinct structure. Run the resulting comparisons across the whole bank before reallocating affected tasks. Do not collapse every task with the same final formula: genuine differences in givens/unknowns can be valid.

**Regression:** these pairs must be presented to the semantic review gate; a different structure name cannot automatically dismiss them.

### A04 — DOK remains inconsistently justified [P1; content-review finding, not a parser failure]

**Strong review candidates:** G5 V2 Q11, V4 Q13 and V7 Q11 (two stated coordinate changes); G6 V3 Q1 and V7 Q1 (compute two explicit decimal quotients and compare); G5 V1 Q11 and V7 Q9 (one missing part from total and other part). Batch 2 also includes G6 V4 Q13, whose DOK 2 assignment can reduce to subtracting known frequencies from a stated total, and G5 V6/V8 Q15, whose supplied complete hierarchy may make the task routine graph reading. Adjudicate these rather than assuming all are DOK 2.

Their DOK 2 rationales do not clearly establish demand beyond familiar procedures or routine one-step interpretation. In contrast, G5 V2 Q8 (two decimal products and a sum) and Q10 (combine recipient counts before sharing) are DOK 1. The number of operations, a context sentence or the word “coordinate” is not enough to resolve this distinction.

`activate-bank-v03.py` generates some DOK rationales from stock wording plus a solved example. `allocationFindings()` checks that a rationale exists and matches the assigned label; it does not adjudicate its quality. These checks establish internal consistency, not independent DOK validity.

**Repair:** review the shortest legitimate solution route, identify the specific nonroutine relationship required, and explicitly approve or lower each disputed label. If lowered, rebalance the affected forms with different tasks instead of restoring DOK 2 merely to meet the quota. For example, lowering G6 V3 Q1 would make that form 7 DOK 1 / 8 DOK 2, outside the current DOK 1 limit.

**Regression:** keep adjudicated counterexamples and rationales as independent fixtures. Require cognitive-demand review separately from successful arithmetic and quota counts. This audit does not assert that every contextual multistep task is DOK 1.

### A05 — Difficulty is assigned by position, not task demand [P1; confirmed source behavior]

**Scope:** all 19 supplied packets, and the current compiler.

`compile-bank-v03.py` assigns Easy to Q1–3, Hard to Q13–15 and Medium to the rest. It therefore guarantees the 3/9/3 count without evaluating the tasks. Examples include G5 V2 Q2's two multidigit multiplications labeled Easy, while G6 V2 Q15's routine inverse substitution and G7 V1 Q15's two-number quotient are labeled Hard. Those labels may sometimes be defensible for particular values, but position alone supplies no evidence.

**Repair:** retain intended difficulty at the task level with operand/workload bounds and a rationale; check realized difficulty after item generation. If position is merely a planned ramp, name it “target difficulty,” not a verified characteristic. Keep the 3/9/3 target nonblocking as already approved.

**Regression:** moving a task to another question number must not automatically change its reviewed difficulty. A quota pass must not be reported as difficulty validation.

### A06 — A binding response field is outside reviewed-evidence validation [P1; reproduced]

**Scope:** shared bank validation.

Changing only G5 V1 Q1's `responseProduct` to “One written explanation of the place-value relationship” leaves `reviewedEvidence()` accepted and returns no `taskIntegrity()` issue. The current evidence contract omits this field, and the catalog-task comparison also omits it. Yet the packet tells the generator that the exact response product is binding.

The specification hash would change if the seed were changed; this is not a hash-tampering bypass. The defect is that a freshly rebuilt but internally contradictory contract can retain its reviewed status.

**Repair:** derive `responseProduct` from the authoritative structured response fields, or include it in the evidence contract and validate its consistency with the answer object, required result and permanent rules. Audit other exported binding fields for the same gap.

**Regression:** a one-field mutation introducing a prose response must invalidate review and block preflight even when all hashes are freshly recomputed.

### A07 — Packet-permitted SVG quoting is rejected by the importer [P1; reproduced]

**Scope:** all SVG-required items.

The packet allows quoted attributes. A complete otherwise-valid SVG with `viewBox="0 0 100 100"` passes. The identical SVG using single quotes fails with “SVG requires a quoted viewBox.” A viewBox using tab-separated numbers also fails. The parser initially accepts both quote styles, but the final viewBox regular expression accepts double quotes and spaces only.

**Repair:** parse and validate viewBox values consistently with the accepted SVG syntax, including safe single-quoted attributes and legal whitespace. Retain active-content, external-resource and element restrictions. Publish the actual allowed attribute list in the packet; the current packet lists elements but not the validator's restricted attributes.

**Regression:** equivalent safe single/double-quoted SVGs must both import and render. Malformed or unsafe SVG must still fail. This is a real round-trip compatibility defect, not a content-review disagreement.

### A08 — Interval wording does not specify the accepted answer encoding [P2; reproduced interoperability risk]

**Locations:** G5 V2 Q13, V6 Q7 and V8 Q6.

The required product is “one short interval label relative to 1.” The validator accepts `less than 1` and `greater than 1`, but rejects `0<k<1`, `(0,1)` and `k>1`. Those are natural mathematical interpretations of an interval request. The general Label grammar mentions a maximum of three words but omits its punctuation restrictions.

**Repair:** give this task an explicit response set and accepted aliases, such as `below 1`, `equal to 1`, `above 1`, and avoid the word “interval” if only categorical text is intended. Alternatively, deliberately support a symbolic interval object. Distinguish student-math encoding from the canonical teacher-answer encoding: for expression answers, plain `(x-5)/3` passes while raw LaTeX does not.

**Regression:** every advertised answer example and alias must pass its actual validator. Do not weaken all Labels to arbitrary prose or punctuation.

### A09 — Context classifications remain inconsistent with the task [P2; confirmed metadata mismatch]

**Examples:** G5 V1 Q5 is a sharing situation labeled Pure mathematics with a 20-word limit. G7 V1 Q9 and G7 V3 Q10 require groups and per-unit quantities but have the same pure-math classification. G7 V2 Q2 uses simulation results under Pure mathematics; G7 V2 Q6 uses measured quantities and a conversion under the same classification.

Not all of these are mathematically unworkable. The problem is that a generator must infer whether an abstract equation, a measurement statement or a context is actually required. That choice also changes language allowance and can change intended DOK.

**Repair:** define context categories operationally, distinguish mathematical measurement situations from narrative contexts, and assign the corresponding word budget intentionally. Do not blanket-upgrade all tasks to 45 words or force unnecessary stories.

**Regression:** the required givens, context category, permissible student presentation and language limit must agree. Recheck the shortest clear ELL-accessible realization rather than relying on a count alone.

### A10 — Necessary domain and uniqueness constraints are missing [P1; concrete failure cases]

| Location | Gap | Necessary repair |
|---|---|---|
| G6 V2 Q15 | `y=ax+b` does not explicitly require nonzero a; a=0 can give no input or infinitely many. | Require a≠0 and a unique admissible input. |
| G7 V3 Q9 | Dividend may be zero although quotient is required nonzero; no valid divisor then exists. | Require nonzero dividend as well as nonzero quotient, and a nonzero recovered divisor. |
| G7 V1 Q3 | A finite domain upper bound can itself be the answer, or there may be no feasible integer. The rationale says the bound does not supply the answer, but the givens do not enforce that. | Require a nonempty integer solution set and an active inequality-derived upper limit strictly below the domain ceiling. |
| G5 V3 Q9 | No positivity/exact-divisibility condition for the portion length or number of pieces. | Specify positive usable remainder/divisor and whether only complete pieces count; require exact division if that is the intended action. |
| G6 V1 Q10 | Nonzero a, b and d are specified, but positivity is not; negative coefficients can enter a task mapped to the nonnegative-rational one-step-equation standard. | Require positive a, b and d, giving positive x and c. |
| G6 V2 Q6 | “different units” is ambiguous about whether rates already share units; no conversion relationship is specified. | Specify common output units and supply any necessary conversion, or explicitly require both pairs already use the same unit system and rate units. |

These are permitted bad instantiations, not a claim that the existing QA example for each is invalid. The [official 6.EE.B.7 wording](https://www.thecorestandards.org/Math/Content/6/EE/) explicitly uses nonnegative rational values.

**Repair:** add machine-readable domains and uniqueness conditions, not just “choose manageable numbers.” Test zero, signs, boundaries, noninteger counts and inconsistent givens before approving each template family.

**Additional domain/response-type conflict directly exposed in batch 2:** G6 V4 Q10, V5 Q8, V6 Q10 and V8 Q9 require a nonnegative integer Count but do not require exact divisibility. The same gap occurs in batch 1 at G6 V2 Q10 and V3 Q9. As a diagnostic—not a student item—(3/4−1/4)/(1/3)=3/2 is valid fraction arithmetic using permitted kinds of givens; the Count validator rejects it. Returning 1 would silently introduce a complete-portions/floor interpretation that is not assigned. Conversely, G5 V6 Q10 and V8 Q9 allow a Unitless scalar for “number of pieces,” so a fractional answer can pass there. Both the mathematical domain and the response subtype need to agree.

**Required implementation:** distinguish an exact integer count, a fractional quantity measured in portion-units, and a maximum-complete-count interpretation. For current unrounded count tasks, require positive divisors and exact divisibility. Only introduce floor/rounding when explicitly assigned. Carry dimensional meaning separately from answer-domain constraints: a count being physically dimensionless does not justify dropping its integer restriction.

**Further batch-2 domain checks:** G6 V4 Q12 needs a realizable nonsquare base: with perimeter P and given edge a, require P>2a and P≠4a, plus positive height. G6 V5 Q13 and V8 Q12 need positive base perimeter/height. Triangular-prism nets such as G6 V7 Q13 need realizable triangle lengths, an unambiguous perpendicular altitude where used, and matching face edges. Recheck G6 V4 Q11 under the shared-equation positivity rule; positive group/divisor counts in G5 V8 Q11; and at least two positive batches in the two-batch cutting family (G5 V2/V5/V8 Q14). LCM templates at G6 V4/V8 Q1 should explicitly select positive integers. These are generation-domain safeguards, not allegations that every currently supplied example is invalid.

### A11 — Variation tags are inherited labels, not reliable evidence [P2; confirmed metadata concern]

**Examples:** G5 V1 Q13 is labeled “Classification versus calculation” but only counts cubes. G5 V2 Q6 is “Representation-to-symbol direction” although the task supplies numerical rules and requires an inferred pair without a visual. G5 V3 Q9 is “Reverse given / unknown” despite presenting a forward sequence of joining, removal and division.

A tag may describe an intended contrast with another task, but the packet does not identify that counterpart or substantiate the contrast. The count of four variation modes can therefore pass without proving the intended variation.

**Repair:** bind a variation claim to the compared task and the actual changed relationship, or define intrinsic mode categories that can be checked from the task itself. Separate descriptive tags from hard quotas unless they have adjudicated meanings.

**Regression:** reject unsupported inherited tags; changing a tag alone must not make an otherwise duplicate task pass.

### A12 — Packets repeat audit internals and answer examples unnecessarily [P2; confirmed size, inferred usability risk]

**Scope:** all 19 supplied files total 5,986,692 bytes. Individual files range from 285,216 to 354,251 bytes. Batch 1 alone totaled 2,776,949 bytes.

Each assigned and comparison row includes a `designReview` containing a second contract, a witness answer, worked witness calculations and boilerplate review evidence. There are 60 records per G5/G7 packet and 75 per G6 packet. The compact review objects alone account for roughly 109–140 kB per packet in batch 1 before their expanded indentation.

This does not prove a truncation or context-window failure occurred. It does increase repeated material, and numeric witness answers without their complete original items can anchor a generator to irrelevant numbers. “Generate from scratch” is not helped by exporting solved internal examples for every excluded task. Global reference context also includes unrelated historical slot notes; it is explicitly nonbinding, but adds noise.

**Repair:** retain the full audit evidence inside Studio. Export one authoritative assigned contract, concise complete comparison fingerprints, necessary response grammar and scoped guidance. If a witness is ever included, label it clearly nonbinding and do not present its answer as a constraint. Preserve all 30 adjacent records and all paired-grade records; compactness must not remove exclusion information.

**Regression:** verify a compact packet preserves every required field, comparison and identity. Set a packet-size regression budget and distinguish schema examples from mathematical exemplars.

### A13 — Unit-identification answers contradict the global units prohibition [P1; new confirmed conflict]

**Locations:** G5 V5 Q13 and V7 Q12, CUBIC-UNIT-IDENTIFY.

The assigned product is a cubic-unit label, but the response contract says “No units or explanatory text in the answer field,” and the row grammar repeats “Unit words belong in the prompt, not the answer.” These rules cannot all be obeyed for a unit-identification task. The importer itself accepts `cubic centimeter` and `cm³`, but rejects `cm^3` under its generic Label grammar. The defect is both contradictory guidance and undocumented permitted aliases; it is not that every cubic-unit answer is rejected.

**Repair:** make the no-units rule conditional on a numerical-result task. Add an explicit Unit label subtype or task-specific answer set for unit identification, and distinguish it from generic category labels. State canonical forms and accepted equivalents; do not broaden all labels to arbitrary prose.

**Regression:** a unit-identification packet must explicitly permit its answer units; supported unit aliases must import and render. A numerical-volume answer with appended units should still follow the numerical-answer policy.

### A14 — Estimation contracts do not guarantee one defensible answer [P1; new domain ambiguity]

**Locations:** G5 V4 Q10 (nearest whole-unit difference), V5 Q3 (estimated sum), V6 Q11 and V8 Q10 (reasonable benchmark answer). Batch-1 G5 V3 Q4 uses the same estimated-sum family.

“Distinct benchmark-based numerical candidate answers” does not guarantee that exactly one is reasonable. “Estimate” alone does not select a unique benchmark or tolerance. The nearest-whole task is more precise, but its domain does not exclude exact half-unit ties or state a tie policy. A one-point objective response must not depend on guessing the author’s preferred estimation strategy.

**Repair:** encode a clear target such as the closest listed value, a specified benchmark set, or a declared numerical tolerance. Require a unique winning candidate for single-choice targets; exclude ties unless an explicit tie policy or accepted-answer set is supplied. Avoid adding a prescribed student solution method. Preserve intentional estimation skills rather than converting all such tasks into exact arithmetic.

**Regression:** enumerate candidate distances where the target is closest-value; test halfway cases and two plausibly reasonable choices. Reject ambiguity before packet export. Where multiple answers are intentionally valid, the prompt and scoring contract must say so.

### A15 — Representation meaning depends on the encoding [P1; new reproduced inconsistency]

**Locations:** G6 V4 Q13 and V6 Q13, assigned Statistical Graph with givens described as a numerical frequency display.

A native table payload is rejected with “A table does not satisfy the assigned statistical graph.” For G6 V4 Q13, however, the existing accepted QA visual is an SVG consisting of Value/Frequency columns—a frequency table in SVG form—and it passes. G6 V6 Q13’s existing visual is a dot plot and passes; a frequency-table representation of its observations is rejected. These cases expose both an ambiguous “frequency display” assignment and unequal enforcement across table/SVG encodings.

**Repair:** decide and record the intended semantic representation. If it is a frequency table, allocate Statistical Organizer or a dedicated Frequency Table representation and accept its supported table encoding. If a graph is mathematically required, say which graph, and do not treat an SVG table as satisfying it. Keep semantic representation separate from media format; allowing SVG must not silently permit any diagram.

**Regression:** semantically equivalent permitted tables should not pass or fail merely because of media format. Prohibited representations must remain prohibited regardless of encoding. For SVG/raster semantics that cannot be checked reliably in code, require an explicit visual-review gate and describe that limitation honestly.

### A16 — Generic Expression validation misses required response structure [P2; new reproduced validation gap]

**Locations:** G6 V4 Q2 and V7 Q2 require an expression with whole-number exponents; G5 V6 Q8 requires a numerical expression preserving grouped operations.

The current response grammar accepts a standalone number such as `42` for these Expression objects. This probe shows syntax acceptance only—it does not claim that 42 solves any assigned task. A generic valid expression is not necessarily the particular response form promised by the packet. For exponent tasks, an answer without any exponent can therefore pass the automated response-type check.

**Repair:** add task-specific output requirements, such as required exponent structure or an unevaluated grouped expression. Validate syntax separately from mathematical equivalence/correctness. Restrict final answer form, not the student’s internal method. Keep educator review for properties the validator does not establish.

**Regression:** an evaluated constant must not satisfy an exponent-expression or explicitly unevaluated-expression requirement. Valid equivalent requested forms should pass; malformed algebra and explanatory prose must still fail.

## V0.4 implementation plan

| Work package | Findings | Required deliverable |
|---|---|---|
| Authoritative contract | A01, A02, A06, A08, A09, A13 | One consistent structured task; derived response prose; conditional unit rules; canonical label aliases; clear context/language policy. |
| Mathematical domains | A10, A14 | Positive/nonzero bounds, exact-count versus complete-count semantics, realizable geometry, unique estimates and valid candidate sets. |
| Bank review and allocation | A03, A04, A05, A11 | Adjudicated mathematical relationships, shortest-solution DOK review, task-based difficulty targets and supported variation tags. |
| Import/export consistency | A07, A15, A16 | Safe SVG normalization, representation-versus-media separation, required expression structure, matching published/runtime grammars. |
| Packet simplification | A12 | Compact complete assigned contracts and comparison fingerprints; internal solved examples removed from default generation payloads. |
| Compatibility and release | All | Protected historical records, fresh-year generation, backup migration, full 24-form regression and honest verification report. |

### Required architecture changes

1. Use one authoritative structured contract. Derive duplicated prose and encoding guidance from it; include every independently binding field in the review dependency/hash. Changing one such field invalidates the previous review.
2. Separate response kind, allowed domain, canonical encoding, and required output structure. For example, an integer count is different from a generic rational value; a unit label is different from a numeric answer with an appended unit.
3. Separate visual policy, semantic representation, and encoding. Required frequency table versus required graph is a task decision, not a side effect of using SVG or a table object.
4. Record the mathematical relation and known/unknown roles independently from names and question positions. Automated normalization supports, but does not replace, semantic adjudication.
5. Separate target quotas from review evidence. DOK/difficulty/variation counts must not certify themselves. Do not invent additional arithmetic solely to force a desired DOK label.
6. Keep diagnostic and generation flows distinct. An unresolved binding conflict blocks ordinary generation and yields an actionable diagnostic; a teacher-readable warning cannot silently waive it.

### Ordered implementation

1. Preserve V0.3 and all historical bank snapshots. Add the reproduced failing cases before modifying production code.
2. Resolve binding-rule contradictions and answer/visual grammar defects. Record deliberate claim changes explicitly; do not silently broaden G6-040.
3. Add numerical domains and objective estimation criteria. Resolve each disputed DOK/semantic finding with a recorded decision.
4. Reallocate only as needed, globally checking all cyclic and paired-grade relations. Never restore a disputed label merely to satisfy a quota.
5. Regenerate the current contracts and compact packets; invalidate incompatible drafts safely while retaining their history. Preserve finalized records unchanged.
6. Update every visible version/export label to V0.4 using one source. Advance blueprint/contract revisions if their binding content changes; do not reuse V0.3 fingerprints for modified contracts.
7. Run all gates below before publishing the offline HTML. Keep the single-file offline workflow, product credit, year management, backups, safe deletion and review controls that already work.

## Release acceptance tests

| Gate | Must demonstrate |
|---|---|
| Contract consistency | No claim/visual, units/label or method/output contradictions; single-field response-product mutation invalidates review. |
| Domains | Zero and negative divisors rejected where forbidden; exact counts integral; no silent rounding; nondegenerate geometry; unique estimate or explicit accepted set. |
| Semantic separation | Adjudicated relationships across all within-form, cyclic V8/V1 and paired-grade comparisons; no dependence on different IDs alone. |
| Cognitive/workload review | DOK approved independently of quotas; difficulty not assigned solely by position; language and variation labels justified. |
| Response compatibility | All advertised aliases and safe SVG quote/whitespace variants accepted; unsupported prose/active content rejected. |
| Output form | Exponent/unevaluated-expression tasks require the promised answer structure; numeric tasks remain numeric. |
| Representation | Native tables and SVG tables receive consistent semantic treatment; genuine graph requirements cannot be satisfied by an unrelated SVG. |
| Complete bank | All 24 G5–G7 V1–V8 current packets exported and checked, including G7 V4–V8. |
| Actual round trips | More than one independently varied compliant response encoding per relevant family, tested through import and Word export in isolated QA state. Render representative fraction/visual edge cases. |
| Negative controls | Deliberate conflicts rejected with specific repair messages; no weakened rules solely to obtain a pass. |
| Preservation | Original finalized records, user-created years, safe deletion, revision conflicts, portable HTML and supported backups remain functional. |

The current audit did not generate the response sets in the round-trip gate. Those are implementation/release tests, not accepted school assessments. Distinguish automatic checks from mathematical review and educator review in the release report. The previous single-witness workflow pass did not establish that every contract-valid encoding would work or that every content label was sound.

## Traceability and evidence

This document supersedes the first-batch backlog as the combined V0.4 repair handoff; the original report remains unchanged for history. A01–A12 preserve its IDs, with expanded locations and the method/output clarification under A02. A13–A16 are newly identified categories. The Count mismatch is merged into A10 rather than counted twice.

Source examined: the supplied packets, `lib/contracts.ts`, `lib/validation.ts`, `lib/task-integrity.ts`, `lib/audit.ts`, `lib/packet.ts`, V0.3 compiler/activation scripts and existing isolated QA examples. No new browser regression or print review is claimed. Prior official standards references are retained for the narrow claims they support.

### Reproduced diagnostic results

| Probe | V0.3 result |
|---|---|
| Change binding responseProduct to request prose | Reviewed evidence remains accepted; no task-integrity finding. |
| Safe SVG double-quoted viewBox | Accepted. |
| Equivalent single-quoted viewBox or tab-separated values | Rejected. |
| Interval label “less than 1” | Accepted. |
| Symbolic interval “0<k<1” | Rejected as Label. |
| Cubic-unit label “cubic centimeter” / “cm³” | Accepted by validator, despite blanket packet no-units instruction. |
| Unit label “cm^3” | Rejected; alias policy not fully specified. |
| Fraction 3/2 for G6 V4 Q10 / V5 Q8 Count | Rejected, despite missing integrality constraints in givens. |
| Fraction 3/2 for G5 V6 Q10 Unitless portion count | Accepted, showing response-domain inconsistency. |
| Native frequency table for G6 V4 Q13 | Rejected, while its existing SVG frequency table passes. |
| Standalone 42 as Expression for G6 V4 Q2 / G5 V6 Q8 | Accepted syntactically despite task-specific output requirements. |

These are diagnostic strings and counterexamples, not generated student-facing items or asserted correct keys.

### Input manifest

Filenames below identify the exact two batches. SHA-256 values identify the audited bytes.

- AAC_TEST-YEAR_G5_V1_Generation_Packet.txt — 6506bae7a3d5d89fa5d9422d464ddf6a20dc7cf66a9fbef5fc70a3efd3ae5176
- AAC_TEST-YEAR_G5_V2_Generation_Packet(1).txt — a55c4bc7cc537ea666e21c7d6e466836adab8aa7486f56fd36deae88577631c2
- AAC_TEST-YEAR_G5_V3_Generation_Packet.txt — 61fc9abd17f7bb3c2a92eec64bf607b128de9c97bb9eecdc2855e3d26e03b04d
- AAC_TEST-YEAR_G5_V4_Generation_Packet.txt — 91a41d9fa5deb5781cd75c1f29dfe1e3bd06206c679e0b3e9b2c5098e35650cc
- AAC_TEST-YEAR_G5_V5_Generation_Packet.txt — 3dfb317c96b7837ba6e36e66a7e94d00297c647004d97d484275c064639c62a8
- AAC_TEST-YEAR_G5_V6_Generation_Packet.txt — c08d19c222cb19bd6203f6d058bffe5a9a86c24bb73be9ca52b380a05574ee6d
- AAC_TEST-YEAR_G5_V7_Generation_Packet.txt — 08747af057507f2c0bb58da1413eab39b5896844ddb1d99503f0c8f21a429bac
- AAC_TEST-YEAR_G5_V8_Generation_Packet.txt — 5c6cb67b1818352fdf4fc76c639260eec821c2d74fcd081fb66129477a5c15d9
- AAC_TEST-YEAR_G6_V1_Generation_Packet.txt — db4248115f2fb14d5599c791d012a3d83341d638861165753b388de742a4c671
- AAC_TEST-YEAR_G6_V2_Generation_Packet.txt — fcb90f90bb7d25aadad3c843a3170c9733238cdd50014ee1dc52ca694b992d36
- AAC_TEST-YEAR_G6_V3_Generation_Packet(1).txt — 32b08dc0145f37d6ec905784cbb5a7e49d183cb58b9636c597f38e11beafa1e9
- AAC_TEST-YEAR_G6_V4_Generation_Packet.txt — 1cf65b1506cd10a534ca2440a84e7e9f6494a686edb299e29bb248b7f9157b7d
- AAC_TEST-YEAR_G6_V5_Generation_Packet.txt — 3e6ab796e6db1199513be79c83603b1c4929884066e72be2e608b328882a5e47
- AAC_TEST-YEAR_G6_V6_Generation_Packet.txt — 287db5b2c1f7d707966a40bbb55d49b17cf04cd924d1713f43d2ff299d47756d
- AAC_TEST-YEAR_G6_V7_Generation_Packet.txt — a092136d2895b6e786e5e2bbfcd4196e25ee7c21214101ad63c8c0f2911ba5d4
- AAC_TEST-YEAR_G6_V8_Generation_Packet.txt — 77de5b9d0f9317d699b090bff10aab1113edc1fd72e674bb7acf19287d75423e
- AAC_TEST-YEAR_G7_V1_Generation_Packet.txt — 06383cefbaa23ccbb30412f668be9056949e3cf1b1a4ec8cb29795bafea8a9f4
- AAC_TEST-YEAR_G7_V2_Generation_Packet(1).txt — 8bc7d35f5381cff8709c0e18bddad0e0fa0cbf04971773eb5f4cc28e57c61582
- AAC_TEST-YEAR_G7_V3_Generation_Packet.txt — c84e6edbb0415bcdc4c8670ccbf272355e6b32fa3ce7fc943cd145a21a71f9db
