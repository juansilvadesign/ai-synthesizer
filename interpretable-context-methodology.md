## The Interpretable Context Methodology: A Practical Guide

*A synthesis for founders, consultants, and builders working seriously with AI*

---

### Why this matters

Most people work with AI the same way: open chat, paste context, get result, start over. This burns tokens, loses continuity, and locks knowledge inside whatever tool you happened to use that day.

The Interpretable Context Methodology (ICM), proposed by Van Clief and McDermott, offers a different approach: **treat your filesystem as the orchestration layer**. Instead of building multi-agent frameworks or dumping everything into a chat, you structure folders and markdown files so an AI agent reads exactly the right context at the right moment. No code, no framework, no lock-in.

The insight is borrowed from Unix: programs that do one thing, output becoming input, plain text as universal interface. Applied to AI, the folder structure *is* the agent architecture.

---

### The core principle

**Context quality beats context quantity.** Every token competes for attention. The goal isn't giving AI everything you know — it's giving it exactly what it needs, in a format it can parse fast.

Research backs this up. Liu et al. showed that LLMs perform significantly worse when relevant information is buried in long contexts. A monolithic prompt can easily hit 30–50k tokens, most of it irrelevant. A well-scoped ICM stage stays under 8k tokens of focused, relevant material.

The mechanism that makes this possible is a five-layer context hierarchy.

---

### The five-layer hierarchy

**Layer 0 — Identity (`CLAUDE.md`)**
A root-level file the agent reads first. Tells it who you are, what the workspace is, where things live. Roughly 800 tokens.

**Layer 1 — Routing (`CONTEXT.md`)**
Workspace-level: given what the user wants, which stage handles it? What shared resources exist? Roughly 300 tokens.

**Layer 2 — Stage contracts**
Each stage has its own `CONTEXT.md` defining inputs, process, and outputs. This is the control point of the whole system. 200–500 tokens per stage.

**Layer 3 — Reference material (the factory)**
Voice guides, design systems, conventions, positioning documents. Stable across runs. Configured once. 500–2k tokens.

**Layer 4 — Working artifacts (the product)**
This week's brief, this client's research output, this run's draft. Unique to each execution. Changes every time.

The factory/product distinction is the insight most people miss. Voice guides and design principles are Layer 3. This week's client brief is Layer 4. Conflating them bloats context and confuses the model about what constrains behaviour versus what to transform.

---

### A typical workspace structure

```
workspace/
  CLAUDE.md                    ← Layer 0
  CONTEXT.md                   ← Layer 1
  stages/
    01_research/
      CONTEXT.md               ← Layer 2
      references/              ← Layer 3
      output/                  ← Layer 4
    02_script/
      CONTEXT.md
      references/
      output/
    03_production/
      CONTEXT.md
      references/
      output/
  _config/                     ← Layer 3 (shared)
  skills/                      ← Layer 3 (reusable procedures)
```

The numbering encodes execution order. Folder boundaries enforce separation of concerns. Stage 01's `output/` becomes stage 02's input. If a human edits a file between stages, the next agent picks up the edited version.

---

### The five design principles

**One stage, one job.** Each stage does a single thing and writes its output to its own folder. A research stage doesn't also write scripts. A writing stage doesn't also format final output.

**Plain text as the interface.** Markdown and JSON only. No binary formats, no databases, no proprietary serialization. Any tool can participate, any human can inspect.

**Layered context loading.** Agents load only what the current stage needs. Prevention, not compression.

**Every output is an edit surface.** Intermediate outputs are files a human can open, read, edit, save before the next stage runs. The system picks up whatever the human left there.

**Configure the factory, not the product.** Set up the workspace once with your preferences, brand, style. Each run produces a new deliverable using the same configuration.

---

### How this compares to the alternatives

| Dimension | Framework approach | ICM approach |
|-----------|-------------------|--------------|
| Change stage order | Edit code, redeploy | Rename folders |
| Modify a prompt | Edit agent config | Edit a markdown file |
| Inspect intermediate state | Add logging, build dashboard | Open the folder |
| Hand off to another person | Document environment, setup | Copy the folder |
| Who can make changes | Developer | Anyone with a text editor |

The trade-off is honest: frameworks give you real-time multi-agent collaboration, concurrent execution, and programmatic branching. ICM gives you portability, inspectability, and zero developer dependency. For sequential workflows that humans review, ICM provides full capability with none of the overhead.

