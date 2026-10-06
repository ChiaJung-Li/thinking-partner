# Thinking Partner

Thinking Partner is a personal Codex Skill for improving the quality of reasoning—not merely producing a more polished answer.

It helps with two recurring situations:

- **Decision and assumption debugging:** separate observations from interpretations, compare competing explanations, and choose a decision-relevant next test.
- **Dissatisfaction debugging:** diagnose why an answer feels shallow, too tactical, incomplete, `怪怪的`, or `格局不夠高` before rewriting it.

The Skill stays lightweight for straightforward questions and uses deeper analysis only when uncertainty or complexity warrants it.

## Install

Clone the repository into your personal Codex Skills directory:

```bash
git clone https://github.com/ChiaJung-Li/thinking-partner.git ~/.codex/skills/thinking-partner
```

If you already cloned it elsewhere, copy the repository folder instead:

```bash
cp -R /path/to/thinking-partner ~/.codex/skills/thinking-partner
```

Start a new Codex task after installation so the Skill can be discovered.

## Use

Invoke it explicitly:

```text
Use $thinking-partner to examine whether my hypothesis is actually supported.
```

Or use it to diagnose a reaction before revising an answer:

```text
Use $thinking-partner. This answer isn't wrong, but the 格局 feels too small. Help me diagnose why before rewriting it.
```

Codex can also select the Skill automatically when a request matches its description.

## Structure

```text
thinking-partner/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── diagnostic-lenses.md
└── evals/
    ├── cases.yaml
    ├── rubric.md
    ├── v0.1-review.md
    └── design-decisions.md
```

- `SKILL.md` contains the core routing and reasoning behavior.
- `references/` contains diagnostic detail loaded only when relevant.
- `evals/` documents behavioral cases, scoring, and the reasoning behind revisions.

## Design principle

> Improve the user's thinking, not merely the answer.

Iteration is treated as part of reasoning. A user's disagreement or vague dissatisfaction is additional evidence—not a failed interaction.

## License

MIT
