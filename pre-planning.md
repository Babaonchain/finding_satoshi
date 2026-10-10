# Finding Satoshi — Pre-Planning Strategy

> This is the strategy layer. `planning.md` will hold the operational plan. This file is about *how we think* before we plan.
>
> It is organized in two layers. **Layer 1 names the terrain** — the very high-level realities we are dealing with: a very large number of files, a very large number of researchers. **Layer 2 describes the management** — how we handle that terrain.

---

## Layer 1: The Terrain

The high-level realities. Everything in Layer 2 exists to answer these.

### 1. The goal

**Identify Satoshi.**

One sentence. Every organizational decision should be traceable back to it.

### 2. A very large number of files

We should expect a LOT of data: evidence and analysis accumulating fast — primary sources, archives, forum posts, emails, code commits, linguistic analysis, timelines, debunks, leads, dead ends.

This repo will ultimately become massive. We design for that from day one; we do not retrofit later.

### 3. A very large number of researchers

We are planning for many contributors. Many of these researchers will be AI agents. Researchers — human and artificial — will have varying intelligence: expert and novice, specialized and generalist.

The system must work for the weakest contributor, not just the strongest. If only brilliant researchers can navigate the repo, we have failed. Design for the floor, not the ceiling.

### 4. Finite context per researcher

Every researcher, human or AI, can only hold so much information in context at once.

A researcher wanting to contribute should **not** need to read thousands of files to be useful. At a glance, they should be able to see that huge portions of the repo are irrelevant to the lead they want to chase.

### 5. The thesis

Let's say this very clearly:

**The hardest problem is not the research itself, but organizing the research, and coordinating research across such a large number of contributors.**

Anyone can chase a lead. Few systems keep hundreds of contributors from duplicating work, losing context, burying signal, or stepping on each other. We win or lose on coordination.

And let's say right off the bat: this is a hard problem, but it is achievable. Finite evidence, modern tools, and enough contributors to cover ground no single researcher could.

---

## Layer 2: The Management

How we handle the terrain above. Each piece answers a specific reality from Layer 1.

### Keys to success

Four things, in order:

1. **Our process.** How research is proposed, done, reviewed, and merged. *(Answers: many researchers.)*
2. **Our ability to identify faults in that process, and improve it over time.** The process is itself a research subject — instrumented, critiqued, iterated. *(Answers: varying intelligence; the system must learn faster than its weakest link.)*
3. **The way we organize information.** Categorization, indexing, retrieval. *(Answers: many files, finite context.)*
4. **Our ability to re-organize information.** Understanding grows; old categories break. We reshape the tree without losing work. *(Answers: growth over time.)*

Process, meta-process, organization, re-organization. That's the game.

### Data organization: read as few words as possible

We need a strategy for data organization which deeply understands how agents (and humans) work. Our largest strength is our ability to **locate relevant data while reading as few words as possible**. Every organizational decision serves that strength. This is the direct answer to *many files* meets *finite context*.

#### The index principle

Imagine you're looking for information about cats. You read an index:

```
/plants — info about plants
/animals — info about animals
```

You want cats, so you open `/animals` and find:

```
/mammals — info about mammals
/reptiles — info about reptiles
/fish — info about fish
```

You know where to look next. You never opened a file about plants. You read ~20 words to eliminate 90% of the repo.

That is the pattern everywhere: **nested, human-readable indexes that let a researcher prune the search tree with minimum reading.**

- Every directory gets an index describing its children in a few words each.
- Every single file is indexed somewhere. No orphans.
- Indexes are load-bearing infrastructure, not documentation afterthoughts.
- Prefer depth over breadth: a tree a researcher can descend beats a flat folder they must scan.

#### Naming and descriptions are an art

Naming and descriptions are an art we should not take lightly. Writing a very clear description that cannot be misinterpreted, in as few words as possible, is non-trivial. We should think hard about this.

- Names unambiguous at the parent level. No `misc/`, no `stuff/`, no `other/`.
- Descriptions say what *is* inside — and what is *not*.
- Optimize for the skimmer deciding in five seconds whether to descend.
- Boring, precise names beat clever ones.

This deserves its own style guide, iterated over time. It matters doubly because contributors vary in intelligence: the index must be legible to the weakest reader.

#### Data re-organizers

Some contributors are assigned specifically to reorganization. A re-organizer understands the full structure of the data **reading nothing but indexes** — then thinks critically about whether we should re-index or categorize differently.

- Indexes must be complete and honest, or re-organization fails.
- Re-organization is first-class work, not janitorial.
- Moves preserve history and update every index that referenced the moved content.

This is key #4 (re-organize) made into a role.

### Contribution contract: every contribution carries a reflection

Every contribution MUST come with a reflection:

- **Pain points** — "a lot of effort was spent doing xyz," "the index at `/x` was misleading," "I read 40 files to find one fact." These are bug reports against our process and organization — the fuel for key #2 (find faults, improve the process).
- **Tools** — "here's an API that gives you this data, and here's how you call it." Scripts, queries, search strategies. Individual leverage becomes collective leverage.

Without reflections we repeat suffering and re-discover tools. With them, the system learns.

### Human assistance: a ranked queue

Some research requires humans — paywalled archives, physical records, interviews, credentials, judgment calls, ground truth a machine cannot reach. There are places where AI needs a human to gather evidence it cannot get.

We maintain a **ranked list of requests for human assistance**: evidence researchers are asking humans to obtain, ordered by expected value (impact vs. effort), updated as the investigation evolves.

- Each request states exactly what's needed, why it matters, and what's already been tried.
- Completed requests become evidence, indexed like everything else, provenance noted.

Human effort is our scarcest resource. Point it at the highest-leverage gaps.

### Tooling

Researchers provide tooling, not just findings. Small, composable tools over monoliths — a researcher reuses one piece without adopting a framework. Every tool ships with the same reflection: what it does, how to call it, what it costs, where it breaks.

---

## What comes next

- `planning.md` — the operational plan: workstreams, roles, contribution lifecycle, review, governance.
- Index scaffolding: `/evidence`, `/analysis`, `/tools`, `/reflections`, `/human-requests`.
- The first contribution template, reflection section included.

We build the machine that builds the answer.
