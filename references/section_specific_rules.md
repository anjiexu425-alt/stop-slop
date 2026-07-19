# Section-Specific and Protection Pilot Rules

## Scope and status

This reference contains the canonical formal definitions of pilot rules 7–8 and the section-sensitive application notes for all eight pilot rules. Protection rules suppress indiscriminate warnings; the mere presence of passive voice or hedging must not produce a warning. These are unvalidated pilot rules, and all remaining prompts require human judgement.

## Rule 7 — Methodology passive-voice protection

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-PRT-001` |
| **2. Rule name** | Methodology passive-voice protection |
| **3. Rule behaviour** | Protect |
| **4. Category** | Protection — voice and actor visibility |
| **5. Unit of analysis** | Passive clause, its procedural sentence, and enough surrounding Methodology context to identify whether the actor matters |
| **6. Trigger** | Do not warn merely because passive voice occurs. Protect reasonable passive constructions in Methodology. Prompt human review only when a passive construction appears to hide an important actor whose identity, role, discretion, responsibility, or potential influence is material to interpreting or reproducing the action. |
| **7. Academic risk** | Indiscriminate passive-voice warnings conflict with legitimate methodological convention; selectively hidden actors can nevertheless reduce transparency, accountability, or reproducibility. |
| **8. Protected contexts** | Standard procedure descriptions; focus on materials, samples, or processes; actor already clear from context; actor genuinely irrelevant or unknown; disciplinary convention; anonymisation or ethical constraints; concise descriptions where active voice would add no information. |
| **9. Applicable sections** | Primarily Methodology. The protection may extend to procedural passages elsewhere, but an actor-visibility review should use the section-specific guidance below. |
| **10. Severity** | Not applicable |
| **11. User-facing explanation** | This passive construction may obscure who made a decision or performed an action that matters for interpreting or reproducing the method. Display this explanation only when the full triggered-review condition is satisfied, never when passive voice is protected. |
| **12. Suggested action** | If actor identity materially affects responsibility, discretion, ethics, or reproducibility, clarify it where possible; otherwise retain the passive construction. The user may reject the suggestion. |
| **13. Do-not-auto-rewrite constraint** | Do not automatically delete passive voice, convert it to active voice, invent or infer an actor, expose protected identities, or rewrite the sentence or paragraph. |
| **14. Evidence status** | Unvalidated pilot protection heuristic. Actor-materiality criteria, passive detection, disciplinary practice, and ethical exceptions require expert review and annotated testing. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “The borderline responses were excluded after review.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “The samples were stored at the specified temperature.” |

## Rule 8 — Academic hedging protection

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-PRT-002` |
| **2. Rule name** | Academic hedging protection |
| **3. Rule behaviour** | Protect |
| **4. Category** | Protection — evidential calibration |
| **5. Unit of analysis** | Claim-bearing clause and its local evidential context |
| **6. Trigger** | Do not warn merely because *may*, *might*, *suggest*, *appear*, *likely*, *approximately*, or another hedge occurs. Protect functional evidence calibration. Prompt human review only when hedges are stacked without a distinct function, contradict one another, obscure the claim, or appear to serve no evidential or scope-calibrating purpose. |
| **7. Academic risk** | Removing functional hedging can overstate evidence and alter authorial meaning; excessive or contradictory hedging can make the intended claim difficult to identify. |
| **8. Protected contexts** | Calibrated uncertainty; limitations; approximate quantities; probabilistic inference; cautious source attribution; responsible generalisation; disciplinary convention; multiple markers that perform distinct scope, probability, or attribution functions. |
| **9. Applicable sections** | Literature Review, Methodology, Findings, Discussion, and General Academic Writing, with section-specific interpretation below. |
| **10. Severity** | Not applicable |
| **11. User-facing explanation** | These hedge markers may be contradictory, functionally redundant, or meaning-obscuring. Display this explanation only when the full triggered-review condition is satisfied; normal evidence-calibrating hedging remains protected. |
| **12. Suggested action** | Identify the intended level and source of uncertainty; retain each functional hedge and consider clarifying only redundant or contradictory markers. The user may reject the suggestion. |
| **13. Do-not-auto-rewrite constraint** | Do not automatically delete hedging, strengthen a cautious conclusion into certainty, weaken a claim, substitute certainty markers, or invent evidence, data, or citations. |
| **14. Evidence status** | Unvalidated pilot protection heuristic. Functional stacking, contradiction detection, and discipline-specific calibration require annotated examples and expert evaluation. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “The pattern may perhaps possibly appear likely to reflect a difference.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “The pattern may reflect a difference under the stated conditions.” |

