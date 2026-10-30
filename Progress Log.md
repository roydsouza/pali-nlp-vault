---
title: Progress Log
type: log
updated: 2026-10-29
---

[[Pali NLP]] › Progress Log

# 📓 Progress Log

*Newest first.*

### 2026-10-29
- **Study pages work (v0).** Roy asked Nemesis to "study MN 118" and got a chat report, not a page. Galena built `pali-study` the same evening, and pages for MN 10, MN 118 and SN 56.11 are in `Tipitaka/study/`. Fixes along the way: words starting with a capital diacritic (*Ānāpānassati*) were losing their first letter; *ahaṃ* resolved to "day" until the rule became "most frequent in the early texts"; SN suttas inside collection files are now found.
- DPD 2026-10-26 installed for the pipeline: 89,763 headwords and 852,425 split forms (Simsapa's June copy had about 78,800 and 731,000). A monthly updater is in place.
- Roy ratified the clearance: Nemesis is caretaker of this vault and has full read/write access to Tipitaka. It ships in release Step B, with the Diet vault's changes.
- Serenity delivered the dashboard banner and the Directory card.
- Nemesis wrote the Pali NLP proposal at Roy's request.
- **Reviewed:**
  - Galena, Lilith, Minerva and Serenity read it.
  - Lilith found that the first stage already exists in `pali-nlp` (508 suttas with vocabulary tables, a 518-sutta graded reader).
  - Galena confirmed that DPD already carries sandhi splits (*tathāgatopi* → *tathāgato + api*).
- **Roy approved it with revisions.** See [[Decisions]].
- Revision brief sent to Nemesis: Armageddon vault, `Coven/Nemesis/home-proposals/pali-nlp/REVISION BRIEF.md`.
- This vault created.
