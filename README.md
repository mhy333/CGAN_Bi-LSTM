# CGAN_Bi-LSTM

This repository supports the manuscript:

> **Lost Circulation Events Diagnosis Based on CGAN Data Augmentation and Domain Knowledge-Guided Bi-LSTM**  
> Submitted to *Computers & Geosciences*

---

## Project Description

This study proposes a novel framework to improve lost circulation event diagnosis in drilling operations. The framework integrates:

- **Conditional Generative Adversarial Networks (CGAN)** for data augmentation  
- **Bidirectional Long Short-Term Memory (Bi-LSTM)** for sequential modeling  
- **Domain knowledge embedding** via a multidimensional lost circulation risk model (MLR)

This CGAN_Bi-LSTM model achieves high performance in both accuracy and generalization.

---

## Usage

### 1. Environment Setup

Install dependencies using pip:

```bash
pip install -r requirements.txt
```

### 2. Run the Three Notebooks

- `1_Data_Augmentation.ipynb`: Train CGAN to generate synthetic samples
- `2_Lost_Circulation_Events_Diagnosis.ipynb`: Train and evaluate LSTM/Bi-LSTM models
- `3_Knowledge_Embedding.ipynb`: Integrate domain knowledge using MLR features

You can run each notebook in order using Jupyter.

---

## Data Availability

Due to confidentiality agreements, the full dataset is not publicly available.  
We provide an anonymized **sample file** with 10 representative records:

```
data/Well_B_MLR_example10.csv
```

This file demonstrates the structure and can be used for testing.  
For further collaboration, please contact the corresponding author.

---

## Model Description

- **CGAN** is used to augment minority class samples by conditioning on leak types.
- **Bi-LSTM** architecture:
  - Layer 1: Bidirectional LSTM (64 units)
  - Layer 2: Dense layer with sigmoid activation
- **MLR (Multidimensional Lost Circulation Risk Index)** is embedded in two ways:
  - As additional input features (MLR-in)
  - To guide attention weight allocation (MLR-at)

---

## Results

Experimental outputs are saved in:

```
results/
├── figures/   # ROC, PR curves, confusion matrices
└── tables/    # Performance metrics and classification reports
```

Key findings:
- CGAN_Bi-LSTM achieved **Accuracy > 95%**, **F1-score > 0.95**, **AUC > 0.98**
- MLR-based embedding improved both generalization and interpretability

---

## License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

---

## Contact

- **Corresponding Author**: huayanmu5@gmail.com  
- **Affiliation**: China University of Petroleum (Beijing), College of Artificial Intelligence

---

