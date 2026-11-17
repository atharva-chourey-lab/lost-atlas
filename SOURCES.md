# Sources Map — Paper 1

Author: Atharva Chourey
Affiliation: Atharva Chourey Lab (independent research lab)

Manuscript in preparation — not yet peer-reviewed.

Paper: "Shrinkage-corrected histological compilation values average ~1.6× MRI-atlas values: an audit of a comparative neuroanatomy archive" (`paper.md` in this folder).

Rule applied: every quantitative claim in the paper traces to a number in the source files listed below. Values are reproduced as used in the paper. Where a number appears in the sources in more than one variant (different fit versions), the variant used is identified and the others are noted. No number was invented, estimated, or rounded into existence; rounding follows the sources' own rounding (e.g. 2.022 cm³ → 2.02 cm³, 4.496 cm³ → 4.50 cm³, as in REPORT.md).

All source paths are relative to `~/workspace/brain-scan-comparison/` unless stated otherwise. Precedent-sweep verdicts are from `~/workspace/papers/precedent-sweep/SWEEP.md`, section P1.

## Key numbers — trace table

| # | Quantity as used in paper | Value | Exact source file (section) |
|---|---|---|---|
| 1 | Label files checked (census) | 71 total | `aquatic/REPORT_aquatic.md` (§2, QC verdicts: "18 of 71 catalogue label files"); `logs/processing_log.md` (2026-11-16 night, Goldmine Hunter follow-on: "53 real label files, 18 empty placeholders, of 71 label files checked") |
| 2 | Label files with real data | 53 | `logs/processing_log.md` (2026-11-16 night: "Deep-check census: 53 real label files, 18 empty placeholders"); `aquatic/REPORT_aquatic.md` (§1: "census sealed: 53 real / 18 empty-placeholder label files") |
| 3 | Empty placeholder label files | 18 | Same as #2 |
| 4 | Species in catalogue census | 37 species | `REPORT.md` (2026-11-16 Addendum: "Audit of the full 37-species label set"); `BENCHMARK.md` (Test set: "not among the Brain Catalogue's 37 specimens"); `PREDICTION.md` §3 |
| 5 | Lion brain volume (specimen mask) | 188.1 cm³ (band 178–194) | `REPORT.md` §2 (delta table) and §1/§8 provenance; sensitivity in `logs/processing_log.md` (2026-11-16) |
| 6 | Lion hippocampus, MRI label | 2.02 cm³ (2.022 cm³ registered); 1.07% of brain | `REPORT.md` (2026-11-16 Addendum: "hippocampus 2.02 cm³ (1.07% of the 188.1 cm³ brain)"); `PREDICTION.md` §4 (2.022 cm³); `outputs/cross_species_volumes_v2.csv` / `v3.csv` (Lion row) |
| 7 | Lion telencephalon, MRI label | 145.60 cm³ (77.4%) | `REPORT.md` (2026-11-16 Addendum) |
| 8 | Lion hippocampus, histology (prior) | 4.50 cm³ (4,496.16 mm³; 4.496 cm³; specimen 62-79) | `REPORT.md` (2026-11-17 Addendum §(a): Reep et al. 2007, 4,496.16 mm³ ≈ 4.50 cm³, specimen 62-79); `PREDICTION.md` §4 (4.496 cm³) |
| 9 | Leopard hippocampus, MRI label | 1.18 cm³ (1.178 cm³) | `PREDICTION.md` §4; `REPORT.md` (2026-11-17 Addendum §(b)) |
| 10 | Leopard hippocampus, histology | 3.12 cm³ (3.121 cm³) | `PREDICTION.md` §4; `REPORT.md` (2026-11-17 Addendum §(a)–(b)) |
| 11 | Felid gap ratio (lion) | ~2.2× | `REPORT.md` (2026-11-17 Addendum §(b): "The ~2.2× gap"); computed from #6/#8 as in sources |
| 12 | Felid Test B, +1 voxel gap closure | Lion 15.5%; leopard 19.2% (<20% band) | `REPORT.md` (2026-11-17 Addendum §(b)); `logs/processing_log.md` (2026-11-17, Felid reconciliation) |
| 13 | Felid Test B, +2 voxel gap closure | Lion 34.4%; leopard 38.4% | Same as #12 |
| 14 | Felid Test A | VOID; Dice 0.000 (lion) / 0.001 (leopard); centroid offsets 33.2 / 15.9 mm | `REPORT.md` (2026-11-17 Addendum §(b)); `logs/processing_log.md` (2026-11-17, Felid reconciliation) |
| 15 | Reep shrinkage-correction multiplier | ≈2.4 mean factor (rest of taxa); species-specific for six taxa | `BENCHMARK.md` (Primary subset — Reep 2007); `REPORT.md` §(b) ("≈2.4, resting on estimated shrinkage of 51.8–65%") |
| 16 | Reep shrinkage factors (sweep-verified) | Mean volumetric shrinkage 59.0%; correction factors 2.1–2.9 | `~/workspace/papers/precedent-sweep/SWEEP.md` (P1c, citing Reep et al. 2007 Table 2). NOTE: distinct from #15's project-record figures (51.8–65% estimated shrinkage); both are reported in the paper, labelled by source |
| 17 | Registered line | log₁₀(Vh) = −1.6609 + 0.8467 × log₁₀(Vb); n = 8, r = 0.930, p = 8.1×10⁻⁴; fit range ≈6–443 cm³ | `PREDICTION.md` §1; `BENCHMARK.md` (The registered line and criterion) |
| 18 | Registered fit set | Black rhinoceros, cat, cheetah, ferret, giant panda, leopard, lion, red kangaroo (n = 8) | `PREDICTION.md` §1 |
| 19 | Fit exclusions | Sloth bear (artifact, same-side components); giraffe (unilateral, second component 1.3% of first) | `PREDICTION.md` §1 |
| 20 | Descriptive n = 10 fit | Slope 0.81, r = 0.90 | `REPORT.md` (2026-11-16 Addendum); `logs/processing_log.md` (2026-11-16 late, Table v3 entry gives headline n = 10 slope 0.809, r 0.897) |
| 21 | Newborn point check | Predicted 3.30 cm³; measured 2.90 ± 0.31 cm³ (n = 10); −12.0% | `PREDICTION.md` §2; `REPORT.md` (2026-11-17 Addendum, State of registered items) |
| 22 | Newborn brain volume | 374.4 ± 37.0 cm³ tissue | `REPORT.md` §2 |
| 23 | Blind benchmark test set | 343 species (Reep n = 26 + Patzke compilation n = 317) | `BENCHMARK.md` (Verdict; Test set); `REPORT.md` §(c) |
| 24 | Benchmark, full set — line | Median APE 66.0%; mean signed −53.5%; within ±25% 2.0%, within ±50% 18.7% | `BENCHMARK.md` (Verdict; Scorecard) |
| 25 | Benchmark, full set — Patzke model | Median APE 18.2%; mean signed +17.5%; within ±25% 61.2%, within ±50% 82.5% | `BENCHMARK.md` (Scorecard; Reading the failure) |
| 26 | Benchmark head-to-head | 56–287 (line–Patzke) | `BENCHMARK.md` (Scorecard) |
| 27 | Benchmark, Reep-only subset | Line 55.5% vs Patzke 29.2% median APE | `BENCHMARK.md` (Scorecard) |
| 28 | Benchmark, both-blind subset | n = 6; line 301.6% vs Patzke 184.0% median APE | `BENCHMARK.md` (Scorecard, footnote *) |
| 29 | Patzke in-sample declaration | Fitted on 337 of 343 test species | `BENCHMARK.md` (Comparators — Patzke: In-sample warning); `REPORT.md` §(c) |
| 30 | Patzke model equation | ln(Vh) = 9.26 × (0.72 − exp(−0.097 × ln(Vb))); a = 9.26, b = 0.72, c = 0.097, r² = 0.97 | `BENCHMARK.md` (Comparators — Patzke) |
| 31 | Karbowski comparator | NOT gradeable; −0.14 exponent is volume-specific glucose metabolic rate; no volume equation published | `BENCHMARK.md` (Comparators — Karbowski); `REPORT.md` §(c) |
| 32 | Compilation-to-compilation ratio ("Two Rulers") | ~1.6× (paired material); felid instance ~2.2× | `REPORT.md` §(c) ("histological hippocampus volumes run ~1.6× the MRI-segmentation values"); `BENCHMARK.md` (Reading the failure §1: "by a factor of roughly 1.6 here, and ~2.2 in the felid case"). RESCOPED per sweep P1c — see Novelty section below; paper uses only the compilation-to-compilation wording |
| 33 | Benchmark size bands (line median APE) | 65.7% (<2 cm³); 69.0% (2–20 cm³); 51.3% (>20 cm³); fit-range (5–450 cm³, n = 65) 62.6% | `BENCHMARK.md` (Reading the failure §2) |
| 34 | Small-brain species count | 247 of 343 with brains <2 cm³ | `BENCHMARK.md` (Compilation subset; Reading §2) |
| 35 | Patzke Table 1 dropped-digit rows | 3 species excluded: *Micropotamogale lamottei*, *Hipposideros sperois*, *Notopteris macdonaldi* (identity Vb = Mb/1.036) | `BENCHMARK.md` (Validation of the transcription); `REPORT.md` §(c) |
| 36 | Verified hippocampus set (n = 10, pre-QC) | Ferret 0.17, cat 0.54, cheetah 0.85, red kangaroo 0.20, giant panda 1.07, leopard 1.18, lion 2.02, sloth bear 4.00, giraffe 2.92, black rhinoceros 6.85 cm³ | `REPORT.md` (2026-11-16 Addendum: Verified cross-species hippocampus set); `outputs/cross_species_volumes_v2.csv` |
| 37 | Ferret neocortex (recovered label) | 1.87 cm³ (1.867 cm³) | `logs/processing_log.md` (2026-11-16 late, Neocortex check: "Ferret (nz=1,080,694 -> 1.87 cm3)"); `outputs/cross_species_volumes_v2.csv`/`v3.csv`; `aquatic/REPORT_aquatic.md` §1 |
| 38 | White-headed capuchin neocortex | 27.33 cm³ (27.332 cm³) | Same as #37 ("White-headed_capuchin (nz=1,215,954 -> 27.33 cm3)") |
| 39 | Chimpanzee propagation cross-check | D99 1.48 cm³; CIVM 1.56 cm³ (+5.4%); stereology comparator 1.77 cm³ (−12%); CIVM label 79 = 0.641 cm³ in rhesus template | `REPORT.md` §(d); `logs/processing_log.md` (2026-11-17, CIVM chimp cross-check) |
| 40 | Rhino catalogue label / brain / line prediction | Label 6.854 cm³; brain 442.65 cm³; predicted 3.80 cm³; registered residual +80.5% | `PREDICTION.md` §5; `PREREGISTRATION_rhino_anomaly_2026-11-17.md` (State of the record) |
| 41 | Rhino confirmatory re-delineation | 6.97 cm³ (sides 2.41 / 4.57); ±1 voxel −28.2%/+21.9%, erode-1 5.01 cm³; verdict REFUTED (band ≥5.48; confirmed ceiling 4.83); fixed prediction ≈4.2 cm³ | `REPORT.md` §(h); `outputs/rhino_confirmatory_redelineation.md`; `PREREGISTRATION_followups_2026-11-17.md` Item 2 |
| 42 | Rhino literature pair (same-brain inference) | Patzke compilation 7.48 cm³ vs Bhagwandin MRI 4.71 cm³; ratio 1.59×; shared brain mass 531 g | `REPORT.md` §(e); `outputs/rhino_anomaly_investigation.md` Direction 1 |
| 43 | Rhino vs Patzke model | Label +47.0%; tracing +49.5%; Patzke own value +49.3%; Bhagwandin −6.0% | `REPORT.md` §(k5); `outputs/rhino_anomaly_investigation.md` Direction 5 |
| 44 | Rhino identity / second specimen | Identity CONFIRMED, Zenodo record 44797 (mesh 44795), md5-identical; catalogue specimen ≠ Patzke/Bhagwandin animal (mass-equivalent 458.6 g vs 531 g); second specimen NONE OPENLY AVAILABLE | `REPORT.md` §(k1),(k3); `outputs/rhino_anomaly_investigation.md` Directions 1, 3 |
| 45 | Rhino Bhagwandin simulation | 2 mm slabs phase-median 7.21 cm³; Cavalieri 6 mm 6.92 cm³; ≥75%-fill 6.07 cm³; verdict FAILS | `REPORT.md` §(k4); `outputs/rhino_anomaly_investigation.md` Direction 4 |
| 46 | Ferret residual | +70.7% registered (0.173 vs 0.101 cm³ at brain 6.13 cm³); Otsu band 5.97–6.27 cm³, residual +67.7% to +74.8%; verdict FORM FAILURE (post-hoc) | `PREDICTION.md` §5; `REPORT.md` §(i); `outputs/ferret_forensics.md` |
| 47 | Dolphin delineation attempt | Traced object 3.44 cm³; FAILED gates (a) and (d); sanity band 0.3–2.0 cm³; NO volume claimed | `REPORT.md` §(g); `outputs/dolphin_delineation.md`; `PREREGISTRATION_followups_2026-11-17.md` Item 1 |
| 48 | Aquatic census | 5 aquatic/semi-aquatic of 37 species; bottlenose brain 515.46 cm³; telencephalon labels La Plata 91.29, crocodile 12.21, nursehound 20.24 cm³; zero usable hippocampus labels | `aquatic/REPORT_aquatic.md` §§1–2 |
| 49 | Cetacean literature residuals vs line | −81.3% to −92.0% (four cetaceans); manatee +20.2%; hippo +47.1% / +5.6% | `aquatic/REPORT_aquatic.md` §3b |
| 50 | Literature audit count | 14 verified items (3 direct, 6 shrinkage, 2 authority, 3 delineation) | `outputs/two_rulers_literature_audit.md` §1 |
| 51 | Navarrete et al. 2018 hippocampus discrepancy | +31.5% (range 13.1–59.6); ratio ≈1.3–1.46× depending on convention; 17 species with both, 39 MRI species | `outputs/two_rulers_literature_audit.md` §1A item 1 |
| 52 | Delgado-González et al. 2015 | Histology > MRI in all 4 cells; pooled ratio ≈1.37× (audit computation from Tables 3–4); n = 12 human brains | `outputs/two_rulers_literature_audit.md` §1A item 2 |
| 53 | Wagstyl / BigBrain shrinkage factor | 1.931 (volume-based); per-axis 1.15 / 1.22 / 1.43 | `outputs/two_rulers_literature_audit.md` §1B item 8, §2; sweep P1c (same value) |
| 54 | Nadkarni et al. 2019 (sweep-mandated) | Hippocampus histology overestimate ~38% vs in vivo MRI; pallidum underestimate ~38% (reversal) | `~/workspace/papers/precedent-sweep/SWEEP.md` (P1c, citing Nadkarni et al. 2019, *NeuroImage* 185:85–95). NOT in the brain-scan-comparison sources; introduced by the binding sweep verdict and cited as such in the paper (§1.1, §4.4) |
| 55 | Raw histology direction (sweep-mandated) | Raw (uncorrected) histological volumes run BELOW fresh/MRI volumes | `~/workspace/papers/precedent-sweep/SWEEP.md` (P1c: "Raw (uncorrected) histological volumes run BELOW fresh/MRI volumes"); consistent with shrinkage factors in #16/#53 |

