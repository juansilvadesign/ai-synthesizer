# Compile: Article

Use when the source is a standalone piece — essay, blog post, paper, newsletter issue, op-ed.

## What makes articles different

- **One thesis, one argument chain.** Articles rise or fall on a single claim defended over a few thousand words.
- **The "real" thesis often sits 1/3 to 2/3 in.** The intro is throat-clearing; the conclusion is restatement. The load-bearing paragraph is usually buried.
- **Density is high; padding is low.** Compress aggressively — most articles fit in 500–800 tokens of pack.

## Procedure

1. **Read end-to-end first.** Don't compress while reading.
2. **State the thesis in one sentence**, in your own words. If you can't, re-read.
3. **Map the argument chain** — 3 to 7 nodes max: premise → evidence → claim → counter → resolution. Drop steps the author repeats.
4. **Extract any named framework or model.** If the article introduces "the X principle," capture it with its canonical name.
5. **Pull at most two quotes** that genuinely cannot be paraphrased without losing meaning. Cite paragraph or section.
6. **Note the limits.** What does the author *not* claim? What objections do they pre-empt?
7. **Write "How to apply"** — the situation in which a future reader should reach for this pack and the move it unlocks.

## Output shape

Use the shared skeleton from [`SKILL.md`](SKILL.md). Set `type: article`. Specific to articles:

- **TL;DR**: 3 sentences max. The thesis, the one piece of evidence that sells it, the move it implies.
- **Core ideas**: the argument chain, one bullet per node.
- **Frameworks / models**: often empty for articles — that's fine.
- **Quotes worth keeping**: 0–2 entries.

## Hard rules

- **No paragraph-by-paragraph paraphrase.** That's a transcript, not a pack.
- **Skip the anecdote unless it encodes the framework.** Most opening stories are decoration.
- **Don't preserve the article's structure** if a different ordering compresses better. The pack is for the AI reader, not a reproduction.
- **Cap at ~1k tokens.** If you can't, the source is probably a guide or short book in disguise — switch playbook.

## Common pitfalls

- Treating the headline as the thesis. The headline sells clicks; the thesis sits inside.
- Including every example. Pick the one that's load-bearing.
- Saving "How to apply" for last and writing it weakly. It's the most reusable section — write it deliberately.
