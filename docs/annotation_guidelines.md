# Annotation Guidelines — Stage 2C

## 1. Purpose

These guidelines define a reproducible human-review process for the eight unvalidated Academic Voice Auditor pilot rules. They support synthetic pilot-case review and future evaluation design; they do not establish validated ground truth, automated detection behaviour, or performance claims.

## 2. Scope

The guidelines apply only to `ACP-PHR-001`, `ACP-CLM-001`, `ACP-CLM-002`, `ACP-MET-001`, `ACP-STR-001`, `ACP-STR-002`, `ACP-PRT-001`, and `ACP-PRT-002`. Reviewers assess textual and contextual features, not author identity, ability, intent, or use of writing technology. No decision authorises automatic rewriting.

## 3. Annotation unit

The annotation unit is **one rule–passage pair**. Each case names one `primary_rule_id`; the reviewer decides only whether that primary rule applies. A passage may contain `context_before`, one `target_sentence`, and `context_after`. Empty context fields are permitted when the case is intentionally testing whether available context is sufficient.

## 4. Required context

Reviewers must read all three passage fields, the named section, and the complete canonical Trigger and Protected contexts for the primary rule. They should use enough context to judge rhetorical function, evidence alignment, claim scope, attribution, actor materiality, and disciplinary or section convention. They must not assume facts, evidence, sources, or intentions not supplied by the case.

## 5. Annotation decisions

Only four decisions are allowed:

- **FLAG:** The complete Trigger is satisfied, no protected context applies, and a human-review prompt may be appropriate.
- **PROTECT:** A relevant surface feature is present, but a protected context applies, so the prompt should be suppressed.
- **NO_MATCH:** The primary rule does not apply or no candidate surface feature is present.
- **UNCERTAIN:** Available context is insufficient, or the reviewer cannot reliably judge evidence, authorial purpose, disciplinary convention, actor importance, or rhetorical function.

`UNCERTAIN` must not be forced into `FLAG`. `PROTECT` does not mean that the text is perfect; it means only that this rule should not issue a prompt. `FLAG` does not mean that the text is wrong; it means only that a human-review prompt may be appropriate. Every decision evaluates the supplied text and context, never the author's identity or ability.

## 6. Flag-rule procedure

For a rule whose canonical behaviour is `Flag`, identify a candidate feature, test every protected context, and then test the complete contextual Trigger. A term-list or surface-pattern match alone is insufficient. Use `FLAG` only when the complete Trigger is satisfied after protections have been excluded. Use `PROTECT` when the candidate feature is present but a protection applies, `NO_MATCH` when the rule is inapplicable or no candidate exists, and `UNCERTAIN` when the necessary judgement cannot be made from the supplied material.

## 7. Protection-rule procedure

For `ACP-PRT-001` and `ACP-PRT-002`, protection is the default response to legitimate passive voice or functional hedging. The surface feature alone must never cause `FLAG`. Use `PROTECT` when the protection operates normally. Use `FLAG` only when the protection conditions do not apply and the rule's full triggered-review condition is satisfied—for example, a materially important actor appears hidden, or hedges are contradictory, functionally redundant, or meaning-obscuring. Their severity is `Not applicable` even in a provisional `FLAG` case.

## 8. Decision order

1. Confirm the primary Rule ID.
2. Read the complete Trigger and Protected contexts.
3. Check whether a candidate feature is present.
4. If no candidate feature is present, assign `NO_MATCH`.
5. Assess whether the supplied context is sufficient for the required judgement.
6. If context is insufficient, assign `UNCERTAIN`.
7. If context is sufficient, check Protected contexts.
8. If a protection applies, assign `PROTECT`.
9. If no protection applies and the complete Trigger is satisfied, assign `FLAG`.
10. Otherwise assign `NO_MATCH`.

This order prevents a missing candidate from being treated as ambiguity and prevents reviewers from guessing merely to reach a substantive label. Once sufficient context has been established, Protection rules and Protected contexts must be handled before any related surface-pattern warning or user-facing prompt.

## 9. Section-sensitive interpretation

Reviewers must apply the matrix in `references/section_specific_rules.md`. Literature Review attribution, Methodology conventions, Findings denominators and uncertainty, Discussion generalisation, and General Academic Writing context can change a decision. A section label is evidence, not a substitute for rhetorical-function analysis. Mixed-genre passages may warrant `UNCERTAIN` when function cannot be established.

## 10. Handling insufficient context

Use `UNCERTAIN` when missing evidence, neighbouring text, source wording, study scope, procedural roles, disciplinary convention, actor materiality, or rhetorical purpose prevents a reliable decision. Record the specific missing information in the rationale or review notes. Reviewers must not guess evidence, intent, disciplinary convention, actor materiality, or source meaning merely to avoid `UNCERTAIN`. Do not invent support, infer an unnamed actor, assume a citation says something, or use confidence to conceal insufficient context.