## Numbers from the brief — verification outcome

- 71 / 53 / 18 label census — **found** (#1–#3).
- Lion MRI 2.02 cm³ vs Reep histology 4.50 cm³ — **found** (#6, #8).
- "Two Rulers" ~1.6× across 343 species — **found as recorded** (#23, #32), but **rescoped** by the binding precedent sweep (P1c): the paper presents it only as a compilation-to-compilation ratio for paired species/regions, never as a systematic property of histology. Title, abstract and discussion were revised accordingly.
- Blind benchmark median APE 66.0% vs 18.2% — **found exactly as recorded** (#24, #25), with the in-sample caveat (#29) carried wherever the headline is used.
- Ferret neocortex 1.87 cm³; capuchin neocortex 27.33 cm³ — **found** (#37, #38).
- Rhino residual anomaly — **found, with status updated**: the early definition-mismatch explanation was superseded/refuted by its own registered confirmatory test (#41); the paper reports the anomaly as **reopened and unexplained**, the record's one open anomaly (#40–#45). Any draft wording presenting the definition explanation as standing would be wrong and was not used.

No brief number was missing from the sources.

## Gaps flagged in the paper (§4.5, item 11)

Explicitly recorded as not measured / not reported in the underlying project records, and nowhere estimated in the paper:

- Lion amygdala, hypothalamus and periaqueductal grey volumes — no published value in the record; not segmentable with validated tools on the single ex vivo scan (`REPORT.md` §§2, 6).
- Lion diffusion MRI and any lion functional data — none exists openly; specimen is post-mortem (`REPORT.md` §§1, 6).
- A second rhinoceros brain MRI of any species — none openly available after the full registered search (#44).
- A dolphin hippocampus volume in the MRI class — delineation failed at QC; no volume claimed (#47).
- Per-specimen measurement uncertainties for the literature test set — not published by the sources (`BENCHMARK.md`, Caveats).
- Symmetric benchmark (Patzke curve graded against MRI values) — not run (`BENCHMARK.md`, Caveats).

## References discipline

References in the paper are limited to works cited in the source materials or introduced by the binding precedent sweep (Nadkarni et al. 2019). Bibliographic details (journal, volume, pages) are reproduced only where a source gives them; bracketed placeholders in the paper's reference list mark titles/details the sources do not give, rather than supplying them. No DOIs were added except where the sweep itself gives them in its discussion — the paper's reference list omits DOIs throughout for consistency with the project sources. Reep et al. 2007 full citation as in sources: *Brain, Behavior and Evolution* 70:57–70. Patzke et al. 2015: *Brain Structure and Function* 220:361–383. Bhagwandin et al. 2017: *Frontiers in Neuroanatomy* 11:74.

## NOVELTY CLAIMS — SWEEP-ADOPTED (formerly PENDING SWEEP)

Precedent sweep completed 2026-11-17 (`~/workspace/papers/precedent-sweep/SWEEP.md`, §P1). Verdicts below are adopted in the paper in the surviving wording shown. This section replaces the pre-sweep "pending" list; status of each claim: **SWEEP-ADOPTED**.

1. **P1a — HOLDS.** Surviving wording as used in the paper (§3.2): "To our knowledge, 2.02 cm³ is the first MRI-based hippocampus volume for the lion (*Panthera leo*)." Prior value (4.50 cm³) is histological (Reep et al. 2007, via Patzke et al. 2015), not MRI. Closest prior checked by sweep: Reep et al. 2007; Sakai et al. 2016 (CT endocast, cannot yield hippocampus).
2. **P1b — HOLDS.** Surviving wording as used in the paper (§3.1): "To our knowledge, this is the first end-to-end, voxel-level audit of the region-label files of a public comparative-brain atlas archive," finding 53 of 71 labels real and 18 empty placeholders. Prior audits (Rohlfing 2013) covered mislabelling/orientation in a single human atlas, not empty delineations in a comparative archive.
3. **P1c — NARROWED, rescoped wording adopted throughout (title, abstract, §§1.1, 1.3, 3.4, 4.2, 4.4).** Surviving wording: "For the species/regions actually paired between the shrinkage-corrected histological compilation (Stephan/Baron/Reep, as tabulated by Patzke et al. 2015) and MRI-atlas volumes, the compiled histological values average ~1.6× the MRI values — a dataset-pair ratio, not a systematic property of histology (raw histology shrinks below MRI, and regional ratios reverse, e.g. pallidum −38% in Nadkarni et al. 2019)." The paper MUST and DOES: (1) cite Nadkarni et al. 2019, Reep et al. 2007 (shrinkage factors 2.1–2.9), Wagstyl et al. 2020 (factor 1.931); (2) state explicitly that raw (uncorrected) histology runs below MRI. The broad pre-sweep wording ("histological volumes run ~1.6× above MRI volumes" as a property of histology) does **not** appear as a claim anywhere in the paper; the original brief title was rescoped for this reason.
4. **Additional hedged novelty statements in the paper, all within audit/sweep coverage and listed here for completeness:** (a) no meta-analysis / no composite compilation-to-compilation quantification across hundreds of species found within the literature audit's coverage (§4.4; largest prior paired quantification: Navarrete et al. 2018, 17 species); (b) no standard name for the composite difference found — "Two Rulers" is the project's coinage (§4.4); (c) no MRI-label hippocampus exists for any aquatic species in this archive — a census finding (§3.6), not a literature-first claim. If further prior art surfaces for (a)–(c), these statements are to be rescoped in the same manner as P1c.
