# Rule Design Rationale

## 1. Purpose

This document records the Stage 2A audit of rules inherited from Stop Slop. It explains which general-writing rules may be useful for international postgraduate academic writing, which require academic conditions, which should be excluded, and which need further evidence. It is a design rationale, not a validated rule set, an authorship detector, or an instruction to rewrite text automatically.

The initial context is postgraduate writing in education, TESOL, and the social sciences. Judgements here remain provisional because conventions vary by discipline, genre, institution, section, and rhetorical purpose. No rule in this document has been validated through user research or performance evaluation.

## 2. Design principles

1. Preserve intended meaning, claim strength, evidential scope, and disciplinary terminology.
2. Treat a match as a prompt for judgement, not proof of poor writing and never as evidence of authorship.
3. Prefer explanations and alternatives over automatic deletion or replacement.
4. Condition advice on section, genre, discipline, syntax, and rhetorical function.
5. Distinguish empty emphasis from legitimate stance, hedging, transition, and metadiscourse.
6. Allow passive voice when the process, phenomenon, or result is appropriately foregrounded.
7. Do not invent an actor, claim, example, citation, or causal relationship during revision.
8. Avoid equating brevity, informality, or conversational directness with academic quality.
9. Make uncertainty and exceptions visible to the writer.
10. Require future evidence before converting provisional judgements into executable rules.

## 3. Inherited rule audit method

The audit used `references/phrases.md`, `references/structures.md`, and `references/examples.md` as inherited source material. It read those materials against the project guardrails in `references/do_not_overcorrect.md` and the scope and ethical boundaries in `docs/product_definition.md`. The guardrails shape proposed treatments but are not inherited Stop Slop rules.

Each major inherited category was assigned a unique ID in `docs/inherited_rule_audit.md`. The review asked:

- What problem was the original rule trying to solve?
- Can the same surface form perform a legitimate academic function?
- Could revision change meaning, certainty, cohesion, emphasis, or disciplinary fit?
- Does acceptability depend on section or genre?
- Can a future rule be explained and applied without inventing content?
- What evidence would be needed before implementation?

The examples were treated as illustrations of the inherited philosophy, not as academic evidence. The audit did not modify or endorse the example rewrites.

## 4. Rule classification system

- **Retain**: The original trigger and core treatment remain substantially unchanged. A retained rule may still be presented as an advisory flag with a no-change option, but material changes to trigger, scope, action, or exceptions require Adapt instead.
- **Adapt**: The inherited concern may have value, but its trigger, scope, action, or exceptions are materially changed for academic writing.
- **Reject**: The original rule should not enter the academic rule system.
- **Needs evidence**: No implementation decision should be made yet. Relevant literature, corpus analysis, expert review, or evaluation data must first support a defensible decision.

Classification applies to the original rule as audited. A rejected absolute may still motivate a narrower future rule with a different ID.

## 5. Retained rules

The audit retains four rules whose original triggers and core treatments remain substantially unchanged: performative sincerity or false intimacy, unsupported announcements of difficulty or significance, vague importance claims, and unqualified universal claims. Even retained rules must remain advisory and cannot infer authorship.

The retained rules are `GEN-PHR-007`, `GEN-PHR-008`, `GEN-PHR-009`, and `GEN-STR-017`. Their proposed treatment is documented in the audit table.

## 6. Adapted rules

Most inherited rules require adaptation. Throat-clearing, emphasis crutches, business jargon, filler, metadiscourse, binary contrasts, negative listings, fragments, rhetorical setups, passive voice, Wh-openers, list rhythm, em dashes, rhetorical questions, sentence length, and common academic phrases can all be useful or necessary in academic prose. `GEN-STR-002`, `GEN-STR-003`, and `GEN-STR-016` are Adapt because their triggers, scope, and protected contexts differ materially from the inherited rules.

### Review of the priority absolute rules

#### Delete all adverbs — `GEN-PHR-004`

- **Original rule:** Remove all adverbs, including all `-ly` words, softeners, intensifiers, and hedges.
- **Intended problem:** Empty intensification, vague evaluation, and formulaic emphasis.
- **Academic risk:** Adverbs can encode frequency, degree, manner, stance, limitation, and methodological precision. Removing them can strengthen a cautious claim or change a reported procedure.
- **Classification:** Reject.
- **New rule:** Flag only selected adverbs when they add unsupported emphasis, duplicate meaning, or obscure a more precise description; protect evidential, frequency, degree, and method adverbs.
- **Reasonable exceptions:** “statistically significant,” “partially mediated,” “approximately,” “consistently,” and discipline-specific modifiers.
- **Applicable sections:** All, with particular caution in Methodology, Findings, and Discussion.
- **Possible false positives:** “Participants were randomly assigned” and “scores increased slightly.”

