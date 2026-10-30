---
title: Design
type: design
status: draft — Nemesis to complete (seeded by Galena from the reviewed brief, 2026-10-29)
updated: 2026-10-29
---

[[Pali NLP]] › Design

# 🏗️ Design

> [!info] Draft
> Seeded from the Coven's reviewed revision brief (2026-10-29). Nemesis is writing the full design; it is reviewed by Lilith (parser attack surface) and Minerva (sources and licences) before Phase 1 starts.

## Sources (pinned by version)
- **SuttaCentral bilara-data:** Pāli root texts and Sujato's English, **matched line by line by segment ID**, so the Pāli↔English alignment is nearly free.
- **Digital Pāḷi Dictionary (DPD):** its monthly release database. It already carries about **731,000 pre-computed sandhi and compound splits** and inflection tables. Latest release: 2026-10-26.

## The database — `pali.db`
A local SQLite database, built by the code. It holds:
- segments and tokens;
- splits, and dictionary forms with their grammar;
- the concordance and frequencies;
- your known-words list.

## The engine — the `pali_nlp` package
It extends the existing package, which already has an ingester, a DPD lemmatizer, frequency, a graded reader, a vocabulary writer and SRS cards, with 19 tests.
- **New: sandhi.** DPD's splitter goes first; a small set of hand rules then filters its over-splitting. Custom rules are added only where the tests show a gap.
- Pipeline: normalize → tokenize → split → parse → gloss → concordance, grading and SRS.

## Surfaces
- **The `pali` CLI:** generates study pages and answers the queries the Sibyls call.
- **Study pages:** in a generated folder in the Tipitaka vault, made on demand.
- **Flashcards.**

## The ratchet
- Reference passages ("gold"), taken from expert analyses (DPD's own first).
- A regression suite that runs before every change.
- Blind judging wherever a model is involved.

## Keeping current
A monthly check for new DPD and bilara releases. A new release is downloaded, verified and rebuilt, then **adopted only if the ratchet holds**. Galena owns this.

## Write paths
To be stated exactly in Nemesis's draft, so that the sandbox can enforce them.
