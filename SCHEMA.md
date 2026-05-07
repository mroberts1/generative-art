# Wiki Schema: Generative Art & Design

## Domain

This wiki covers the history, theory, techniques, tools, and practitioners of generative art and design.

Scope includes:
- Early computer art and algorithmic art (1960s onward)
- Generative design systems and procedural creativity
- Tools: Processing, p5.js, TouchDesigner, openFrameworks, Max/MSP, Pure Data, etc.
- Artists, collectives, and studios
- Mathematical and artistic concepts (fractals, cellular automata, L-systems, etc.)
- AI-assisted generative art (recent developments)
- Design applications: architecture, graphic design, music, animation
- Exhibitions, institutions, and movements

## Conventions

- **File names:** lowercase, hyphens, no spaces (e.g., `vera-molnar.md`, `processing-language.md`)
- **Every wiki page** starts with YAML frontmatter (see Frontmatter section below)
- **Wikilinks:** Use `[[wikilinks]]` to connect pages. Minimum 2 outbound links per page.
- **When updating a page**, always bump the `updated` date.
- **Every new page** must be added to `index.md` under the correct section.
- **Every action** must be appended to `log.md`.
- **Provenance markers:** On pages synthesizing 3+ sources, append `^[raw/articles/source-file.md]` at the end of paragraphs whose claims come from a specific source. This lets readers trace each claim back without re-reading the raw file.

## Frontmatter

```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | timeline | movement
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
contested: false
---
```

**Fields:**
- `title`: Page title
- `created`: Date the page was created (YYYY-MM-DD)
- `updated`: Date the page was last modified (YYYY-MM-DD)
- `type`: One of entity, concept, comparison, query, timeline, movement
- `tags`: Array of tags from the taxonomy (see below)
- `sources`: Array of paths to raw files this page draws from
- `confidence`: high = well-supported across multiple sources; medium = single strong source or emerging consensus; low = opinion, speculative, or weakly supported
- `contested`: true if there are genuinely contradictory claims about this topic; false otherwise

## raw/ Frontmatter

Raw source files also get a small frontmatter block:

```yaml
---
source_url: https://example.com/article
ingested: YYYY-MM-DD
sha256: <hex digest of body only>
---
```

This lets future re-ingests detect if the source content has changed.

## Tag Taxonomy

Add new tags here BEFORE using them on pages.

**Artists & Practitioners:**
- artist
- designer
- programmer
- collective

**Techniques & Concepts:**
- algorithm
- procedural
- fractals
- cellular-automata
- l-systems
- randomness
- emergence
- recursion
- symmetry

**Tools & Languages:**
- processing
- p5js
- touchdesigner
- max-msp
- pure-data
- openframeworks
- shader
- code-based

**Domains:**
- visual-art
- graphic-design
- architecture
- music
- animation
- installation
- interactive

**Historical & Contextual:**
- early-computer-art
- movement
- exhibition
- institution
- history

**AI & Modern:**
- machine-learning
- neural-networks
- gan
- text-to-image
- diffusion

**Meta:**
- comparison
- timeline
- theory
- controversy
- prediction

## Page Thresholds

- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions or minor details
- **Split a page** when it exceeds ~200 lines — break into sub-topics with cross-links
- **Archive a page** when its content is fully superseded — move to `_archive/`, remove from index

## Entity Pages (Artists, Tools, Institutions)

One page per notable entity. Include:
- Overview / what it is
- Key facts, dates, and contributions
- Notable works (if artist)
- Relationships to other entities ([[wikilinks]])
- Tags and sources

## Concept Pages (Techniques, Theory, Algorithms)

One page per concept. Include:
- Definition / explanation
- Historical origins or first use
- Variations and developments
- Artists/tools that use it
- Related concepts ([[wikilinks]])
- Sources

## Comparison Pages

Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table format preferred)
- Verdict or synthesis
- Relevant entities/concepts ([[wikilinks]])
- Sources

## Timeline Pages

Chronological records of events, movements, or developments. Include:
- Entries in chronological order
- Key figures, works, or publications
- Links to relevant entity/concept pages
- Brief context for each entry

## Movement Pages

Characteristic entries:
- Definition and era
- Key figures and institutions
- Technological context
- Representative works
- Related movements ([[wikilinks]])

## Update Policy

When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Set `contested: true`
5. Flag for user review