## 11. Handling multiple rule matches

Annotate only the named primary rule. A passage that could match another rule remains one rule–passage pair. A reviewer may note a possible secondary match without deciding it in that row; a separate row is required for a separate rule decision. Do not let a secondary concern override a protection under the primary rule.

## 12. Reviewer confidence

Only `High`, `Medium`, and `Low` are permitted. Confidence describes the reviewer's certainty about the decision, not textual risk, rule severity, or author ability. `High` indicates direct contextual support, `Medium` indicates a reasoned decision with a meaningful ambiguity, and `Low` indicates a tentative decision near an operational boundary. `UNCERTAIN` may have any confidence level; for example, a reviewer can have High confidence that context is insufficient.

## 13. Disagreement and adjudication

Future annotation should use at least two reviewers. Reviewers decide independently and must not see one another's first-round decisions. Any decision disagreement enters adjudication. Adjudication must record the final decision and a case-specific reason. Difficult cases must not be deleted to increase agreement. `UNCERTAIN` cases must be retained and used to improve rule wording and context requirements. This workflow is planned; no reviewers have been recruited and no annotation or adjudication has been completed.

## 14. Prohibited annotation behaviour

Reviewers must not:

- label text as AI-authored or infer authorship, identity, competence, or language background;
- treat a common phrase, passive construction, hedge, question, or quantifier as sufficient evidence by itself;
- force `UNCERTAIN` into `FLAG` or use `PROTECT` as a general quality endorsement;
- invent evidence, citations, actors, results, intentions, or disciplinary norms;
- rewrite passages, change claim strength, or prescribe mandatory edits;
- consult another reviewer's first-round answer;
- remove difficult cases to improve apparent agreement; or
- call provisional design expectations validated ground truth.

## 15. Worked synthetic examples

**FLAG — `ACP-PHR-001`:** “This distinction is crucial.” With no supplied consequence or explanation, the complete significance trigger is provisionally satisfied. The label invites review; it does not declare the sentence erroneous.

**PROTECT — `ACP-CLM-001`:** “Every item in the four-item checklist was reviewed.” The universal is explicitly bounded by an enumerated set, so the warning is suppressed.

**UNCERTAIN — `ACP-CLM-002`:** “The analysis confirms the proposed relation.” Without information about the analysis or what “confirms” means in the discipline, the evidence–verb match cannot be judged reliably.

**NO_MATCH — `ACP-STR-002`:** “The next paragraph compares the two definitions.” No question or equivalent rhetorical setup is present, so the primary rule does not match.

**Protection-rule FLAG — `ACP-PRT-001`:** “The borderline records were removed after review.” If surrounding context shows that reviewer discretion affects reproducibility but never identifies the decision-maker, the protection may fail and a human-review prompt may be appropriate. Passive voice alone is not the reason.

## 16. Known limitations

The rules and cases remain unvalidated. Short passages cannot always establish evidential support, source fidelity, actor materiality, rhetorical purpose, or disciplinary convention. Synthetic prose cannot reproduce the diversity and dependencies of authentic academic documents. Section labels may not match function. The case set is deliberately small and balanced by design, so it cannot estimate prevalence or performance. Reviewer guidance may require revision after ethical, permitted human evaluation.

## 17. Stage 2D entry criteria

Stage 2D may begin only after human review confirms all of the following:

- the CSV has exactly 32 rows and eight Rule IDs;
- every Rule ID has exactly four cases and exactly one each of `CLEAR_FLAG`, `CLEAR_PROTECT`, `CLEAR_NO_MATCH`, and `SECTION_SENSITIVE_BOUNDARY`;
- provisional decisions total exactly eight `FLAG`, eight `PROTECT`, eight `NO_MATCH`, and eight `UNCERTAIN`;
- every section-sensitive boundary case genuinely depends on its section or rhetorical function, rather than only carrying a section label;
- every `synthetic` value is `TRUE`;
- all reviewer and adjudication fields remain blank before human annotation;
- the cases contain no real writing, citations, people, or research data;
- decision definitions, sufficiency checking, and protection-first warning suppression are operational;
- reviewer independence, confidence, adjudication, and retention of `UNCERTAIN` cases are accepted; and
- provisional labels are not treated as ground truth, ethical and permission boundaries are explicit, and remaining ambiguities are documented.

The exact balance is a test-suite design for exercising rule boundaries. It cannot estimate real-world prevalence. Stage 2C review readiness is not rule validation, and Stage 2D has not begun.
