# Academic Rule Pilot Specification — Stage 2B

## 1. Pilot purpose

Stage 2B defines a deliberately small set of eight unvalidated academic-writing review rules. The pilot tests whether a common 16-field schema can express rule behaviour, triggers, academic risks, protected contexts, section sensitivity, user-facing guidance, and hard limits on automatic rewriting. It designs rules only: it provides no implementation, evaluation dataset, user-research result, or accuracy, precision, or recall claim.

The pilot evaluates textual features. It does not infer author identity and does not use “AI-written” as a rule label or conclusion.

## 2. Rule selection rationale

The set samples four complementary design problems:

- claim scope and evidential strength;
- phrase-level significance and metadiscourse;
- sentence and discourse structures that may be useful or formulaic depending on context;
- explicit protections for passive voice and academic hedging.

These cases were selected because a simple term or pattern list would create foreseeable false positives. Together they test whether triggers can depend on academic function, evidence alignment, neighbouring context, document section, and protected usage rather than frequency alone.

## 3. Formal rule schema

Every canonical pilot rule contains exactly these 16 fields:

1. Rule ID
2. Rule name
3. Rule behaviour
4. Category
5. Unit of analysis
6. Trigger
7. Academic risk
8. Protected contexts
9. Applicable sections
10. Severity
11. User-facing explanation
12. Suggested action
13. Do-not-auto-rewrite constraint
14. Evidence status
15. Trigger-positive synthetic example
16. Protected / false-positive synthetic example

`Rule behaviour` permits only `Flag` or `Protect`. A `Flag` rule may produce a human-review prompt when its full contextual trigger is satisfied. A `Protect` rule is evaluated first to suppress a surface-pattern warning in protected contexts and permits a prompt only when its explicit triggered-review condition is satisfied.

The example fields have distinct semantics:

- **Trigger-positive synthetic example:** A synthetic example in which the full contextual trigger is intended to be satisfied and a human-review prompt may be appropriate.
- **Protected / false-positive synthetic example:** A synthetic example that contains a surface feature associated with the rule but should not generate a prompt because a protected context applies or the full trigger is not satisfied.

Every example is written solely for rule demonstration, explicitly labelled `Synthetic example`, and is not presented as real student writing.

Canonical formal definitions live in the three reference files. This specification indexes and governs them without duplicating their formal definitions.

## 4. List of eight pilot rules

| Rule ID | Pilot rule | Rule behaviour | Canonical file |
|---|---|---|---|
| `ACP-PHR-001` | Unsupported significance claim | Flag | `references/academic_phrases.md` |
| `ACP-CLM-001` | Unsupported universal claim | Flag | `references/academic_phrases.md` |
| `ACP-CLM-002` | Overstrong reporting verb | Flag | `references/academic_phrases.md` |
| `ACP-MET-001` | Redundant academic metadiscourse | Flag | `references/academic_phrases.md` |
| `ACP-STR-001` | Theatrical binary contrast | Flag | `references/academic_structures.md` |
| `ACP-STR-002` | Formulaic rhetorical setup | Flag | `references/academic_structures.md` |
| `ACP-PRT-001` | Methodology passive-voice protection | Protect | `references/section_specific_rules.md` |
| `ACP-PRT-002` | Academic hedging protection | Protect | `references/section_specific_rules.md` |

## 5. Severity definitions

Flag rules may use only the following severity values:

- **Low:** minor style issue; revision may not be necessary.
- **Medium:** may affect clarity, accuracy, or academic tone.
- **High:** may change evidential strength, authorial meaning, or an academic-integrity boundary.

Severity describes the consequence of a confirmed flagged concern. It is not a confidence score and does not override protected contexts. Protection rules use **Not applicable** because they do not issue warnings when protection applies. The risk of incorrect intervention is documented in `Academic risk` and `Do-not-auto-rewrite constraint`, not encoded as High severity.

The pilot distribution is Low: 2 Flag rules, Medium: 2 Flag rules, High: 2 Flag rules, and Not applicable: 2 Protection rules.

## 6. Protection-rule behaviour

