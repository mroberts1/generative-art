## [2026-05-07] migrate-cleanup | Reprocessed vault to v2 conventions

- **CLAUDE.md** is now the authoritative governance document (v2 MANIFEST inline). Previous split between MANIFEST.md (governance) and CLAUDE.md (bridge) consolidated into single file.
- **Sources consolidated:** `sources/Galanter_Generative_Art_Theory.md` (summary) + `sources/galanter_generative_text.md` (raw extracted text) → single `sources/Galanter - Generative Art Theory (2016).md` with v2 frontmatter (Tier: #source/peer-reviewed, Last verified:, Superseded by:), proper Summary / Key points / Claude's notes sections above the preserved extracted body.
- **Wiki page renamed:** `wiki/Philip_Galanter.md` → `wiki/philip-galanter.md` (kebab-case per vault convention). Wikilink `[[Galanter Generative Art Theory]]` updated to `[[Galanter - Generative Art Theory (2016)]]`.
- **Binary preserved:** PDF moved from `raw/papers/galanter_generative.pdf` to `sources/galanter-generative-2016.pdf` alongside the source note.
- **Removed:** `raw/` directory (not part of v2 structure). Duplicate source files removed.
- **Added:** empty `inbox/` and `wiki/_archive/` directories per v2.
- **index.md rewritten:** proper v2 sections (Concepts / Persons / Sources / Research Threads / Open Questions / Prompts / Candidates / Keywords) with all concept candidates listed as awaiting corroboration. Every concept is currently single-source (Galanter-only) so none are promoted yet.

# Wiki Log

> Chronological record of all wiki actions. Append-only.

## [2026-05-07] init | Vault restructured with MANIFEST.md
- Migrated from old SCHEMA.md structure to new MANIFEST.md structure
- Created inbox/, sources/, wiki/_meta/ directories
- Initialized index.md, log.md, and MANIFEST.md

## [2026-05-07] ingest | Galanter - Generative Art Theory (2016)
- **Raw source**: sources/Galanter_Generative_Art_Theory.md
- **Pages created**: 1
  - wiki/Philip_Galanter.md (people page, author tier)
- **Candidates**: 3 themes awaiting 2nd source
  - Generative Art Definition
  - Autonomy in Generative Systems
  - Complexity Science Framework
- **Index updated**: 1 source added, 3 keywords added, 1 person page created
- **Keywords added**: generative-art, theory, definition
