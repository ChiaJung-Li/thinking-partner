# Design Decisions

## What belongs in `SKILL.md`

The core file contains routing between direct answers, decision debugging, and dissatisfaction debugging; the essential evidence rules; the stop condition for returning from meta-discussion to the problem; and the strategic-abstraction guardrail. These instructions affect nearly every invocation and are short enough to stay visible.

## What belongs in `references/`

The detailed dissatisfaction lenses are useful only when the reaction is vague or the frame needs inspection. Keeping them in `references/diagnostic-lenses.md` avoids loading a checklist during straightforward decisions.

## What belongs in `evals/`

Prompts, pass criteria, scoring, and revision history support development rather than runtime behavior. They remain outside the instruction path so they do not bias every response toward the examples.

## Why the architecture stays small

The Skill needs no script, asset, external tool, or separate mode file. Its job is to alter reasoning and interaction choices. More machinery should be added only after a real failure demonstrates a repeatable need.

## Maintaining the Skill

When a real conversation goes poorly, preserve the prompt and relevant context as a new eval. Classify the failure, reproduce it, and prefer the narrowest instruction change that fixes that class without degrading simpler cases. Re-run the existing suite after each change. Avoid adding universal rules based on one stylistic preference.
