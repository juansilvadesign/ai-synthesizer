# Compile: Book

Use when the source is a long-form text with chapters — non-fiction, practitioner book, academic monograph, manifesto.

## What makes books different

- **Many arguments, one arc.** Each chapter advances a piece, but the book is selling a single overall thesis. Both layers must end up in the pack.
- **Most books have 3–5 load-bearing chapters.** The rest illustrate, repeat, or pad. Compress hard outside the load-bearing set.
- **Frameworks have canonical names.** Books are where named models are minted ("Jobs to be Done," "Atomic Habits," "Blue Ocean"). Preserve those names verbatim — they're how the AI will be cited later.

## Procedure (two passes)

### Always read in chunks

Books almost never fit a single read. Default to chunked reading even when the file *might* fit — a partial read followed by a "I'll fill in the rest later" is how packs end up missing load-bearing chapters.

- **Chunk by structural anchor**, not by line count: one Part, one chapter cluster, or a fixed window of `~1000` lines if the structure is opaque.
- **Keep a running scratch** of per-chapter claims as you go (see Pass 1). Do not start synthesising (Pass 2) until every chunk has been read.
- **Treat manifestos and essay collections** (e.g. books without traditional chapters) the same way: chunk by Part or Section cluster, then digest each section as if it were a chapter.
- **Never compile from a partial read.** If you've only seen the first half, stop and read the rest before writing the pack.

### Pass 1 — Per-chapter digest

For each chapter, capture:

- **Chapter TL;DR** (1–3 sentences): what it argues.
- **Key claim** (one sentence): the load-bearing idea.
- **Framework or model** (if introduced): canonical name + one-line definition.
- **Worth-keeping quote** (optional): only if it cannot be paraphrased.

Keep this pass in scratch — it does **not** ship in the final pack. It's the compression substrate.

### Pass 2 — Whole-book synthesis

- **State the book's overall thesis** in 2–3 sentences.
- **Identify the load-bearing chapters.** Mark which 3–5 chapters carry the argument; everything else supports.
- **Build the chapter map** (see output shape) — short, scannable, ordered as the book orders them.
- **Pull frameworks across chapters.** A book often introduces 2–4 named models that interact. Show how.
- **Capture 3–7 quotes max.** Books earn slightly more quote budget than articles because the prose density is lower.

## Output shape

Use the shared skeleton from [`SKILL.md`](SKILL.md). Set `type: book`. Add this section between **Frameworks / models** and **Quotes worth keeping**:

```markdown
## Chapter map
1. **<Chapter title>** — <one-line digest>. _Load-bearing._
2. **<Chapter title>** — <one-line digest>.
...
```

Mark load-bearing chapters explicitly. Future readers should be able to skip the rest.

## Hard rules

- **Never compress evenly across chapters.** That signals you didn't identify the spine.
- **Preserve framework names verbatim.** "Jobs to be Done," not "the jobs framework."
- **Skip the author's origin story** unless the discovery itself encodes the framework (rare).
- **Cap at ~2k tokens.** If a book genuinely needs more, split into two packs (e.g. theory + application) and cross-link.

## Common pitfalls

- Summarising every chapter at the same depth — produces a flat pack with no spine.
- Losing the canonical framework names by paraphrasing them.
- Including the foreword or acknowledgements. Cut.
- Treating the back-cover blurb as the thesis. The author wrote one; the publisher wrote the other.
