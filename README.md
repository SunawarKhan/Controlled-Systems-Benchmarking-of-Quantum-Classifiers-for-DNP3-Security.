# DNP3 Quantum-IDS — Reproducibility Package

Controlled Systems Benchmarking of Quantum Classifiers for DNP3 Security: Encoding, Scaling, Finite-Shot Reliability, and Classical–Quantum Trade-offs.

## Authors
- **Sunawar Khan** — National College of Business Administration and Economics, Lahore, Pakistan
- **Rahma Zayoud** — Université de Moncton, Moncton, NB, Canada
- **Abdullah J. Alzahrani** — University of Ha'il, Ha'il, Saudi Arabia
- **Sghaier Guizani** — Alfaisal University, Riyadh, Saudi Arabia / Université de Moncton, Canada
- **Habib Hamam** — Université de Moncton, Canada / University of Johannesburg, South Africa / IITG, Gabon

## Contents
- `DNP3_complete_pipeline.ipynb` — single self-contained notebook that regenerates every result (WP1–WP6 plus the four model families, binary hierarchical bootstrap, confusion matrices, base-rate, data audit, PCA curve, classical controls and ceiling).
- `results_tables/` — machine-readable outputs (CSV/JSON) for every table.
- `figures/` — all generated figures used in the manuscript.

## Data
Public DNP3 intrusion detection dataset (Radoglou-Grammatikis et al., IEEE Dataport 2022, doi:10.21227/s7h0-b081): `CICFlowMeter_Training_Balanced.csv`, `CICFlowMeter_Testing_Balanced.csv`.

## Run
Open the notebook on Kaggle/Colab, add the two CSVs as input, set `QUICK_TEST=False`, Run All. CPU is sufficient (8–12 qubit statevector simulation). Runtime ~3–5 h.

## Key findings (real run, 10 seeds)
- **Encoding**: Amplitude vs angle at matched 8 features = +0.025 (p=0.18) — non-significant; amplitude scales with features and saturates ~32.
- **Binary AUC**: Classical MLP (0.912) significantly beats QNN-DRU (0.901), p≈0.004.
- **Trade-offs**: Classical ≥ quantum on every task; full-feature boosting ceiling ≈0.985.
- No quantum advantage claimed.

## Citation

If you use this code, benchmark protocol, or results in your research, please cite:

@article{S.Khan et al,
  title={Controlled Systems Benchmarking of Quantum Classifiers: Encoding, Scaling, Finite-Shot Reliability, and Classical--Quantum Trade-offs for DNP3 Security},
  author={Khan, Sunawar and Zayoud, Rahma and Alzahrani, Abdullah J. and Guizani, Sghaier and Hamam, Habib},
  journal={Github Repository},
  year={2026},
}
