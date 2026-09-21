# IGNIS Event Detector — next-month extreme-fire-month early warning

> Part of the **IGNIS** platform — NASA Space Apps Challenge 2026, challenge #9
> *Harmonization of MODIS and VIIRS Hot Spots*. **Private during judging.**

Predicts whether next month will be an extreme fire month (z >= 2 vs 2000-2021 climatology) from lagged harmonized MODIS+VIIRS calendar features across 9 regions. HGB reference: AUC 0.740 / PR-AUC 0.606 on the hard 2022-2026 holdout (the record 2023-24 fire years). Ships portable logistic weights (weights.json) wired into the IGNIS web app for deterministic in-browser scoring.

## Contents
- `train_event_detector.py` — full reproducible training pipeline (real NASA FIRMS data)
- model artifacts (scikit-learn joblib bundles) + `metrics.json`
- `LICENSE` — MIT

## Hugging Face
The same model, with the full model card, lives at
**https://huggingface.co/Nabidnur/ignis-event-detector** (private; request access or see the main repo).

## Main project
https://github.com/Hisernberg/ignis-spaceapps2026 — live app:
https://ignis-spaceapps2026.vercel.app

## Provenance
All training data derives from NASA FIRMS active-fire detections (public domain),
harmonized across MODIS (Terra/Aqua) and VIIRS (S-NPP/NOAA-20/NOAA-21) by the IGNIS
pipeline. No synthetic data is used for supervised labels.
