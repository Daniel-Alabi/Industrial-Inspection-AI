# Machine Learning for Industrial Inspection — 4-Notebook Series

Four self-contained Jupyter notebooks, ordered from beginner to advanced. All data is
generated synthetically inside each notebook, so they run anywhere with no downloads.
Every notebook ends with pointers to the standard real-world public dataset to graduate to.

| # | Notebook | Data | Task | Level |
|---|----------|------|------|-------|
| 1 | `01_vibration_anomaly_detection.ipynb` | Accelerometer signals | Unsupervised fault detection (Isolation Forest + FFT features) | Beginner |
| 2 | `02_predictive_maintenance.ipynb` | Multivariate sensor streams | Failure classification + Remaining Useful Life regression (Random Forest) | Intermediate |
| 3 | `03_surface_defect_cnn.ipynb` | Camera images | Supervised defect classification (Keras CNN) | Intermediate–Advanced |
| 4 | `04_visual_anomaly_autoencoder.ipynb` | Camera images | Unsupervised anomaly detection + localization (convolutional autoencoder) | Advanced |

## Setup

```bash
pip install numpy scipy pandas scikit-learn matplotlib tensorflow jupyter
```

Then open any notebook with `jupyter lab` or VS Code. Notebooks 1–2 need only
scikit-learn; 3–4 also need TensorFlow (CPU is fine — each trains in about a minute).

## Key concepts covered

- Time- vs. frequency-domain features (RMS, kurtosis, crest factor, band energy)
- Training on healthy/normal data only — the realistic industrial setup
- Rolling-window feature engineering and leakage-free splits (by machine, not by row)
- Precision/recall trade-offs when failures are rare and false alarms are costly
- CNN training, confusion matrices, and inspecting misclassifications
- Reconstruction-error anomaly scoring, percentile thresholds, and defect heat maps

## Real datasets to graduate to

CWRU bearing data (notebook 1), NASA C-MAPSS and AI4I 2020 (notebook 2),
NEU / Severstal / DAGM surface defects (notebook 3), MVTec AD (notebook 4).
For production-grade visual anomaly detection, see Intel's open-source `anomalib`.

All notebooks were executed end-to-end before delivery; outputs (plots, metrics) are embedded.
