# Quantum-Enhanced Feature Representation for Motor Function Assessment

This repository contains all data, preprocessing, and experimental code used in the study on **Quantum-Enhanced Feature Representation for Cognitive and Motor Function Assessment**, published in *Applied Soft Computing*.

---

## 📂 Repository Structure

```
qe-feature-representation/
├── mci/
│   ├── mci_features.csv / mci_features_quantum.csv
│   ├── pose_features_master.csv
│   ├── qernn_mci.ipynb / rnn_mci.ipynb
├── stroke/
│   ├── stroke_features.csv / stroke_features_quantum.csv
│   ├── qernn_stroke.ipynb / rnn_stroke.ipynb
├── parkinson/
│   ├── final_parkinsons_features.csv / quantum_raw_parkinsons_gait_percent.csv
│   ├── qernn_parkinsons.ipynb / rnn_parkinsons.ipynb
│   └── ablation/
│       ├── qernn_parkinsons_ablation_{cnn,mlp,pca,transformer}.ipynb
│       └── rnn_parkinsons_ablation_{cnn,mlp,pca,transformer}.ipynb
├── *_feature_extraction_standard.ipynb
├── *_quantum_features_extraction.ipynb
└── README.md
```

---

## 🧠 Overview

This repository explores the integration of **quantum-enhanced (QE)** feature encoding with classical deep learning architectures for the assessment of cognitive and motor function.  
We evaluate **classical RNNs**, **CNNs**, **Transformers**, and **MLPs** against their **QE-augmented counterparts (QE-RNN, QE-CNN, QE-Transformer)** using:

- 🧩 **Syn-MCI (synthetic gait dataset)**  
- 🧠 **SN-Gait (stroke gait dataset)**  
- 🧍 **PD-Gait (Parkinson’s gait dataset)**  

Each dataset includes classical and quantum-enhanced feature variants, normalized and aligned for model comparison.

---

## ⚙️ Preprocessing and Feature Extraction

All preprocessing pipelines are included:
- **Synthetic (Syn-MCI):** Pose-based feature generation with temporal derivatives and gait statistics.  
- **Stroke (SN-Gait):** Windowed joint-angle time series with per-subject segmentation.  
- **Parkinson’s (PD-Gait):** Statistical and frequency-domain features (FFT, RMS, skewness, kurtosis, dominant frequency).  

Each extraction notebook (e.g., `mci_feature_extraction_standard.ipynb`) produces both **classical** and **quantum** feature tables (`*_features.csv` / `*_features_quantum.csv`).

Normalization, labeling, and windowing parameters are consistent across datasets for fair comparison.

---

## 🧪 Methodology

- Quantum circuits executed on IBM’s **ibm_kyiv (Eagle-r3)** backend via the Qiskit Runtime Sampler (v1).  
- Shallow encoding + entanglement layers optimized for NISQ constraints.  
- Deduplication and caching implemented to minimize redundant quantum executions.  
- Cross-validation (5-fold) with independent caches per fold ensures isolation between training and test partitions.  
- Ablation notebooks evaluate the effect of architecture and preprocessing variants.

---

## 🔍 Reproducibility

All scripts required for reproducing the datasets, feature extraction, and training are provided.  
Due to the double-blind review process, this repository is anonymized; it will be made public with full author metadata upon paper acceptance.

---

## 🧾 Citation

Jalloul, B., Bouaziz, B., & Mahdi, W. (2026). Quantum-enhanced recurrent models for cognitive–motor assessment. Applied Soft Computing, 114696. https://doi.org/10.1016/j.asoc.2026.114696
