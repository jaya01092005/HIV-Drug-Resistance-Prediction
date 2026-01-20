
# 🧬 HIV Drug Resistance Prediction using BioMedBERT

This repository contains the implementation of an **HIV-1 drug resistance prediction system** using **BioMedBERT**, a domain-specific transformer model trained on biomedical literature.
The project focuses on predicting resistance for **three major classes of antiretroviral drugs** using sequence-level mutation data.

> ⚠️ **Note:** This work emphasizes *high recall, low false-positive rate, and minimal loss*, which is critical in clinical decision-support systems.

---

## 📌 Project Overview

HIV drug resistance remains a major challenge in antiretroviral therapy. Traditional machine learning approaches struggle to capture the complex contextual dependencies between mutations.

This project leverages **BioMedBERT** to:

* Model long-range mutation interactions
* Improve resistance prediction reliability
* Achieve strong performance without k-fold cross-validation

---

## 🧠 Drug Classes Covered

The project is organized into **three independent notebooks**, each targeting a specific drug class:

1. **Protease Inhibitors (PI)**
2. **Nucleoside Reverse Transcriptase Inhibitors (NRTI)**
3. **Non-Nucleoside Reverse Transcriptase Inhibitors (NNRTI)**

Each notebook follows the same experimental pipeline but is trained on **class-specific datasets**.

---

## 📂 Repository Structure

```
.
├── PI_Drug_Resistance_Prediction.ipynb
├── NRTI_Drug_Resistance_Prediction.ipynb
├── NNRTI_Drug_Resistance_Prediction.ipynb
└── README.md
```

---

## 🔬 Dataset

* Source: **Stanford HIV Drug Resistance Database**
* Data includes:

  * HIV-1 mutation sequences
  * Phenotypic resistance labels
  * Drug-specific resistance measurements
* Extensive preprocessing was performed to:

  * Handle sequence variability
  * Normalize mutation representations
  * Make the dataset compatible with transformer-based models

> The dataset is publicly available but **not originally model-ready**. Significant preprocessing was required.

---

## ⚙️ Model & Methodology

* **Model:** BioMedBERT (fine-tuned)
* **Input:** Mutation sequences
* **Output:** Binary resistance prediction
* **Loss Function:** Binary Cross-Entropy
* **Training Strategy:**

  * No k-fold cross-validation
  * Single robust train-validation split
  * Focus on real-world generalization

---

## 📊 Evaluation Metrics

Each notebook reports:

* Accuracy
* Precision
* Recall (priority metric)
* F1-Score
* Loss
* Precision-Recall Curve
* PR-AUC

> The model achieves **competitive accuracy (≈89–92%) with significantly lower loss** compared to earlier CNN-based approaches.

---

## 🚀 Key Highlights

* First known application of **BioMedBERT** on this dataset
* Excellent recall and very low false-positive rate
* Class-wise modeling instead of a single generalized classifier
* Research-oriented design with reproducibility in mind

---

## 🛠️ Requirements

Recommended environment:

* Python ≥ 3.8
* PyTorch
* Transformers (HuggingFace)
* NumPy, Pandas
* scikit-learn
* Matplotlib / Seaborn

You can install dependencies using:

```bash
pip install torch transformers scikit-learn pandas numpy matplotlib
```

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Open any notebook:

```bash
jupyter notebook PI_Drug_Resistance_Prediction.ipynb
```

3. Run cells sequentially to:

   * Load data
   * Preprocess sequences
   * Train BioMedBERT
   * Evaluate results

---

## 📌 Research Note

This project is designed as a **research prototype** and not a clinical diagnostic tool.
Predictions should **not** be used directly for medical decision-making.

---

## 👩‍💻 Author

**Jayashree M**
GitHub: [https://github.com/jaya01092005](https://github.com/jaya01092005)

