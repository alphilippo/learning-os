# Changelog — learning-os

All notable changes to this project are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This project adheres to [Semantic Versioning](https://semver.org/).

## [1.0.0] — 2026-04-21

### Initial release

First public release of `learning-os` — a learning system skill for Claude with 5 modules that enforce verification over consumption.

### Added

#### Core routing system
- `SKILL.md` with module router and linguistic signature triggers
- Composition principle with `thinking-os` and `execution-os` (learning × decision × execution)

#### 5 learning modules
- `learning-path-planner` — plan a 1-3 month learning path with testable checkpoints, observable objective, named external resources, realistic time budget, and final project
- `concept-explainer` — explain a concept with the Feynman method: one-sentence child-level explanation + analogy with its limits + concrete numerical example + historical/contextual framing + non-trivial test question
- `study-session-designer` — structure 30-90 min sessions with observable deliverable, mandatory active recall method (teach-back, blank page, practice, prediction, or elaboration), timed blocks with breaks, non-negotiable wrap-up
- `knowledge-synthesizer` — synthesize 3-10 sources around a central question, map consensus/divergences/blind spots, state confidence level, name assumed biases
- `math-rebuild` — special module for math catchup with 4-level diagnostic, dependency mapping, ordered sequential path, named free resources (Khan Academy, 3Blue1Brown, *Mathematics for Machine Learning*, *Think Stats*), realistic duration estimates, safety rule on math anxiety

#### Templates (reusable markdown)
- Learning plan template
- Concept card template (with spaced repetition dates)
- Study session template
- Synthesis template
- Math diagnostic template

#### Documentation & validation
- 3 end-to-end examples (math rebuild for ML, eigenvalue concept explanation, 1h30 study session on partial derivatives)
- 11 test cases with expected module routing + red flags
- Apache 2.0 license

### Design principles enforced
- No plan without output test
- No explanation without check question
- No session without observable deliverable
- No analogy without its limit
- External sources named precisely (no "a good book" allowed)
- Honest about realistic durations
- Active recall mandatory in study sessions
- Safety rule: math anxiety triggers human-support recommendation

### Known limitations in v1.0
- Trigger descriptions and module content are French-first
- English translation of module bodies on roadmap
- No persistent memory — artifacts must be re-injected between sessions
- No auto-update on outdated resource URLs

### Tested on
- Claude Opus 4.7
- Claude Sonnet 4.6

---

## [Unreleased]

### Planned for v1.1
- Spaced repetition helper (Anki flashcard generation from concept cards)

### Planned for v1.2
- Research mode (deep-learning a single research paper)

### Planned for v1.3
- Language learning module

### Planned for v2.0
- Progress tracker with exported status file for continuity between sessions
