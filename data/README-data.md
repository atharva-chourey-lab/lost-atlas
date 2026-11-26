# Data Package — P1 (Lost Atlas)

Accompanies: "Shrinkage-corrected histological compilation values average ~1.6× MRI-atlas values: an audit of a comparative neuroanatomy archive" (Atharva Chourey, Atharva Chourey Lab).

**Status: deposited 2026-11-26.** These files are deposited in Zenodo as part of the manuscript record (concept DOI [10.5281/zenodo.24409193](https://doi.org/10.5281/zenodo.24409193); the deposited version archives this folder as `data/` alongside the manuscript), minted via the lab's Zenodo↔GitHub integration from https://github.com/atharva-chourey-lab/lost-atlas. The DOI is cited in the manuscript's Data & Code Availability statement.

**Provenance.** All files are tidy outputs copied unchanged from the source project `~/workspace/brain-scan-comparison/outputs/` on 2026-11-17. No values were altered in copying. Source scans and labels are NOT included: Brain Catalogue scans/labels are available from the catalogue's Zenodo records and website under CC BY-NC 4.0 (lion: Zenodo record 44855; black rhinoceros: record 44797, mesh record 44795); M-CRIB 2.0 from OSF node 4vthr. Literature values were transcribed from Reep et al. (2007) Table 1 and Patzke et al. (2015) Table 1, as cited in the manuscript.

## Files

| File | Rows | Contents |
|---|---|---|
| `benchmark_testset.csv` | 343 | The blind-benchmark roster and grading: one row per test species with subset (Reep primary / Patzke compilation), brain volume, published hippocampus volume, the registered line's prediction, signed and absolute percentage errors for the line and for the Patzke model. The scorecard in manuscript §3.4 / Table 1 is computed from this file. |
| `cross_species_volumes.csv` | 37 | First-pass cross-species volumetry for all 37 catalogue species (brain, telencephalon, hippocampus, striatum and other regions where labels exist), with voxel zooms. Superseded in detail by v2/v3; retained for the audit trail. |
| `cross_species_volumes_v2.csv` | 37 | Cross-species volumes, version 2: per-species brain-volume source tagged (catalogue Atlas mask vs Otsu mask), hippocampus and striatum notes. Source of the verified ten-species hippocampus set in §3.2. |
| `cross_species_volumes_v3.csv` | 37 | Cross-species volumes, version 3 (final table of record for the catalogue volumetry). |
| `label_forensics.csv` | 10 | Forensic QC of the ten initially verified hippocampus labels: volume, component counts, top-component shares, symmetry verdicts. Basis for the exclusions (sloth bear, giraffe) in §2.3/§3.2. |
| `measurements.csv` | 44 | Project measurement ledger: species, specimen, region, value, unit, normalisation, source, method, value type and confidence for the study's individual measurements. |
| `human_volumes_per_subject.csv` | 10 | M-CRIB 2.0 newborn reference: per-subject regional volumes for the 10 term neonates, including hippocampus (mean 2.90 ± 0.31 cm³ used in the registered point check, §2.3). |
| `human_wm_volumes_per_subject.csv` | 10 | M-CRIB 2.0 per-subject white-matter tract/region volumes for the same 10 neonates. |
| `lion_volume_sensitivity.csv` | 5 | Lion brain-volume sensitivity to the Otsu threshold factor (the 178–194 cm³ band around the 188.1 cm³ value used in §3.2). |
| `felid_reconciliation_testA.csv` | 2 | Felid reconciliation Test A (D99 atlas propagation): per-species propagated volumes and overlap statistics. Test graded VOID in §3.3. |
| `felid_reconciliation_testB.csv` | 2 | Felid reconciliation Test B (boundary sensitivity): catalogue volumes, +1-voxel and +2-voxel dilations, Reep et al. values, and gap-closure percentages (lion 15.5%/34.4%; leopard 19.2%/38.4%). Basis of the §3.3 verdict. |
| `rhino_boundary_sensitivity.csv` | 2 | Black rhinoceros label boundary sensitivity: catalogue, erode-1 and dilation volumes with percentage changes. |
| `rhino_anomaly_mri_class_table.csv` | 14 | MRI-class comparison table for the rhinoceros investigation: species, brain and hippocampus volumes, shares, residuals against the registered line and against the Patzke model (§3.5). |
| `morphospace_features.csv` | 24 | Morphospace features per specimen/point (volume, shape proxies, principal components) from the project's exploratory morphospace analysis. |
| `morphospace_distances.csv` | 13 | Pairwise morphospace distances (z-space) between the points in `morphospace_features.csv`. |

## Not included (by design)

- Raw MRI scans, segmentation (`.nii.gz`) files, meshes and QC overlay images — bulk source data, available from the Brain Catalogue under CC BY-NC 4.0 (records above).
- Analysis scripts — held in the source project's `scripts/` folder; the manuscript's Data & Code Availability statement covers their release on publication.
- Narrative project records (REPORT.md, BENCHMARK.md, PREDICTION.md, pre-registrations, processing log, literature audit) — the registration and audit trail; available from the lab on request and slated for the publication repository per the manuscript statement.

## Licence note for the deposit

The CSVs are the lab's own derived measurements and transcriptions of published tables. The deposit is licensed CC BY 4.0 (the record's licence), covering the lab's own outputs; the underlying scans remain CC BY-NC 4.0 from the Brain Catalogue and are not part of this deposit.
