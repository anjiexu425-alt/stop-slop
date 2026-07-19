# Evaluation Plan — Stage 2C

## 1. Evaluation purpose

This plan defines how the eight unvalidated pilot rules could be evaluated through contextual human review. It assesses rule behaviour and protections, not AI authorship, writer identity, or writer ability.

## 2. Current evaluation status

No real annotation, user study, or empirical evaluation has been conducted. No reviewers have been recruited. There are no accuracy, precision, recall, raw-agreement, or other agreement results. Stage 2C supplies guidance and synthetic design cases only.

## 3. Pilot rules

The scope is limited to the six Flag rules (`ACP-PHR-001`, `ACP-CLM-001`, `ACP-CLM-002`, `ACP-MET-001`, `ACP-STR-001`, `ACP-STR-002`) and two Protect rules (`ACP-PRT-001`, `ACP-PRT-002`) defined in the existing canonical reference files. Evaluation must use their complete triggers, protections, section guidance, and do-not-auto-rewrite constraints without changing the rules.

## 4. Pilot case design

`data/pilot_annotation_cases.csv` contains 32 wholly synthetic cases: exactly four distinct cases per rule. `case_design_type` records why a case exists and is separate from `provisional_expected_decision`, which records the design-stage expected outcome. Each Rule ID has exactly one `CLEAR_FLAG`, one `CLEAR_PROTECT`, one `CLEAR_NO_MATCH`, and one `SECTION_SENSITIVE_BOUNDARY`. Their associated provisional decisions are respectively `FLAG`, `PROTECT`, `NO_MATCH`, and `UNCERTAIN`, producing eight of each decision overall. The cases cover Literature Review, Methodology, Findings, Discussion, and General Academic Writing. This exact balance is a test-suite design for exercising rule boundaries and cannot estimate real-world prevalence.

## 5. Annotation process

The unit is one rule–passage pair. Reviewers read the primary rule, complete Trigger and Protected contexts, all supplied passage context, and the section. They first determine whether a candidate exists, then assess context sufficiency, and only with sufficient context test protections before issuing any warning. They choose only `FLAG`, `PROTECT`, `NO_MATCH`, or `UNCERTAIN`. Future rounds should use at least two independent reviewers who cannot see one another's initial decisions.

## 6. Provisional design labels

`provisional_expected_decision` records a case author's Stage 2C expectation for checking case coverage and guideline clarity. It is not validated ground truth and must not be scored as if it were an expert gold label. It may be revised through documented human review.

`case_design_type` is independent design metadata. Its allowed values are `CLEAR_FLAG`, `CLEAR_PROTECT`, `CLEAR_NO_MATCH`, and `SECTION_SENSITIVE_BOUNDARY`. It explains which test-suite role the case was constructed to serve; it is not a reviewer decision, confidence value, or empirical result.

## 7. Reviewer roles

Reviewer 1 and Reviewer 2 will independently record a decision and `High`, `Medium`, or `Low` confidence. Confidence measures certainty in the decision, not risk or severity. A future adjudicator will examine disagreements without erasing the independent records. These are planned roles, not completed appointments.

## 8. Disagreement resolution

All decision disagreements proceed to adjudication. The adjudicator records a final decision and reason, including the relevant Trigger, protection, missing context, or section convention. Difficult and `UNCERTAIN` cases remain in the dataset and inform revisions to operational definitions or context requirements; they are not removed to inflate agreement.

## 9. Planned measurements

Future, appropriately authorised evaluation may report:

- Raw agreement
- Rule-level precision
- Rule-level recall
- False-positive review
- False-negative review
- Protection suppression accuracy
- `UNCERTAIN` rate
- Results by section
- Results by rule
- Disagreement categories

Cohen's kappa may be considered as an optional future agreement measure if its assumptions suit the design. It has not been calculated. No metric results are available at Stage 2C.

## 10. Rule-level error analysis

Future analysis should separate missed candidate features from incorrect contextual decisions. Categories should include protection overlooked, Trigger incomplete, evidence–claim mismatch misjudged, scope boundary misread, rhetorical function misclassified, actor materiality disputed, section convention misapplied, and insufficient context. Findings should be reported per rule rather than collapsed into a single headline score.

## 11. Protection-rule evaluation

Evaluation must measure both appropriate suppression and inappropriate suppression. For `ACP-PRT-001`, passive voice alone is never a positive error condition; reviewers must assess whether actor identity materially affects responsibility, discretion, ethics, interpretation, or reproducibility. For `ACP-PRT-002`, hedging alone is never a positive error condition; reviewers must distinguish functional calibration from contradictory, redundant, or meaning-obscuring accumulation. Protection-rule severity remains `Not applicable`.

## 12. Fairness and multilingual-writer considerations

Future evaluation should examine whether explanations, context requirements, and false-positive patterns differ by discipline, genre, accessibility need, or language background without treating those attributes as textual defects. Reviewers must not infer identity or competence from prose. Common academic phrasing and legitimate variation require protection, and no case may be used to detect AI authorship.

## 13. Data limitations

All 32 current cases are synthetic and intentionally constructed around rule boundaries. They contain no real student papers, participants, findings, or citations. The small balanced set cannot estimate real-world frequency, generalisability, calibration, or performance and does not represent disciplinary or multilingual diversity.

## 14. Ethical boundaries

The pilot evaluates text features only. It must not be used for AI authorship detection, surveillance, grading, disciplinary action, or claims about a writer. Suggestions remain advisory and rejectable. Before any authentic writing is added, the project requires appropriate ethics, privacy, data-permission, retention, consent or lawful-basis, de-identification, and governance review. No evidence, actors, citations, or results may be fabricated.

## 15. Stage 2D plan

Stage 2D is future work and has not begun. Entry requires human confirmation of exactly 32 rows, eight Rule IDs, four cases per Rule ID, and exactly one of each allowed `case_design_type` per Rule ID. The decision distribution must be eight `FLAG`, eight `PROTECT`, eight `NO_MATCH`, and eight `UNCERTAIN`; every section-sensitive boundary must genuinely depend on section or rhetorical function; all `synthetic` values must be `TRUE`; reviewer and adjudication fields must be blank before annotation; and the cases must contain no real writing, citations, people, or research data. Entry also requires approval of the guidelines, schema, context-sufficiency and protection-first decision order, ethical boundaries, and documented ambiguities. A later plan may refine cases and reviewer training before any properly authorised authentic-data evaluation; it must continue to separate provisional design labels from validated reference decisions and report limitations alongside any future measurements.
