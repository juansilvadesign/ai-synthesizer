# Compile: Course

Use when the source is a structured learning experience — video course, workshop series, cohort program, lecture series, paid masterclass.

## What makes courses different

- **Curriculum + capability, not just ideas.** Courses teach you *how to do something*, not just what to think. The pack must capture both the concepts and the skills they build.
- **Exercises encode the real lesson.** What the instructor *asks the student to do* often reveals more than what they say. Pay attention.
- **Instructors leak rules of thumb.** The casual asides ("I always start with X," "watch out for Y") are usually the most reusable material — capture them.
- **Sequencing is intentional.** Module order is a pedagogical choice. Note when it matters.

## Procedure

1. **Map the curriculum first.** List modules / lessons in order, one line each. This is the spine.
2. **For each module, capture three things:**
   - The **key concept** introduced.
   - What the **exercise** asks the student to do (the verb matters: "draft," "critique," "rebuild").
   - Any **rule of thumb** the instructor drops in passing.
3. **Identify the meta-lesson.** Beyond the content, what's the course teaching? (E.g. a course on landing pages might really be teaching "decisions before pixels.")
4. **List capabilities unlocked.** What does the student know how to *do* after finishing? Frame as verbs: "audit a landing page," "write a positioning statement."
5. **Pull frameworks across modules.** Courses often build one master framework across 4–6 modules. Show the assembled version.
6. **Note the instructor's worked examples.** Pick the one that best demonstrates the framework end-to-end; cite where it sits in the course.

## Output shape

Use the shared skeleton from [`SKILL.md`](SKILL.md). Set `type: course`. Add two sections between **Frameworks / models** and **Quotes worth keeping**:

```markdown
## Curriculum
1. **<Module title>** — <key concept>. _Exercise:_ <verb + object>.
2. **<Module title>** — <key concept>. _Exercise:_ <verb + object>.
...

## Capabilities unlocked
- <verb-led skill the student can now perform>
- <verb-led skill the student can now perform>
```

The **How to apply** section, in courses, should answer: *which capability does this pack help the AI exercise on the user's behalf?*

## Hard rules

- **Never transcribe lectures.** Compression is the whole point.
- **Don't skip the exercises.** A pack that captures only the lectures misses half the course.
- **Preserve the instructor's named heuristics.** "Hormozi's Value Equation," not "the value formula."
- **Cap at ~2k tokens.** If a course is genuinely too rich for one pack, split by module cluster (e.g. "fundamentals" / "advanced") and cross-link.

## Common pitfalls

- Compressing only the slides. The voiceover and the exercises usually carry more.
- Listing modules without capturing what each builds toward — produces a table of contents, not a pack.
- Missing the meta-lesson. Courses with a strong worldview teach that worldview as much as the content.
- Treating Q&A or office-hours sessions as core material. They're worth scanning for rules of thumb, but rarely worth quoting.