#### Ban all passive voice — `GEN-STR-009`

- **Original rule:** Every sentence needs an actor; rewrite every passive clause in active voice.
- **Intended problem:** Hidden responsibility, vague actors, and flat prose.
- **Academic risk:** Passive voice can appropriately foreground procedure, object, result, or established knowledge. Forced active voice can invent an actor or overuse first person.
- **Classification:** Adapt.
- **New rule:** Flag a passive only when the omitted agent is important to responsibility or interpretation, or when repeated passives impede comprehension.
- **Reasonable exceptions:** Reproducible procedures, conventional method descriptions, agent-irrelevant processes, and result-focused statements.
- **Applicable sections:** Highest caution in Methodology and Findings; more scrutiny where responsibility matters in Discussion or critique.
- **Possible false positive:** “Interviews were transcribed verbatim and coded in two stages.”

#### Ban all Wh- sentence starters — `GEN-STR-010`

- **Original rule:** Avoid sentences beginning with what, when, where, which, who, why, or how.
- **Intended problem:** Repetitive pseudo-clefts and formulaic setup language.
- **Academic risk:** Wh-clauses can organise an argument, state a research question, delimit scope, or connect evidence to interpretation.
- **Classification:** Adapt.
- **New rule:** Flag repeated or vague pseudo-cleft openers such as “What is important is” when a specific subject would be clearer; do not flag Wh-openers by form alone.
- **Reasonable exceptions:** Explicit research questions, embedded question framing, cohesive pseudo-clefts, and definitions.
- **Applicable sections:** Introduction, Literature Review, and Discussion; research-question passages require protection.
- **Possible false positive:** “What remains unclear is whether the effect transfers across contexts.”

#### Ban three-item coordination — `GEN-STR-012`

- **Original rule:** Replace every three-item list with one or two items.
- **Intended problem:** Formulaic rhetorical triads and repetitive cadence.
- **Academic risk:** Three items may reflect the actual categories, variables, stages, or findings. Deletion changes content.
- **Classification:** Reject.
- **New rule:** Never flag a list merely because it contains three items; only consider repetitive ornamental triads when no analytical taxonomy or evidence supports them.
- **Reasonable exceptions:** Exhaustive categories, constructs, research questions, procedural stages, and reported themes.
- **Applicable sections:** All, especially Methodology and Findings.
- **Possible false positive:** “The analysis identified access, identity, and assessment as the three themes.”

#### Ban em dashes — `GEN-STR-015`

- **Original rule:** Remove all em dashes and replace them with commas or periods.
- **Intended problem:** Overused interruption and manufactured emphasis.
- **Academic risk:** An em dash may mark a legitimate parenthetical or clarification; mechanical replacement can create comma splices or alter emphasis.
- **Classification:** Adapt.
- **New rule:** Flag dense or repeated em-dash use when it disrupts formal flow; suggest punctuation based on syntax and the relevant style guide.
- **Reasonable exceptions:** A controlled parenthetical, quoted text, or discipline/style-guide permission.
- **Applicable sections:** All.
- **Possible false positive:** A single syntactically clear parenthetical in a Discussion paragraph.

#### Encourage second-person “you” — `GEN-STR-008`

- **Original rule:** If no specific human actor fits, use “you” to put the reader in the scene.
- **Intended problem:** Distant, abstract, or disembodied prose.
- **Academic risk:** Second person may be too conversational, may generalise the reader's experience, and may violate local conventions.
- **Classification:** Reject.
- **New rule:** Do not introduce “you” as a default repair. Name a supported actor, use an appropriate impersonal construction, or retain the abstraction when it accurately names the analytic object.
- **Reasonable exceptions:** Reflective assignments, practitioner guidance, instructions, and genres that explicitly permit direct reader address.
- **Applicable sections:** Generally avoid as a default throughout conventional research writing.
- **Possible false positive:** “You can observe this pattern in Table 2” in an approved pedagogic genre.

#### Require a human actor in every sentence — `GEN-STR-006`

- **Original rule:** Inanimate subjects create false agency; every sentence should identify a human actor.
- **Intended problem:** Concealed responsibility and vague causal attribution.
- **Academic risk:** Academic writing legitimately makes theories, studies, texts, institutions, processes, and data the grammatical subject. Adding humans can be inaccurate or cumbersome.
- **Classification:** Reject.
- **New rule:** Flag agency only when the verb makes an unsupported causal, intentional, communicative, or evaluative attribution, or when omission hides accountable actors.
- **Reasonable exceptions:** Conventional metonymy (“the study examines”), process descriptions, and accurate descriptions of observed relations.
- **Applicable sections:** All; responsibility claims deserve special scrutiny.
- **Possible false positive:** “The model predicts lower participation under the second condition.”

