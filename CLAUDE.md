# Instructions for Claude (and other agents)

You are operating inside the **generative-art Foundry**, an autonomous knowledge vault about generative art, systems-based creative practice, and computational aesthetics.

## Read these first, in this order

1. **`MANIFEST.md`** (root) — authoritative governance doc. This is v2 of the Foundry pattern. It defines directory structure, frontmatter, source tiers, conflict handling, freshness, pruning, sibling vaults, and the eval loop. **Everything you do in this vault must follow MANIFEST.md.**
2. **`wiki/_meta/index.md`** — current catalog of pages, keywords, open questions, candidates. Read this before answering any query or deciding whether a new page is needed.
3. **`wiki/_meta/log.md`** — chronological record of operations. Read the last 20-30 entries to understand recent vault state.
4. **`wiki/_meta/eval.md`** — 10 stable evaluation questions. Don't answer them unless explicitly running `/foundry-eval`.
5. **`wiki/_meta/eval-usage.md`** — explains the eval loop and how questions are used. Read this if the user asks about eval or evaluation.

## Operations

The MANIFEST defines six operations. Match the user's request to the right one:

- `/foundry-ingest` — process `inbox/` into `sources/`
- `/foundry-compile` — promote sources into `wiki/` concepts (2-source rule)
- `/foundry-ask` — research a question, write report to `wiki/YYYY-MM-DD-slug.md`
- `/foundry-lint` — health check, overwrite `wiki/_meta/health.md`
- `/foundry-prune` — archive stale candidates/orphans (confirmation-gated)
- `/foundry-eval` — run eval questions, rate coverage, feed findings back to index

## Hard rules (from MANIFEST, surfaced for emphasis)

- **Never delete.** Archive into `wiki/_archive/YYYY-MM/` with a stub at the original path.
- **Never silently resolve contradictions.** Set `Contested: true` and add a `Disagreements` section.
- **Never ingest a source without a `Tier:`.** Pick one of: `#source/peer-reviewed`, `#source/primary`, `#source/journalism`, `#source/secondary`, `#source/informal`.
- **Never spin out a concept from a single source.** Log to Candidates in index.md and wait for corroboration.
- **Never break a wikilink.** Renaming or archiving requires updating every backlink or leaving a forwarding stub.
- **Never write outside `sources/`, `wiki/`, `wiki/_archive/`, or `inbox/`.**

## Voice

Concepts read like field notes from a practitioner, not gallery wall text, not academic survey, not marketing copy. Favour sharp claims, tight evidence, and honest open questions. (See MANIFEST.md "## Voice anchor" — if the user has customised that paragraph, that's authoritative over this summary.)

## If you're unsure

Ask the user before doing anything destructive or structural. The MANIFEST is the source of truth; this file is a pointer to it.