## Section-sensitive application matrix

The matrix governs interpretation; it does not create additional formal rules. “Protect” means suppress a warning unless the full trigger, including contextual risk, is satisfied.

| Pilot rule | Literature Review | Methodology | Findings | Discussion | General Academic Writing |
|---|---|---|---|---|---|
| Unsupported significance claim | Ask whether importance to the synthesis or gap is explained; protect accurately attributed evaluations. | Protect conventional descriptions of essential steps; review evaluative claims about why a design choice matters. | Distinguish statistical significance from unexplained practical or interpretive importance. | Ask for the stated implication, scope, or consequence of importance claims. | Require a contextual reason, not merely an evaluative adjective. |
| Unsupported universal claim | Protect accurately attributed universals while checking whether the review itself generalises beyond sources. | Protect exact statements about an enumerated sample or procedure; check unbounded claims about all participants or contexts. | Closely compare universal scope with reported observations and denominators. | Closely compare generalisation with study scope, conditions, and limitations. | Protect definitions and logical necessities; otherwise review unbounded scope. |
| Overstrong reporting verb | Separate the reviewed source's claimed strength from the writer's endorsement; protect accurate attribution. | Review only when a method or check is said to establish a substantive conclusion; protect procedural uses such as confirming receipt. | Compare verb strength with what the reported analysis establishes. | Check whether interpretation, causality, or generalisation exceeds the described evidence. | Use local evidence and disciplinary meaning; protect logically conclusive uses. |
| Redundant academic metadiscourse | Protect orientation across themes, debates, or bodies of literature; review repetitive low-information announcements. | Protect useful sequence and procedure roadmaps, especially in complex designs. | Protect navigation across analyses or result groups; review announcements that merely duplicate headings. | Protect signposting among interpretations, limitations, and implications. | Apply conservatively at document and major-section openings and where accessibility benefits from signposting. |
| Theatrical binary contrast | Protect genuine theoretical distinctions, competing accounts, and corrections of documented misunderstandings. | Protect explicit comparisons of methods, conditions, and hypotheses; review dramatized false choices. | Protect pre-specified hypothesis or condition comparisons; review binary framing unsupported by reported patterns. | Protect reasoned distinctions; review repeated dramatic opposition that removes nuance. | Require evidence of oversimplification or repetition in addition to the surface form. |
| Formulaic rhetorical setup | Protect genuine conceptual questions and questions organising synthesis. | Protect formal research questions, protocol questions, and analytic questions. | Protect research questions reproduced to organise results; review suspense that delays a result statement. | Protect unresolved interpretive questions that are actually examined. | Review only when the question presumes agreement, creates empty suspense, or delays the proposition. |
| Methodology passive-voice protection | Protect passive descriptions of prior procedures; review actor visibility when attribution affects source interpretation. | Strong protection for conventional procedural passive voice; review only materially hidden responsibility, discretion, ethics, or reproducibility. | Protect passive reporting where actor identity is immaterial; review concealed analytic decisions. | Protect passive references to processes; review when responsibility for an interpretation or recommendation matters. | Protect legitimate information focus; prompt only where a materially important actor is obscured. |
| Academic hedging protection | Protect cautious synthesis, source attribution, and disagreement calibration; review only dysfunctional stacking or contradiction. | Protect uncertainty about sampling, measurement, approximation, and procedural limits. | Protect calibration to estimates, variation, and uncertainty; never strengthen results automatically. | Strongly protect cautious interpretation, limitation, implication, and generalisation. | Protect functional uncertainty and approximation; review only unclear, contradictory, or functionless accumulation. |

## Cross-rule protections

- A protected context overrides a surface-term match unless another part of the full trigger remains satisfied.
- Protection rules do not generate warnings from passive voice or hedging alone.
- Rules assess text features and local context, not author identity, intent, competence, or use of any writing technology.
- No suggestion may automatically add or remove hedging, change claim strength, delete passive voice, rewrite a paragraph, or fabricate actors, evidence, citations, or data.
- Users retain the option to reject every suggestion.
