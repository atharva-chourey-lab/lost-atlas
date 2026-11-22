# Shrinkage-corrected histological compilation values average ~1.6× MRI-atlas values: an audit of a comparative neuroanatomy archive

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24409194.svg)](https://doi.org/10.5281/zenodo.24409194)

Neuroanatomy · 2026

Author: Atharva Chourey
Affiliation: Atharva Chourey Lab (independent research lab)

*Manuscript — not yet peer-reviewed.*

## Abstract

Comparative neuroanatomy rests on volumes measured by different methods in different decades, yet those volumes are routinely pooled as if they were commensurable. We audited a public comparative archive — the Brain Catalogue — and tested whether a scaling relationship fitted to its magnetic resonance imaging (MRI) segmentations could predict the published histological record. The audit covered 71 label files across 37 species: 53 files contained real data and 18 were empty placeholders with a correct grid and zero voxels. After forensic quality control, eight catalogue species supported a pre-registered log–log line relating hippocampus volume to brain volume. We measured 2.02 cm³ in one archived lion MRI. Reep et al. reported 4.50 cm³ by histology in a separate specimen (Reep et al. 2007). In a blind benchmark against 343 published species, pre-registered before the test values were examined, the MRI line failed its registered success criterion decisively: median absolute percentage error 66.0%, against 18.2% for the Patzke et al. (2015) model. Post-hoc decomposition, labelled as such in the underlying records, attributes the failure principally to a compilation-to-compilation ratio: for the species and regions actually paired, the shrinkage-corrected histological compilation values (Stephan/Baron/Reep, as tabulated by Patzke et al. 2015) average ~1.6× the MRI-atlas values at the same brain size, compounded by power-law form failure at small brain sizes. This ratio is a property of that named dataset pair, not a systematic property of histology as a method: raw (uncorrected) histological volumes run below MRI volumes, because histological processing shrinks tissue, and regional ratios reverse (see §1.1 and §4.4). Any comparison that pools the two compilations undeclared inherits the ratio for the paired material.

## Key results

- Archive audit: of 71 label files across 37 species in the Brain Catalogue, 53 contained real data and 18 were empty placeholders with a correct grid and zero voxels.
- Lion hippocampus: we measured 2.02 cm³ in one archived lion MRI; Reep et al. reported 4.50 cm³ by histology in a separate specimen — a ~2.2× difference between specimens which, on its own, does not show which method accounts for the gap.
- Blind benchmark against 343 published species, pre-registered before the test values were examined: the MRI line's median absolute percentage error was 66.0%, against 18.2% for the Patzke et al. (2015) model — the registered success criterion failed decisively.
- The ~1.6× figure is a compilation-to-compilation ratio for the species and regions actually paired (Stephan/Baron/Reep via Patzke et al. 2015 vs MRI-atlas values), not a property of histology as a method: raw, uncorrected histological volumes run below MRI volumes.

## Read the paper

- [paper.md](paper.md) — full text (Markdown)
- [paper.pdf](paper.pdf) — full text (PDF)

## Sources and fidelity

Every quantitative claim in the paper is traced to its source file in [SOURCES.md](SOURCES.md). Novelty claims were checked against the published literature before release; where a prior work already held a claim, the paper says so and cites it.

## Corrections

- 2026-11-22: The abstract and key results previously stated that the 2.02 cm³ MRI value and the 4.50 cm³ histology value came from the same lion specimen. They did not: the histology value is from a separate specimen (Reep et al. 2007, specimen 62-79), as §4.1 of the paper states. The wording has been corrected above; no measurement or result changes.

## Licence

This work is licensed under a [Creative Commons Attribution 4.0 International Licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it with attribution to Atharva Chourey, Atharva Chourey Lab.

## Cite this work

Chourey, Atharva (Atharva Chourey Lab). Public manuscript record, v1.0.0-publication. Zenodo. https://doi.org/10.5281/zenodo.24409194