---

### The practical question: how does this fit alongside Claude Projects, Cowork, and Claude Code?

They're not competitors. They serve different modes:

- **Claude Projects** give you ambient context injection in a chat UI. Good for conversational iteration and exploratory work.
- **Claude Code** reads the filesystem natively. Good for production pipelines, code work, anything that outlives a conversation.
- **Orchestration tools** (Paperclip, n8n, custom scripts) point at the same folders. Stages map cleanly because ICM was designed for this.

The key problem Projects create: **context trapped inside a Project doesn't move**. It can't go to Claude Code, can't version in Git, can't be handed to a client, can't run through automation.

**The resolution: one canonical filesystem repository as source of truth. Every other surface is an interpreter.**

Demote Projects to view layers over the repository. The Project's knowledge base becomes a synced subset of the repo's Layer 3 files. The Project's instructions become a short pointer: "Stable context loaded here for conversational work; for pipeline execution, switch to Claude Code."

If your context lives in any single interpreter, you're locked in. When that tool changes, your context dies with it.

---

### How context scopes and second-brain tools fit

Notion (or any second brain) remains your ambient knowledge base — where ideas live and grow. But the parts that touch real work get compiled into the filesystem as Context Packs: short, curated markdown files written for an AI reader. Things like "Voice essentials," "Design principles," "ICP personas," "Landing page heuristics."

Notion is where knowledge lives. The filesystem is where knowledge gets compiled into a usable form for agents.

---

### On skills

A skill isn't "more context." It's a procedure the agent follows when a specific trigger fires. Think "when the task looks like X, load this checklist."

Skills pay off when:
- You have a repeatable workflow whose steps tend to get skipped
- The procedure is stable across projects
- You catch yourself re-explaining the same method

They don't pay off for one-off tasks or things better handled by clear asking in the moment. Curate them like design tokens — five to seven high-leverage skills beats thirty mediocre ones.

---

### On multiple agents

Most people over-decompose. Every agent boundary is a context handoff, and handoffs lose fidelity.

Use separate agents when:
- Tasks require genuinely different tool access or system prompts
- You need parallelisation
- One agent's context would pollute another's (a brutal critic shouldn't share context with a generative brainstormer)

Don't use separate agents when you're just organising by task type, when subtasks depend on each other, or when it merely *feels* more organised. Three to four agents with genuinely distinct roles is usually plenty.

---

### What the research suggests about how humans actually use this

Across 33 practitioners using multi-stage ICM workspaces, editing follows a U-shaped pattern:

- **Heavy editing at stage 1** (direction-setting, creative judgement)
- **Light editing in the middle** (constrained execution, trusted)
- **Heavy editing at the final stage** (alignment with earlier decisions)

The middle stages get trusted because they sit between well-defined anchors. This is the signal your factory (Layer 3) is well-configured: if you're constantly editing middle-stage output, your reference material needs work.

One caveat worth noting: ICM is a young methodology. The paper's empirical base is modest — self-reported, single model family, no controlled comparisons. The authors are transparent about this. The underlying principles (Unix pipelines, separation of concerns, context scoping) are rock-solid. The specific five-layer protocol is a reasonable convention, not gospel. Adapt it.

---

### How to start

1. **Build a root workspace for yourself first.** Your voice, your principles, your positioning, your skills. Commit it to Git.
2. **Use client/project folders that inherit from the root.** Each new engagement starts as a new folder that references shared Layer 3.
3. **Write one `CLAUDE.md` and one `CONTEXT.md` per workspace.** Keep them lean — 200–400 words for instructions. Bloat is expensive because these load every turn.
4. **Move stable context into Layer 3.** Voice, design, positioning, ICP, conventions.
5. **Keep Projects, but demote them.** Sync Layer 3 into Project knowledge for conversational work. The filesystem remains source of truth.
6. **Write a personal `how-i-work-with-ai.md`.** Stop re-explaining your preferences each session.

You'll feel the compounding within two or three projects.

---

### The meta-principle

Treat AI workflow design the way you'd treat a design system. Tokens, primitives, composition, consistency. The filesystem is the contract. Every surface is an interpreter. The factory stays stable; the products change with each run.

The simplest viable architecture for this class of problem already exists on every computer: the filesystem.

---

*Based on Van Clief & McDermott's "Interpretable Context Methodology" (arXiv:2603.16021v2) and practical adaptation for consultancy and product work.*