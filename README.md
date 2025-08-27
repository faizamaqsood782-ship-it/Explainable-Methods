# Explainable-Methods

# CRISPRedict: Prediction and Explainability on Knockout Dataset

This repository contains a reproducible pipeline for predicting CRISPR-Cas9 cleavage efficiency and interpreting model predictions using CRISPRedict, CRISPRAidit, DeepHF and CRISPROn on the **Knockout dataset** and **Hanna dataset**. The workflow includes feature extraction, model prediction, and SHAP-based explainability using a trained statsmodels regressor.

---

##  Repository Structure
Explainable-Methods/
├── crispredict_knockout_prediction_and_explainability.ipynb
└──  crisprAidit_prediction_and_explainability.ipynb (1).ipynb
├── requirements.txt
├── data/
│ └── 30nt crispredict scores data.csv
└──   63nt CRISPRAidit scores data
├── results/
│ └── prediction_scores_with_shap_values
└──predictions_shap_values_with_all_features
└── README.md


---

##  Datasets

The dataset used in this analysis is the **Knockout dataset** and **Hanna dataset**,containing 30-nt sequences and associated scores.  
You can find it under: `data/30nt crispredict scores data.csv`

---

##  Workflow Summary

The notebook performs the following steps:

1. Load the Knockout dataset  
2. Automatically detect the gRNA sequence column  
3. Extract CRISPRedict-relevant biological features using `features.py`  
4. Predict cleavage efficiency scores using a pre-trained statsmodels model  
5. Use SHAP to explain the contribution of each feature to the predicted outcome  
6. Save the results with prediction scores and SHAP values

---

## Output

The output file contains:
- Original sequences
- Predicted cleavage scores
- SHAP values for all important features

 Located in: `results/prediction_scores_with_shap_values`

---

##  How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/faizamaqsood782-ship-it/Explainable-Methods.git
   cd Explainable-Methods
    ## Requirements
Python version: 3.7.12
Required libraries are listed in requirements.txt
Citation:
**CRISPRedict (original tool):**  
Konstantakos, V., Nentidis, A., Krithara, A., & Paliouras, G. (2022). *CRISPRedict: a CRISPR‑Cas9 web tool for interpretable efficiency predictions*.
Acknowledgments
Developed by Faiza Hasin for explainability analysis of CRISPR-Cas9 cleavage prediction.
Special thanks to the authors of CRISPRedict and SHAP for foundational tools.
suport:
If you have any other questions, please contact us at
faiza.hasin@uniba.it or faizamaqsood782@gmail.com



