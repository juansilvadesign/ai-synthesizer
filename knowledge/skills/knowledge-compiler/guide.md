# Compile: Guide

Use when the source is a practitioner-oriented procedural document — playbook, framework write-up, how-to, checklist, methodology paper, internal handbook chapter.

## What makes guides different

- **Procedural shape, not argumentative.** A guide tells you *how to do X* in a specific order. Preserve the order; don't rearrange into prose.
- **The trigger matters as much as the procedure.** Guides answer "when do I reach for this?" — capture that explicitly.
- **Decision points are the hard part.** Most guides have branches: "if A, do X; if B, do Y." These are where guides earn their keep — never collapse them into linear steps.
- **A guide sits halfway between knowledge and skill.** If you find yourself wanting to *execute* the guide rather than cite it, promote it to [`knowledge/skills/`](../) instead.

## Procedure

1. **Identify the trigger.** In one sentence: what situation does this guide address? If the guide doesn't say, infer it and flag the inference.
2. **List prerequisites.** What must be true before this procedure applies? (Inputs available, decisions already made, tools at hand.)
3. **Extract the steps as steps**, numbered. One verb per step. Don't merge steps to save tokens — granularity matters for procedures.
4. **Surface decision points** as explicit branches. Use `if … then …` form. Never bury a branch inside a step.
5. **Capture the "watch out for" list.** Most guides include cautions ("don't skip step 3," "this fails when X"). Extract them.
6. **Note what the guide does not cover.** Procedures have boundaries; future readers need to know where this one stops.
7. **Decide: pack or skill?** If the procedure is something an agent should *run*, propose promoting it to `knowledge/skills/`. Note that recommendation at the bottom of the pack.

## Output shape

Use the shared skeleton from [`SKILL.md`](SKILL.md). Set `type: guide`. Replace the **Core ideas** section with these three:

```markdown
## When to use
<One sentence trigger. The situation that makes this guide the right tool.>

## Prerequisites
- <thing that must be true / available before starting>

## Procedure
1. <verb-led step>
2. <verb-led step>
   - **If** <condition>, **then** <branch>
3. <verb-led step>
...

## Watch out for
- <pitfall>
- <failure mode>
```

Keep the standard **Frameworks / models**, **Quotes worth keeping**, **How to apply**, **See also** sections.

## Hard rules

- **Never turn steps into prose.** A numbered list compresses better than a paragraph and is faster for the AI reader to follow.
- **Preserve branches.** A guide with hidden branches misleads future readers.
- **Don't invent steps** the source doesn't include. If the procedure has a gap, note the gap — don't fill it.
- **Cap at ~1.5k tokens.** Guides compress well because they're already structured. If you're over, you're paraphrasing too much.

## Common pitfalls

- Smoothing branches into linear steps "for readability." That's where the guide loses its value.
- Skipping the trigger. Without it, the pack tells you *how* but never *when*.
- Over-quoting. Guides are written to be operational, not memorable — quotes are rarely worth keeping.
- Compiling a guide that's actually a skill. Stop, propose promotion to `knowledge/skills/`, and write a `SKILL.md` instead.
