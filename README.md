
# Quantum-Enhanced Feature Representation for Motor Function Assessment

This repository contains all data and code used in the experiments described in our ECAI 2025 submission (Paper #2668).

## 📂 Repository Structure

```
qe-feature-representation/
├── mci/
│   ├── mci_features.csv / mci_features_quantum.csv
│   ├── pose_features_master.csv
│   ├── qernn_mci.ipynb
│   └── rnn_mci.ipynb
├── stroke/
│   ├── stroke_features.csv / stroke_features_quantum.csv
│   ├── qernn_stroke.ipynb
│   └── rnn_stroke.ipynb
├── parkinson/
│   ├── final_parkinsons_features.csv
│   ├── quantum_raw_parkinsons_gait_percent.csv
│   ├── qernn_parkinsons.ipynb / rnn_parkinsons.ipynb
│   └── ablation/
│       ├── qernn_parkinsons_ablation_{pca,mlp}.ipynb
│       └── rnn_parkinsons_ablation_{pca,mlp}.ipynb
├── quantum_features_extraction_mci.ipynb
└── .gitattributes
```

## 🧠 Overview

The project evaluates the use of quantum-enhanced (QE) feature encoding for cognitive and motor function classification. We compare traditional RNNs against QE-RNNs across three datasets:
- MCI (synthetic)
- Stroke (clinical)
- Parkinson's (clinical)

Each dataset contains classical and quantum versions of extracted gait features. Experiments are grouped accordingly with separate notebooks per model and dataset.

## 🛠️ Contents

- 📁 `mci/`: Experiments and features for MCI dataset
- 📁 `stroke/`: Experiments and features for stroke dataset
- 📁 `parkinson/`: Experiments and features for Parkinson's dataset including ablation studies
- 📄 `quantum_features_extraction_mci.ipynb`: Notebook for extracting QE features using quantum hardware

## 🧪 Methodology

Each experiment uses PCA-reduced features (4D) as inputs to RNN and QE-RNN models. Quantum-enhanced features were obtained via parameterized circuits executed on IBM Qiskit backends. Ablation studies explore PCA vs raw feature usage, and RNN vs MLP classifier performance.
