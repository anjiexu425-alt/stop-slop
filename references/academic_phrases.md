# Academic Phrase and Claim Pilot Rules

## Scope and status

This reference contains the canonical formal definitions of pilot rules 1–4. They evaluate textual features, not author identity. They are unvalidated pilot rules and must not be labelled as detecting “AI-written” text. A match is a prompt for contextual human review, not proof of an error. Common academic language is not problematic merely because it is common.

## Rule 1 — Unsupported significance claim

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-PHR-001` |
| **2. Rule name** | Unsupported significance claim |
| **3. Rule behaviour** | Flag |
| **4. Category** | Phrase and claim — significance language |
| **5. Unit of analysis** | Sentence, read with the surrounding claim and its immediately available support |
| **6. Trigger** | Flag for review when *important*, *significant*, *crucial*, or a close equivalent asserts importance but the text does not state what consequence, scope, decision, interpretation, or affected object makes the claim important. Do not trigger from the marker alone. |
| **7. Academic risk** | An empty significance label can substitute evaluation for an explicit account of why a point matters and can obscure the intended contribution. |
| **8. Protected contexts** | Statistical significance used with a defined statistical meaning; significance explained in the same or adjacent sentence; a clearly scoped disciplinary term; headings or quoted material; a claim whose consequence is explicitly connected to prior context. |
| **9. Applicable sections** | Literature Review, Findings, Discussion, and General Academic Writing. In Methodology, apply only to interpretive claims about the importance of a choice, not to conventional descriptions of essential procedural steps. |
| **10. Severity** | Medium |
| **11. User-facing explanation** | This sentence labels a point as important or significant, but the basis or consequence of that importance may not yet be explicit. |
| **12. Suggested action** | Review the local context and, if useful, state the specific implication or remove the evaluative label. The user may reject the suggestion. |
| **13. Do-not-auto-rewrite constraint** | Do not invent an implication, stakeholder, result, citation, or evidence; do not automatically remove or replace the term; do not rewrite the paragraph. |
| **14. Evidence status** | Unvalidated pilot heuristic. Candidate terms and contextual protections require corpus testing, disciplinary review, and human annotation. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “This distinction is crucial.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “This distinction is crucial because it separates measurement error from conceptual disagreement.” |

## Rule 2 — Unsupported universal claim

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-CLM-001` |
| **2. Rule name** | Unsupported universal claim |
| **3. Rule behaviour** | Flag |
| **4. Category** | Phrase and claim — scope and certainty |
| **5. Unit of analysis** | Claim-bearing sentence, checked against its local evidence, quantifiers, population, and stated scope |
| **6. Trigger** | Flag for review when *always*, *never*, *everyone*, *nobody*, or a close universal quantifier makes an unrestricted claim whose scope is not supported or bounded in the local text. Do not trigger solely because a universal term appears. |
| **7. Academic risk** | Universal wording can extend a claim beyond the population, conditions, or evidence described and may misrepresent the intended level of certainty. |
| **8. Protected contexts** | Definitions and logical necessities; explicitly bounded universals; accurately attributed or quoted claims; negated discussion of a universal claim; instrument instructions; universal terms supported by the stated domain (for example, every item in an enumerated set). |
| **9. Applicable sections** | Literature Review, Findings, Discussion, and General Academic Writing. Use heightened scope checking in Findings and Discussion. In Methodology, protect exact statements about fully enumerated procedures or samples. |
| **10. Severity** | High |
| **11. User-facing explanation** | This universal wording may extend the claim beyond the evidence or scope stated in the text. |
| **12. Suggested action** | Check whether the universal scope is intended and evidenced; clarify the population or conditions if needed. The user may retain the wording. |
| **13. Do-not-auto-rewrite constraint** | Do not automatically add a hedge, change a quantifier, narrow the population, alter claim strength, or invent evidence or citations. |
| **14. Evidence status** | Unvalidated pilot heuristic. Universal-term coverage, scope resolution, and section thresholds require annotated examples and disciplinary testing. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “These approaches always improve interpretation.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “Every item in the four-item checklist was reviewed.” |

