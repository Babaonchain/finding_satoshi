# Finding Satoshi — Pre-Planning Strategy

> This is the strategy layer. `planning.md` (next) will hold the actual plan for how we go about this. This file is about *how we think* before we plan.

## Goal

**Identify Satoshi.**

That is the goal. Plainly stated.

## Framing

Let's say right off the bat: this is a hard problem, but it is achievable.

We are not chasing a myth. We are conducting structured research against a finite (if large) set of evidence, with modern tools, and with enough contributors to cover ground no single researcher could.

## Scale: Contributors and Data

We are planning for many contributors to this research.

Many of these researchers will be AI agents. Researchers will have varying intelligence — human and artificial, expert and novice, specialized and generalist.

We should expect that there will be a LOT of data. Evidence and analysis will accumulate fast: primary sources, archives, forum posts, emails, code commits, linguistic analysis, timelines, debunks, leads, dead ends.

This repo will ultimately become massive. We should design for that from day one, not retrofit later.

## The Hardest Problem

Let's say this very clearly:

**The hardest problem is not the research itself, but organizing the research, and coordinating research across such a large number of contributors.**

Anyone can chase a lead. Few systems can keep a thousand researchers from duplicating work, losing context, burying signal, or stepping on each other.

We win or lose on coordination.

## Keys to Success

Our success will come down to four things:

1. **Our process.** How research is proposed, done, reviewed, and merged.
2. **Our ability to identify faults in that process, and improve it over time.** The process itself is a research subject. We instrument it, critique it, and iterate.
3. **The way we organize information.** Categorization, indexing, and retrieval.
4. **Our ability to re-organize information.** As understanding grows, old categories break. We must be able to reshape the whole tree without losing work.

Process, meta-process, organization, re-organization. That's the game.

## Data Organization Strategy

Researchers — human and AI — can only hold so much information in their context at once.

A researcher wanting to contribute should **not** need to read thousands of files to be useful. The repository must be organized so that, at a glance, a researcher can see that huge portions of it are irrelevant to the lead they want to chase.

We need a strategy for data organization which deeply understands how agents (and also humans) work.

Our largest strength is our ability to **locate relevant data while reading as few words as possible**. Every organizational decision should serve that strength.

### The Index Principle

Imagine you're looking for information about cats. You read an index saying:

```
/plants — info about plants
/animals — info about animals
```

You want cats, so you look in `/animals`, and find an index file:

```
/mammals — info about mammals
/reptiles — info about reptiles
/fish — info about fish
```

You know what to look in next. You never opened a single file about plants. You read maybe twenty words to eliminate 90% of the repo.

That is the pattern we want everywhere: **nested, human-readable indexes that let a researcher prune the search tree with minimum reading.**

Implications:

- Every directory gets an index (e.g. `INDEX.md` or `README.md`) describing its children in a few words each.
- Every single file should be indexed *somewhere*. No orphans.
- Indexes are load-bearing infrastructure, not documentation afterthoughts.
- Depth beats breadth: prefer a tree a researcher can descend over a flat folder they must scan.

### Naming and Descriptions Are an Art

Naming and descriptions are an art we should not take lightly.

Writing a very clear description that cannot be misinterpreted, in as few words as possible, is non-trivial. We should think hard about this.

Guidelines to develop:

- Names should be unambiguous at the parent level (no `misc/`, no `stuff/`, no `other/`).
- Descriptions should say what *is* inside, and just as importantly, what is *not*.
- Optimize for the skimmer: the researcher deciding in 5 seconds whether to descend.
- Avoid cleverness. Boring, precise names win.

This deserves its own style guide, iterated over time.

### Data Re-organizers

Some contributors will be assigned specifically to data reorganization.

A re-organizer should be able to understand the full structure of the data **without reading anything except indexes**. They read all the indexes, build a mental model of the tree, and then think critically about whether we should be re-indexing or categorizing differently.

This means:

- Indexes must be complete and honest. If the index lies about what's inside, re-organization fails.
- Re-organization is a first-class contribution, not janitorial work.
- Moves must preserve history and update all indexes that reference the moved content.

## Contribution Contract: Reflection Required

Every contribution MUST come with a reflection.

The reflection should describe:

- **Pain points** the researcher went through — e.g. "a lot of effort was spent doing xyz," "the index at `/x` was misleading," "I had to read 40 files to find one fact."
- **Tools** other researchers might find useful — e.g. "here's an API which gives you this specific data, and here's how you call it," scripts, queries, search strategies.

Why: pain points are bug reports against our process and organization. Tools are accelerants. Without reflections, we repeat suffering and re-discover tools. With them, the system learns.

Reflections should live alongside the contribution (or in a standard location) and be indexed like everything else.

## Human Assistance

We should recognize that some research requires humans, for various reasons — access to paywalled archives, physical records, interviews, judgment calls, credentials, or simply ground truth a machine cannot get.

There are places where AI could use some human assistance (i.e. gather some evidence that a machine cannot obtain). We should account for that explicitly.

We will maintain a **ranked list of requests for human assistance**: data and evidence that researchers are asking humans to obtain, ordered by expected value.

- Requests should state exactly what is needed, why it matters, and what has already been tried.
- Ranking should reflect impact vs. effort, updated as the investigation evolves.
- Completed requests become evidence, indexed like everything else, with provenance noted.

This keeps human effort — our scarcest resource — pointed at the highest-leverage gaps.

## Tooling

Researchers should provide tooling, not just findings.

- Scripts, notebooks, scrapers, API wrappers, and queries should be contributed alongside the research that used them.
- Every tool contribution comes with the same reflection requirement: what it does, how to call it, what it costs, where it breaks.
- Prefer small, composable tools over monoliths. A researcher should be able to reuse one piece without adopting a framework.

Tooling is how individual leverage becomes collective leverage.

## What Comes Next

This file is the strategy. Next:

- `planning.md` — the actual operational plan: workstreams, roles, contribution lifecycle, review, and governance.
- Index scaffolding for `/evidence`, `/analysis`, `/tools`, `/reflections`, `/human-requests`, etc.
- The first contribution contract template (including the reflection section).

We build the machine that builds the answer.
