# L-Carnitine Thru-Hike Research

*The kidney is the body's carnitine-conservation organ — and a desert thru-hike is a renal event. This repository is where those two facts meet.*

This repository holds a **grounded-citations review paper** (LaTeX → PDF) of L-carnitine supplementation as renal support during long-distance thru-hikes and sustained exertion, with emphasis on desert conditions where water is limited and kidneys work under heat, dehydration, and eccentric-load stress — frequently compounded by trail-culture ibuprofen.

## The paper

**`paper/lcarnitine_review.pdf`** — 38 pages, ~8,500 words, 153 cited sources (152 carrying verbatim captured evidence sentences), two tables: the renal-stress evidence in exertion-heat settings, and the human carnitine trials that matter on trail.

## What it found

The answer comes in tiers, and the paper keeps them honest:

- **The stressor is quantified.** 82% of Hartford Marathon finishers met creatinine-based AKI criteria; multistage desert ultramarathons produce injury-grade AKI in 19–32% of runners per stage — with renal function *resolving between stages*, the exact daily cycle a thru-hike repeats for weeks. The desert ibuprofen RCT: AKI in 52% of ibuprofen users vs 34% of placebo (NNH 5.5). Eliminating NSAID use and dehydration could cut exertional-rhabdomyolysis AKI risk by an estimated 92.6%.
- **The carnitine economy is a renal story.** Free carnitine is freely filtered and 98–99% reabsorbed by OCTN2, a saturable, insulin-regulated transporter whose mutation causes cardiomyopathy; the human kidney performs the final biosynthetic step of the molecule it then conserves; dialysis strips 64–75% of serum free carnitine per session — the one setting where regulatory medicine formally prescribes carnitine for renal patients.
- **Direct renal-support evidence is mechanistically deep, clinically early.** Ischemic AKI reads as a carnitine-pathway failure (accumulated acylcarnitines inhibit tubular Na⁺/K⁺-ATPase); carnitine pretreatment protects rodent kidneys from ischemia-reperfusion and heat-stress AKI; contrast-nephropathy trials blunt NGAL rises; a peritoneal-dialysis RCT preserved residual renal function — but sepsis megadosing was null, Cochrane doesn't support routine dialysis supplementation, and no trial with a hard renal primary endpoint exists.
- **The muscle file is the practical lever.** 2 g/day L-carnitine L-tartrate for three weeks reduces MRI-assessed muscle damage and CK/myoglobin/soreness (2020 meta-analysis) — reducing the upstream substrate of rhabdomyolysis, the injury pathway most dangerous to a desert kidney. True muscle loading (+21% at 24 weeks with carbohydrate) is a pre-season project, not a trail maneuver.
- **The TMAO counterweight is carried, not buried.** Chronic supplementation raises fasting TMAO via the gut microbiome, and TMAO associates with CKD incidence and mortality — but Mendelian randomization reads reverse causality, the hemodialysis cohort with the highest TMAO levels on record showed *no* mortality association, and no source demonstrates renal harm from oral carnitine at supplement doses in healthy people.
- **The water question gets a boundary, not an invention.** Carnitine does not spare water; its response to dehydration is simply untested. The renal plan with actual evidence is water-with-electrolytes, retired ibuprofen, modest first weeks — with carnitine as the adjunct on top.

**The trail protocol:** LCLT powder, 2 g/day split with carbohydrate meals (~$0.13/day), below the ~3 g symptom threshold; four cautions (coumarin anticoagulants → INR check, thyroid replacement at gram doses, seizure disorders, CKD); pre-season loading if you want it; and the printed gaps (no heat-stability data for desert storage, no label-accuracy surveys) stated as gaps.

## How the evidence was built

Same paranoid pipeline as [tulsi-research](https://github.com/dwjkirkpatrick-web/tulsi-research) and [scutellaria-research](https://github.com/dwjkirkpatrick-web/scutellaria-research):

1. **Six parallel research streams** — physiology/OCTN2 economy, exercise/muscle, renal stress of desert exertion, direct renal-support evidence, the TMAO counterpoint, and practical dosing/safety — each instructed to *flag* unverifiable leads rather than round them off. Three streams died mid-run to a model-provider usage limit; all fetched pages survived on disk and were completed from salvage — the provenance is recorded in the paper's Limitations section.
2. **A retrieval ledger of 279 fetched sources** (`citations/ledger.json`), page text saved for every source.
3. **150/150 claims carry verbatim quotes**, each re-verified by the parent as an exact substring of its saved page — child self-reports were never trusted.
4. **A generated Sources block** — never hand-typed — so citations cannot drift from the ledger.
5. **Rendered-PDF verification**: all 153 cited ids resolve in the compiled output, 64 key facts present in the rendered text, zero overfull margins, no markup leakage, and a 154-id citation-drift audit passing at 100%.

## Repository layout

- `paper/` — `lcarnitine_review.tex`, `body2.tex`, generated `sources_block.tex`, and the compiled PDF
- `citations/ledger.json` — the full retrieval ledger with evidence quotes
- `research/` — six stream dossiers (`01`–`06`), findings JSONs, saved page texts per stream, merge/audit artifacts
- `scripts/` — the pipeline: `merge_and_register.py`, `quote_rescue.py`, `gen_sources_block.py`, `compile_and_verify.py`
- `notes/` — the six research briefs plus the two completion briefs, preserved as artifacts

**Author:** Walker J. Kirkpatrick, ND · November 2026
