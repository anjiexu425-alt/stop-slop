# Academic Voice Auditor

A rule-based academic writing auditor that identifies formulaic and generic AI-style writing patterns while preserving academic hedging, disciplinary conventions, appropriate passive voice, and the writer's intended meaning.

## Target users

Academic Voice Auditor is intended for international postgraduate students writing coursework or dissertations in English. Stage 1 focuses on writing in education, TESOL, and the social sciences.

## The problem

General-purpose AI writing humanisers often apply absolute rules: remove every adverb, prohibit passive voice, shorten sentences indiscriminately, delete appropriate hedging, or make academic prose sound like marketing copy. These changes can distort meaning, erase disciplinary conventions, or introduce claims the writer did not make.

Academic conventions vary across disciplines. A useful auditor must therefore consider section, discipline, rhetorical purpose, and intended level of certainty instead of treating every common feature as an error.

## Proposed solution

The planned product will use transparent, rule-based review to flag potentially formulaic or generic patterns for the writer's consideration. It will distinguish potentially unhelpful habits from legitimate academic language, including cautious claims and appropriate passive constructions in Methodology. It will audit rather than blindly rewrite.

## Current scope

The repository currently covers product definition, ethical boundaries, a high-level skill definition, and the structure for a future academic rule system. All analysis, interface, and evaluation capabilities described as future work are **planned**, not implemented.

## Development status

Stage 1: Product definition and repository restructuring
Status: in progress

The project remains in the product-definition and rule-design stage. There is currently no Python analysis tool, Streamlit application, or web interface. There are no validated accuracy, reliability, or performance results.

## Planned roadmap

- **Stage 1 (in progress):** define the product, boundaries, attribution, and repository structure.
- **Stage 2 (planned):** review and reclassify inherited patterns; design academic, structural, and section-specific rules.
- **Later stages (planned):** develop evaluated examples and an evaluation dataset; prototype analysis tooling only after rules and evaluation criteria are reviewed.

Future evaluation is required before making claims about usefulness, reliability, or performance.

## Project structure

```text
.
├── ATTRIBUTION.md
├── CHANGELOG.md
├── LICENSE
├── README.md
├── SKILL.md
├── docs/
│   ├── evaluation_plan.md
│   ├── product_definition.md
│   └── rule_design_rationale.md
├── examples/
│   ├── findings_example.md
│   ├── literature_review_example.md
│   └── methods_example.md
└── references/
    ├── academic_phrases.md
    ├── academic_structures.md
    ├── do_not_overcorrect.md
    ├── examples.md
    ├── generic_patterns.md
    ├── phrases.md
    ├── section_specific_rules.md
    └── structures.md
```

The original reference files—[phrases](references/phrases.md), [structures](references/structures.md), and [examples](references/examples.md)—are retained as source material pending review. They are not the current academic rule set. New Stage 1 reference scaffolds are described in [SKILL.md](SKILL.md).

## Attribution

Academic Voice Auditor is a redesign and extension of **Stop Slop**, created by **Hardik Pandya** and released under the MIT License. See [ATTRIBUTION.md](ATTRIBUTION.md) for the full attribution and a clear account of current original contributions.

## Limitations

- This project is not an AI detector and cannot determine whether a person or AI wrote a passage.
- It does not promise to reduce any AI-detection score and must not be used to evade institutional or platform detection.
- It must not invent claims, evidence, data, examples, or references.
- It must preserve intended meaning and appropriate academic caution.
- Its rule set is incomplete and unevaluated; future evaluation is required.
- Its initial disciplinary focus is limited, and academic conventions vary across disciplines.

## License

This project retains the original [MIT License](LICENSE). See [ATTRIBUTION.md](ATTRIBUTION.md) for origin and contribution details.