Protection rules are evaluated before surface-pattern Flag rules and before any user-facing prompt. A surface match to passive voice or a hedge does not generate a warning. The passive-voice rule protects conventional Methodology prose and permits a review prompt only when an important actor may be hidden; its triggered-review explanation is not displayed when protection applies. The hedging rule protects normal evidence calibration and permits a review prompt only when markers appear contradictory, functionally redundant, or meaning-obscuring.

Protected contexts in every rule have the same suppressive role. For example, statistical significance, bounded universals, conclusive logical proof, useful roadmaps, genuine theoretical distinctions, and formal research questions must not be treated as violations merely because they resemble a candidate pattern.

The system must not automatically delete passive voice or hedging, add a hedge, or lower or increase claim strength.

## 7. Human-review requirements

Every pilot output is advisory and rejectable. A reviewer must inspect enough context to assess rhetorical function, evidence alignment, scope, attribution, disciplinary convention, and document section. Review is specifically required before:

- deciding that significance is unsupported;
- treating a universal as outside the available evidence;
- judging the strength of a reporting verb;
- deciding that signposting is redundant;
- classifying contrast as theatrical or oversimplified;
- distinguishing a rhetorical setup from a genuine question;
- deciding that an unnamed actor is material;
- deciding that multiple hedges lack distinct functions or conflict.

No pilot rule authorises whole-paragraph rewriting or the fabrication of actors, evidence, references, data, findings, or implications. Common academic phrases are not errors merely because they are frequent. No suggestion is mandatory.

## 8. Known limitations

- Local context may be insufficient to determine evidential support, authorial intent, or actor materiality.
- Section labels and rhetorical functions may not align, particularly in mixed or non-IMRaD genres.
- Terminology, acceptable certainty, passive-voice practice, and signposting conventions vary by discipline, language background, venue, and genre.
- The candidate lexical examples are not exhaustive and may be polysemous.
- Quotation, attribution, negation, mathematical reasoning, and statistical terminology complicate surface matching.
- Accessibility needs and long-document navigation can make repeated signposting useful.
- The pilot does not specify detection algorithms, thresholds, context-window size, or conflict resolution between multiple matched rules.
- The synthetic examples demonstrate rule boundaries but are not evaluation data.

## 9. Evidence gaps

The pilot has not been validated against real student writing, expert annotations, disciplinary corpora, or user decisions. It lacks:

- agreed annotation guidance and inter-rater evidence;
- estimates of false-positive and false-negative behaviour;
- accuracy, precision, recall, calibration, or coverage measurements;
- discipline- and section-specific threshold evidence;
- validated inventories of significance terms, universal quantifiers, reporting verbs, rhetorical patterns, passive constructions, and hedges;
- evidence that the proposed explanations and suggestions are understandable, useful, or non-coercive;
- evidence about accessibility, multilingual writing, and unintended differential impact;
- user research on whether protections preserve meaning in practice.

No performance or user-research claim should be inferred from this specification.

## 10. Stage 2C entry criteria

Stage 2C must not begin until a human review confirms all of the following:

1. Each canonical rule has all 16 fields.
2. Rule IDs, categories, `Flag` and `Protect` Rule behaviour values, severity values, and canonical file ownership are accepted.
3. Human reviewers approve the execution order in which Protect rules are evaluated before surface-pattern Flag rules.
4. Protection rules use `Severity: Not applicable`, while Flag-rule severity describes the consequence of a confirmed concern rather than confidence.
5. Trigger and protection language is sufficiently operational for the next-stage scope.
6. The definitions of trigger-positive synthetic examples and protected / false-positive synthetic examples are accepted, and each canonical rule includes one of each.
7. Section differences for Literature Review, Methodology, Findings, Discussion, and General Academic Writing are accepted.
8. Do-not-auto-rewrite constraints and user refusal rights are explicit and internally consistent.
9. Remaining ambiguities and evidence gaps are documented and judged acceptable for progression.
10. Reviewers approve a Stage 2C plan without treating these pilot rules as validated or expanding them into a full rule library.

Stage 2B ends with human-review readiness, not with implementation or validation.