#### Treat “the data suggest” as false agency — `GEN-STR-007`

- **Original rule:** Data cannot speak; replace expressions such as “the data tell us” with a named human interpreter.
- **Intended problem:** Anthropomorphism and hidden interpretation.
- **Academic risk:** “The data suggest” is conventional evidential metonymy that usefully marks a cautious inference. Replacing it may increase author prominence or alter stance.
- **Classification:** Adapt.
- **New rule:** Permit conventional evidential verbs such as “suggest,” “indicate,” and “show” when calibrated to evidence; flag stronger anthropomorphic or intentional verbs and claims that exceed the analysis.
- **Reasonable exceptions:** Discipline-accepted evidential formulations and concise Findings/Discussion transitions.
- **Applicable sections:** Findings and Discussion.
- **Possible false positive:** “The data suggest that prior experience moderated the association.”

#### Shorten sentences wherever possible — `GEN-STY-001`

- **Original rule:** Prefer compressed, punchy sentences and remove runway.
- **Intended problem:** Wordiness, buried claims, and slow delivery.
- **Academic risk:** Complex relations, qualifications, citations, and methodological detail may require syntactic complexity. Splitting can break logical scope or citation attachment.
- **Classification:** Adapt.
- **New rule:** Flag sentences for review when syntactic load or referential ambiguity impedes comprehension; revise for clarity, not minimum length.
- **Reasonable exceptions:** Carefully controlled complex sentences expressing contrast, conditions, scope, or multi-part procedures.
- **Applicable sections:** All.
- **Possible false positive:** A longer sentence that accurately scopes a cautious claim and its limitations.

#### Delete all common academic phrases — `GEN-STY-002`

- **Original rule:** Remove familiar or generic phrases because they may sound formulaic.
- **Intended problem:** Boilerplate, vague transitions, and prose that announces rather than advances an argument.
- **Academic risk:** Lexical bundles provide cohesion and conventional rhetorical signalling, especially for multilingual writers. Frequency alone does not make a phrase defective or establish anything about authorship.
- **Classification:** Adapt.
- **New rule:** Flag only a defined phrase in a defined context when it is redundant, semantically empty, misleading, or excessively repeated; explain its local function and preserve useful metadiscourse.
- **Reasonable exceptions:** Conventional signposting, cautious framing, definitions, and discipline-specific bundles.
- **Applicable sections:** All, with section-specific expectations.
- **Possible false positive:** “The findings of this study suggest that...” used once to introduce an appropriately cautious interpretation.

#### Avoid all rhetorical questions — `GEN-STR-004`

- **Original rule:** Remove rhetorical setups such as “What if...?” and state the answer directly.
- **Intended problem:** Socratic posturing, manufactured suspense, and conversational scaffolding.
- **Academic risk:** Questions may state research problems, organise inquiry, or serve legitimate pedagogic and theoretical functions.
- **Classification:** Adapt.
- **New rule:** Flag rhetorical questions when they substitute for an argued claim, presume agreement, or create promotional drama; protect genuine research questions and purposeful disciplinary uses.
- **Reasonable exceptions:** Explicit research questions, conceptual problem framing, reflective genres, and quoted source questions.
- **Applicable sections:** Introduction and Discussion; research-question sections require protection.
- **Possible false positive:** “How, then, do novice teachers negotiate these competing expectations?” followed by a literature-based analysis.

#### Avoid all hedging — `GEN-STY-003`

- **Original rule:** Remove softeners and hedges to make claims direct.
- **Intended problem:** Empty qualification, evasiveness, and weak commitment.
- **Academic risk:** Hedging calibrates claims to evidence, marks uncertainty, limits generalisation, and supports responsible scholarly stance. Removal can create false certainty.
- **Classification:** Reject.
- **New rule:** Preserve evidence-calibrated hedging. Flag only stacked, contradictory, or functionless hedges, and never strengthen a claim without evidential justification.
- **Reasonable exceptions:** Epistemic modals, approximators, probability terms, scope limitations, and cautious reporting verbs.
- **Applicable sections:** All, especially Literature Review, Findings, and Discussion.
- **Possible false positive:** “These findings may partly reflect differences in sampling.”

## 7. Rejected rules

Five audit-table rules are classified as Reject: deleting all adverbs (`GEN-PHR-004`), requiring human actors for all clauses (`GEN-STR-006`), defaulting to second person (`GEN-STR-008`), banning three-item lists (`GEN-STR-012`), and deleting hedging (`GEN-STY-003`). In addition, the absolute demand to treat brevity as the governing sentence objective is rejected, while its narrower clarity concern remains classified as Adapt under `GEN-STY-001`.

Rejected rules must not enter the academic rule library in their inherited form. A future narrower rule requires a new, testable specification rather than silent reuse of the absolute.

