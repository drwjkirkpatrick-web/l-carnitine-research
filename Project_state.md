# Project State: L-Carnitine Thru-Hike Research

> **Last updated:** 2026-11-15
> **Current phase:** complete
> **Overall health:** green

---

## 1. Goal (1-2 sentences)
A grounded-citations LaTeX research paper (PDF) on L-carnitine supplementation as renal support during long-distance thru-hikes and sustained athletic exertion, with emphasis on desert conditions where water is limited and kidneys are under heat/dehydration/exertion stress; published to GitHub with its full evidence trail.

## 2. Current Status
### Done
- [x] Project scaffold: paper/, citations/, research/{6 theme dirs}/pages, scripts/, notes/, docs/
- [x] Pipeline scripts copied from scutellaria-research (with as_text, glob, rescue fixes already in)
- [x] Script constants adapted (PROJ, THEMES, TEX/PDF names)
- [x] Six streams COMPLETE (~223 sources, ~236 saved pages, six dossiers 2,461-2,499 words) after the 429 outage recovery
- [x] Merge: 208 unique child sources -> ledger (279 total with seed sweep); 378 quotes attached verbatim-verified
- [x] Quote rescue: 6/6 -> 150/150 claims carry verified quotes
- [x] PMID esummary spot-check: 28/28 load-bearing records match children's metadata
- [x] Paper written (parent only): lcarnitine_review.tex + body2.tex, ~8,500 words, 153 cited ids, 2 tables
- [x] sources_block.tex generated: 153 sources, 152 with evidence quotes
- [x] Compiled clean (pdflatex x2), 38 pages, 469 KB; RENDERED PDF VERIFIED (all ids listed, 64 key facts present, no markup leaked)
- [x] Zero overfull hboxes; tables placed in-section (pp. 5, 9) via [!htbp]
- [x] Citation-drift audit: 154 key-claim ids -> 0 failures
- [x] Visual check: Table 1 page passed vision; Table 2 page fell back to text-level checks after the model switch dropped vision support (same geometry as Table 1, zero overfull in log)

### Not Started
- [x] ~~Merge child findings into master ledger; mechanical verbatim-quote verification~~ (done)
- [x] ~~Parent writes paper/lcarnitine_review.tex~~ (done)
- [x] ~~Generate sources_block.tex; compile pdflatex x2; rendered-PDF verification~~ (done)
- [x] ~~Citation-drift audit; README (Phosphorus style); git; GitHub push~~ (this session)

## 3. Architecture & Key Decisions
| Decision | Rationale | Date |
|---|---|---|
| Same pipeline as tulsi + scutellaria (subagents research, parent writes prose) | proven twice; single voice; no ledger id collisions | 2026-11-15 |
| Streams: physiology / exercise / renalstress / support / tmao / practical | renal-economy + exertion-stress + carnitine-kidney evidence + honest TMAO counterpoint + dosing; `support` renamed from renalsupport after filename-collision loop | 2026-11-15 |
| TMAO counterweight gets its OWN stream | the kidney framing must survive its strongest counter-argument | 2026-11-15 |
| Children flag unverifiable hints as NOT FOUND | prevents confabulated seeds | 2026-11-15 |

## 4. Blockers & Risks
- **Risk:** direct evidence for "carnitine protects kidneys during desert hiking" may be thin → paper must assemble from renal carnitine economy + muscle-damage reduction + kidney-disease evidence, and label extrapolation honestly.
- **Risk:** TMAO literature could argue against chronic supplementation → resolve, not hide; dose and duration context matter.

## 5. Next Step (only ONE)
> **Next:** none — project complete and pushed to GitHub.

## 6. Environment & Tooling Notes
- Jetson; pdflatex (TeX Live 2022), pdftotext, gh at ~/bin/gh (authed as drwjkirkpatrick-web)
- Ledger: citations/ledger.json (sources.py global --ledger BEFORE subcommand)
- Paper: paper/lcarnitine_review.tex (+ body2.tex split) + generated sources_block.tex
- Unicode guard mandatory for quoted text (μ vs µ, ∞, ′, ·, ®, CJK precedent)

## 7. Recent Session Log
- 2026-11-15: Project created from scutellaria-research pipeline; scripts adapted; ledger reset; seed sweep (78 sources); six subagents dispatched; brief-04 theme renamed to `support` after a filename-collision generation loop.
- 2026-11-15: 429 outage killed 3 streams mid-run; exercise artifacts found complete on disk; tmao/practical completed from saved pages by two completion children. Model provider switched (Ollama Cloud → Nous z-ai) mid-project.
- 2026-11-15: Merged (279-source ledger, 150/150 verified claims); paper written (~8,500 words, 153 cited ids); compiled and verified (38 pp, zero overfull, all key facts in rendered text); drift audit 0/154; README; pushed to GitHub.

## 8. References
- Skills: research/grounded-citations; research/research-toolkit (grounded-latex-paper-workflow, research-fanout-dossiers, pubmed-botanical-research)
- Precedents: ~/projects/tulsi-research, ~/projects/scutellaria-research
