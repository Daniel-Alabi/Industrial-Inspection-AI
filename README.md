# Industrial-Inspection-AI

Industrial inspection demonstrations covering sensor-based machine learning, image-based defect detection, and interactive non-destructive testing (NDT) simulation.

**Scope:** All four notebooks generate synthetic data internally and include saved plots and evaluation outputs. Their metrics describe those synthetic experiments. The NDT simulator uses simplified physical models and handbook-typical material constants; its **Physics notes** document assumptions and omitted effects.

## Entry points

Browse the notebooks on GitHub to inspect code and saved outputs, or run them locally. Choose sensor workflows (01–02), vision workflows (03–04), or the interactive NDT simulator.

| Entry point | Scope | What to inspect |
|---|---|---|
| [01 · Vibration anomaly detection](01_vibration_anomaly_detection.ipynb) | Synthetic accelerometer signals; unsupervised ML | Time traces and Welch spectra; RMS, kurtosis, crest factor, and band-energy features; Isolation Forest trained on healthy recordings, with held-out confusion matrix and classification report. |
| [02 · Predictive maintenance](02_predictive_maintenance.ipynb) | Synthetic multivariate sensor histories; supervised ML | Rolling features and train/test separation by machine; Random Forest failure classification and clipped remaining useful life (RUL) regression; precision–recall evaluation, RUL mean absolute error, and prediction plots. |
| [03 · Surface-defect CNN](03_surface_defect_cnn.ipynb) | Synthetic surface images; supervised vision | TensorFlow/Keras CNN classifying OK, scratch, pit, and crack images; training curves, validation confusion matrix, and prediction inspection. |
| [04 · Visual anomaly autoencoder](04_visual_anomaly_autoencoder.ipynb) | Synthetic surface images; normal-only training | Convolutional autoencoder, reconstruction-error scores and heat maps, threshold from normal validation data, and image-level ROC-AUC and classification results. |
| [NDT Bench simulator](ndt_simulator.html) | Browser simulation; simplified inspection physics | Ultrasonic, eddy-current, radiographic, magnetic-particle, and penetrant testing; adjustable materials, part/flaw geometry, probe position, technique parameters, and graphical readouts. |

## Run the notebooks

Use a Python 3 Jupyter environment. Dependencies follow the notebooks' imports:

```bash
python -m pip install numpy scipy pandas scikit-learn matplotlib jupyter
# Additional dependency for notebooks 03 and 04:
python -m pip install tensorflow
jupyter lab
```

Open any notebook and run its cells from top to bottom; each is self-contained and requires no external dataset download. Public datasets mentioned in the closing notes are suggested next steps.

## Open the simulator

Download or clone the repository, then open `ndt_simulator.html` directly in a browser. CSS and JavaScript are embedded, so no build step or server is required. Select a technique, adjust the controls, and drag the probe or a flaw in the plan view.

## Supporting material

- [Notebook-series overview](00_README_industrial_inspection_ml.md)
- [NDT archive](ndt-site.tar.gz)