## 8. Rules requiring evidence

Three areas remain evidence-dependent:

- `GEN-STR-005`: whether specific narrative templates are sufficiently problematic in postgraduate academic genres to justify flags.
- `GEN-STR-014`: whether repeated punch-line paragraph endings can be identified reliably and distinguished from legitimate synthesis.
- `GEN-STY-004`: whether pattern density or co-occurrence is more useful than isolated matches for prioritising review of formulaic prose without over-flagging conventional academic language. This is a research hypothesis derived from inherited rules, not an explicit or validated Stop Slop rule.

Useful evidence could include genre- and section-labelled corpora, published academic-writing research, concordance analysis, qualified reviewer judgements, multilingual-writer review, and documented disagreement. Evidence must address false positives and meaning preservation, not merely pattern frequency.

## 9. Academic exceptions

Cross-cutting exceptions include quotations, titles and headings, source paraphrase constrained by citation accuracy, established technical terms, conventional lexical bundles, explicit research questions, enumerated constructs, reported participant language, methodological procedures, cautious evidence statements, and institutionally prescribed formats.

An exception is not a loophole. It identifies a context in which the form performs a legitimate function. Future rule specifications should define protected contexts where they can be recognised reliably and otherwise present a low-confidence prompt rather than a correction.

## 10. Section-sensitive considerations

- **Introduction:** Allows problem framing, research questions, scope statements, and explicit roadmap metadiscourse. Formulaic importance claims still need concrete support.
- **Literature Review:** Requires reporting verbs, cautious synthesis, contrasts, and source-centred or study-centred subjects. Repetition across many source summaries may still warrant review.
- **Methodology:** Often foregrounds procedures through passive voice, sequencing, precise adverbs, and exhaustive lists. Actor omission matters when researcher choices or responsibility affect interpretation.
- **Findings:** Permits data- and result-centred subjects, calibrated evidential verbs, repeated category labels, and parallel structures that map the analysis.
- **Discussion:** Requires hedging, comparison, limitation, implication, and interpretive metadiscourse. Unsupported significance language and claims exceeding the evidence remain risks.
- **General academic writing:** Genre, discipline, assignment instructions, and institutional style take precedence over a universal preference.

## 11. Risks of overcorrection

The most serious risks are changing epistemic strength, deleting analytically necessary categories, inventing human agents, shifting formal prose into conversational or promotional language, damaging cohesion, breaking citation scope, erasing disciplinary conventions, and treating normal multilingual academic phrasing as suspicious. Automatic shortening may also fragment reasoning; automatic active-voice conversion may misassign responsibility; and phrase blacklists may create false associations with AI authorship.

These risks support an advisory design with visible rationales, exceptions, and a no-change option. No textual feature or combination of features can be treated by this project as proof of AI writing or as a basis for inferring authorship.

## 12. Open questions

- Which academic-writing and corpus studies should support each adapted rule?
- How should “excessive,” “repeated,” “vague,” and “unsupported” be operationalised?
- Which exceptions can be detected reliably from section labels and local syntax?
- How should rules vary across education, TESOL, and adjacent social sciences?
- How should assignment genre and institutional guidance override defaults?
- Which reviewer qualifications and adjudication process are appropriate?
- How should false positives involving multilingual writers be sampled and reported?
- Should co-occurrence influence priority without implying authorship detection?
- How should the system represent low confidence and reviewer disagreement?

## 13. Stage 2B entry criteria

Stage 2B should begin only after human review confirms that:

1. every major inherited category is represented by a unique Rule ID;
2. the four classifications and counts are internally consistent;
3. the twelve priority absolutes have explicit treatments and exceptions;
4. section-sensitive protections for hedging, passive voice, data-centred language, lists, and research questions are adequate for design work;
5. rejected rules are clearly excluded from implementation;
6. evidence-dependent rules remain provisional and have identified evidence needs;
7. no text claims completed user research, validation, precision, recall, or accuracy;
8. the audit aligns with the product's non-detector scope and ethical boundaries; and
9. unresolved disagreements and required expert or literature review are recorded.

Stage 2B must define a formal rule schema containing: Rule ID, Rule name, Category, Unit of analysis, Trigger, Academic risk, Protected contexts, Applicable sections, Severity, User-facing explanation, Suggested action, Do-not-auto-rewrite constraint, Evidence status, Positive example, and False-positive example.

Stage 2B should begin with a pilot of 6–8 rules rather than a complete rule library. Pilot selection must preserve the Stage 2A classifications and evidence limits; selection does not imply that a rule has been validated.

Meeting these criteria makes Stage 2A ready for human review; it does not validate the rules or authorise implementation beyond the limited Stage 2B pilot design.
