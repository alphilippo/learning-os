# learning-os

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-Apache%202.0-green) ![Claude](https://img.shields.io/badge/Claude-Skill-purple)

🌍 **[Français](README.md)** · **English**

> A learning system for Claude: turns curiosity into mastery via 5 modules that enforce verification over consumption.

## What it does

Most people confuse **exposure** with **mastery**. They read a book, watch a video, and think they've learned something. They haven't learned — they've consumed.

`learning-os` applies 4 hard principles:

1. **No plan without an output test** — every plan includes checkpoints where you prove what you know
2. **No explanation without a check question** — every explained concept ends with a test question
3. **No session without an observable deliverable** — exercises solved, concept explained in writing, code that runs
4. **No analogy without its limit** — analogies are useful but dangerous; the skill always names where they break

## The 5 modules

| Module | When to use |
|---|---|
| **Learning Path Planner** | Start a new domain over 1-3 months |
| **Concept Explainer** | Stuck on a specific concept |
| **Study Session Designer** | 30-90 min session with a goal |
| **Knowledge Synthesizer** | Synthesize multiple sources |
| **Math Rebuild** | Math catchup with diagnostic + ordered path |

## Triggers

The skill triggers automatically when you say:
- *"I want to learn X"*, *"where to start"* → Learning Path Planner
- *"Explain X to me"*, *"I don't get X"*, *"what is X really"* → Concept Explainer
- *"I have 1h to study"*, *"session on X"* → Study Session Designer
- *"Synthesize these sources"*, *"I read several articles on X"* → Knowledge Synthesizer
- *"I want to catch up on math"*, *"I have gaps in math"* → Math Rebuild

## Complementary skills (full ecosystem)

- 🧠 [**thinking-os**](https://github.com/alphilippo/thinking-os) — cognitive router
- ⚙️ [**execution-os**](https://github.com/alphilippo/execution-os) — execution system
- 📚 [**learning-os**](https://github.com/alphilippo/learning-os) — learning system
- ⚔️ [**strategy-intel**](https://github.com/alphilippo/strategy-intel) — strategic analysis
- 🧭 [**alignment-os**](https://github.com/alphilippo/alignment-os) — personal alignment

The 5 answer different questions:
- `thinking-os` — **WHAT** to do (thinking frame)
- `execution-os` — **HOW** to do it (cadence)
- `learning-os` — **HOW TO LEARN** it (skill building)
- `strategy-intel` — **WHERE & AGAINST WHOM** to do it (positioning)
- `alignment-os` — **WHY** do it (life/values coherence)

## Installation

### Claude.ai

1. Download the ZIP from GitHub (Code → Download ZIP) or clone the repo
2. Ensure the ZIP structure contains the `learning-os/` folder at root (not files directly)
3. In Claude.ai: Settings → Skills → "+" → "+ Create skill" → upload the ZIP
4. Toggle the skill ON

### Claude Code

```bash
cp -r learning-os ~/.claude/skills/
```

### Claude API

Package as `.skill` and upload via the `/skills` endpoint. See [official docs](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).

## Examples

### Math catchup
> *"I want to catch up on math to understand ML papers. Science bac 15 years ago, I forgot everything."*

→ The skill forces a **4-level diagnostic** before planning, identifies the real entry point (often lower than the user thinks), proposes a 6-month sequential path with specific free resources (Khan Academy, 3Blue1Brown, *Mathematics for Machine Learning*).

### Explaining a fuzzy concept
> *"I don't understand what an eigenvalue is."*

→ The skill **diagnoses the missing prerequisite** (often the intuition of linear transformations), explains with analogy + numerical example + limits, ends with a test question without giving the answer.

### Stuck session
> *"I have 1h30 to solidify partial derivatives, I read 2 chapters but it's not sticking."*

→ The skill identifies the **method problem** (exposure without active recall), structures a session with blank page recall + specific exercises + observable deliverable (1-page document).

## Structure

```
learning-os/
├── SKILL.md                         # Metadata + router
├── README.md                        # French version
├── README.en.md                     # This file
├── modules/
│   ├── learning-path-planner.md
│   ├── concept-explainer.md
│   ├── study-session-designer.md
│   ├── knowledge-synthesizer.md
│   └── math-rebuild.md
├── templates/
│   ├── learning-plan-template.md
│   ├── concept-card-template.md
│   ├── study-session-template.md
│   ├── synthesis-template.md
│   └── math-diagnostic-template.md
├── examples/
│   ├── math-rebuild-example.md
│   ├── concept-explainer-example.md
│   └── study-session-example.md
└── tests/
    └── test-cases.md                # 11 validation cases
```

## Philosophy

- **Progressive disclosure**: the SKILL.md only contains the router.
- **No passive consumption**: the skill refuses to produce a simple summary without testing.
- **External sources named**: not "a good book", always a precise title/author/platform.
- **Exportable artifacts**: every output is a structured markdown you can save.
- **Humility**: the skill doesn't replace real practice (exercises, projects, human feedback) nor a human tutor.

## Limitations

- No memory between sessions — you need to re-inject your plans/notes
- Doesn't replace practice (exercises, projects, feedback)
- Recommended resources may be outdated (to verify)
- Some key resources are English-only
- For math, a human tutor remains strongly recommended as a complement for deep blockages

> **Note**: Content in French (modules, templates, examples) is currently the reference version. English translation of module bodies is on the roadmap.

## Roadmap

- **v1.0** (current): 5 modules + 5 templates + routing
- **v1.1**: **Spaced repetition helper** (module to generate Anki flashcards from concept cards)
- **v1.2**: **Research mode** (module for deep-learning a research paper)
- **v1.3**: **Language learning** (specific language-learning module)
- **v2.0**: **Progress tracker** that remembers between sessions via an exported status file

## License

Apache 2.0 — fork, adapt, republish.

## Credits

Built with Claude as Skill Architect. Inspired by the Feynman method, Anders Ericsson (deliberate practice), Peter Brown (*Make It Stick*), and 3Blue1Brown (visual intuition in math).