## Rule 3 — Overstrong reporting verb

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-CLM-002` |
| **2. Rule name** | Overstrong reporting verb |
| **3. Rule behaviour** | Flag |
| **4. Category** | Phrase and claim — evidential strength |
| **5. Unit of analysis** | Reporting clause and its attributed evidence or proposition, with sentence-level and adjacent context |
| **6. Trigger** | Flag for review when *prove*, *confirm*, *demonstrate*, or a close high-certainty reporting verb appears to claim stronger support, causality, or conclusiveness than the described evidence warrants. Trigger requires an apparent evidence–verb mismatch, not a word-list match. |
| **7. Academic risk** | A reporting verb can overstate what data, a source, or an analysis establishes, changing evidential strength or attribution. |
| **8. Protected contexts** | Mathematically or logically established propositions; accurate attribution of a source's wording; descriptions of a verification procedure; genuinely conclusive evidence within an explicitly bounded claim; reasonable uses of *suggest*, *indicate*, and *show* that match the evidence and disciplinary convention. |
| **9. Applicable sections** | Literature Review, Findings, Discussion, and General Academic Writing. In Methodology, apply only where a method or check is said to establish a substantive conclusion. Apply especially carefully to inference in Findings and Discussion. |
| **10. Severity** | High |
| **11. User-facing explanation** | The reporting verb may express more certainty or conclusiveness than the accompanying evidence supports. |
| **12. Suggested action** | Compare the verb with the evidence and intended claim; revise only if the strength is mismatched. The user may reject the suggestion. |
| **13. Do-not-auto-rewrite constraint** | Do not automatically substitute a weaker or stronger verb, add hedging, change causal meaning, or invent supporting evidence, data, or citations. |
| **14. Evidence status** | Unvalidated pilot heuristic. Verb-strength rankings and evidence-matching criteria need disciplinary review and annotated corpus evaluation. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “A limited comparison proves that the framework applies in every setting.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “The derivation proves the identity under the stated assumptions.” |

## Rule 4 — Redundant academic metadiscourse

| Field | Definition |
|---|---|
| **1. Rule ID** | `ACP-MET-001` |
| **2. Rule name** | Redundant academic metadiscourse |
| **3. Rule behaviour** | Flag |
| **4. Category** | Phrase and claim — metadiscourse |
| **5. Unit of analysis** | Sentence and neighbouring paragraph or section-opening sentences |
| **6. Trigger** | Flag for review when repeated or low-information phrases such as “This section will…” merely announce content that is immediately obvious and add no useful sequence, purpose, relationship, or navigation. A single roadmap phrase is insufficient to trigger. |
| **7. Academic risk** | Repetitive announcements can delay substantive content and reduce clarity, while indiscriminate removal could damage navigation. |
| **8. Protected contexts** | Thesis or article roadmaps; chapter and section orientation; transitions that explain sequence or argumentative function; accessibility-supporting signposting; complex documents where navigation is useful; required genre conventions. |
| **9. Applicable sections** | Literature Review, Methodology, Findings, Discussion, and General Academic Writing. Apply more conservatively at document, chapter, and major-section openings. |
| **10. Severity** | Low |
| **11. User-facing explanation** | This signposting may repeat information without adding a clear navigational or argumentative function. |
| **12. Suggested action** | Check whether the sentence helps readers follow purpose, order, or relationships; keep it if it does, or consider condensing it. The user may reject the suggestion. |
| **13. Do-not-auto-rewrite constraint** | Do not automatically delete signposting, merge paragraphs, rewrite the section, or assume a conventional phrase is wrong because it is common. |
| **14. Evidence status** | Unvalidated pilot heuristic. Repetition windows, information-value criteria, genre expectations, and accessibility effects require human evaluation. |
| **15. Trigger-positive synthetic example** | **Synthetic example:** “This section will now discuss the issues that this section addresses.” |
| **16. Protected / false-positive synthetic example** | **Synthetic example:** “This section first defines the construct, then distinguishes it from the measure used in the analysis.” |
