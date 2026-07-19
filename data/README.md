# Stage 2C pilot annotation data

`pilot_annotation_cases.csv` is a design artifact for reviewing the annotation guidelines and the boundaries of eight unvalidated pilot rules. It contains 32 synthetic rule–passage pairs and no real student writing, participant data, research findings, or real citations.

## Columns

- `case_id`: unique identifier from `AVA-C001` to `AVA-C032`.
- `primary_rule_id`: the only rule decided for the row.
- `case_design_type`: why the synthetic case was designed; one of `CLEAR_FLAG`, `CLEAR_PROTECT`, `CLEAR_NO_MATCH`, or `SECTION_SENSITIVE_BOUNDARY`. This is separate from the provisional expected decision.
- `rule_behaviour`: canonical `Flag` or `Protect` behaviour.
- `section`: intended academic section or writing context.
- `context_before`: synthetic text immediately before the target; may be empty.
- `target_sentence`: sentence or passage targeted for the decision.
- `context_after`: synthetic text immediately after the target; may be empty.
- `surface_feature`: candidate textual feature relevant to the primary rule.
- `provisional_expected_decision`: Stage 2C design expectation, not validated ground truth.
- `provisional_rationale`: why the provisional decision was designed.
- `protected_context`: applicable protection, or `None identified` where none is designed.
- `severity_if_flagged`: canonical severity for Flag rules; `Not applicable` for Protect rules.
- `synthetic`: always `TRUE` in this dataset.
- `reviewer_1_decision`, `reviewer_2_decision`: reserved for independent future decisions.
- `reviewer_1_confidence`, `reviewer_2_confidence`: reserved for `High`, `Medium`, or `Low` confidence.
- `adjudicated_decision`: reserved for a future final decision after disagreement review.
- `adjudication_notes`: reserved for the future adjudicator's case-specific reason.

## Decision definitions

- `FLAG`: the complete Trigger applies, no protection applies, and a human-review prompt may be appropriate.
- `PROTECT`: a relevant surface feature exists but a protected context applies, so the prompt is suppressed.
- `NO_MATCH`: the primary rule is inapplicable or no candidate feature exists.
- `UNCERTAIN`: supplied context is insufficient for a reliable judgement.

`FLAG` does not mean “wrong,” and `PROTECT` does not mean “perfect.” `UNCERTAIN` must not be forced into `FLAG`. The provisional labels are case-design expectations only, not validated ground truth. All reviewer and adjudication fields are currently blank because no annotation has occurred.

## Test-suite balance and validation

The dataset must retain exactly 32 rows, eight Rule IDs, and four cases per Rule ID. Every rule must have exactly one of each `case_design_type`. The provisional decision totals must be eight `FLAG`, eight `PROTECT`, eight `NO_MATCH`, and eight `UNCERTAIN`. Every `SECTION_SENSITIVE_BOUNDARY` must genuinely depend on section or rhetorical function and state what information is missing. All `synthetic` values must be `TRUE`, all reviewer and adjudication fields must remain blank before annotation, and no row may contain real writing, citations, people, or research data.

This exact balance is a test-suite design for exercising rule boundaries. It cannot estimate the prevalence of these features or decisions in real-world writing.

This dataset must not be used for AI authorship detection or claims about writer identity or ability. Before real cases are added, the project requires appropriate ethical, privacy, permission, consent or lawful-basis, de-identification, retention, and governance review.
