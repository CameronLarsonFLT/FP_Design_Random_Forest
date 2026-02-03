# Random Forest Fluorescent Protein Design

Train and interrogate **Random Forest regressors** on FPbase fluorescent protein sequences to predict photophysical properties and perform **greedy in-silico sequence design**.

This workflow supports:

- Property prediction from amino-acid sequence
- Multi-run model interrogation with randomized train/test splits
- Position × amino-acid mutation scanning
- Greedy sequence optimization (“directed evolution” in silico)
- Downstream characterization with statistics + publication-style plots

Designed for fast iteration in **Google Colab** or local Python.

---

## Features

- Pulls FP sequences directly from the FPbase API
- Species filtering via taxonomy ID (Aequoria, Discosoma, Entacmaea, or All)
- Automatic Stokes shift computation (`em_max - ex_max`)
- One-hot encoding of protein sequences
- Random Forest regression (scikit-learn)
- Supports prediction of:
  - `brightness`
  - `ex_max`
  - `em_max`
  - `stokes_shift`


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CameronLarsonFLT/FP_Design_Random_Forest/blob/main/FP_Regressor_RF.ipynb)

## Notes
- FPbase API: https://www.fpbase.org/api/proteins/
- Intended as an educational / rapid-prototyping baseline model.
