# Explainable-Methods

# Prediction and Explainability through CRISPRedict ,CRISPRAidit, deepHF and CRISPROn on SpCas9-Endo(Knockout)  and Hanna Datasets

This repository contains a reproducible pipeline for predicting CRISPR-Cas9 cleavage efficiency and interpreting model predictions using CRISPRedict, CRISPRAidit, DeepHF and CRISPROn on the **Knockout** and **Hanna datasets** respectively. The workflow includes feature extraction, model prediction, and SHAP-based explainability using a trained statsmodels regressor.

---

##  Repository Structure
Explainable-Methods/
├── crispredict_knockout_prediction_and_explainability.ipynb
└──  crisprAidit Knockout_prediction_and_explainability.ipynb (1).ipynb
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

The dataset used in this analysis is the **Knockout dataset** and **Hanna dataset**: 
You can find it under: `data/30nt crispredict scores data.csv`, `63nt CRISPRAidit scores data`, `Prepared_23nt_DeepHF_Input` and  `23nt_CRISPRon_Scores data` for Knockout dataset while `30nt crispredict scores data - Copy - Hanna - Copy`, `63nt CRISPRAidit scores data - Copy - Hanna - Copy`, `Prepared_23nt_DeepHF_Input - Copy-Hanna - Copy` and `30nt_CRISPRon_Scores data - Copy - Hanna - Copy` for Hanna dataset.

---

##  Workflow Summary

The notebook performs the following steps:

1. Load the Knockout and Hanna datasets  
2. Automatically detect the gRNA sequence column  
3. Extract CRISPRedict, CRISPRAidit, deepHF and CRISPROn relevant biological features using original `features.py` logic.
4. Predict cleavage efficiency scores using a pre-trained statsmodels model  
5. Use SHAP to explain the contribution of each feature to the predicted outcome  
6. Save the results with prediction scores and SHAP values

---

## Output

The output file contains:
- Original sequences
- Predicted cleavage scores
- SHAP values for all important features

 Located in: `results/prediction_scores_with_shap_values`, `predictions_shap_values_with_all_features`, `Predicted_Efficiencies_Perfect_Match_Final`and `CRISPRon_Predictions_Only_20250430-163131`(these are resuts of crisprEdict, crisprAidit, deep HF and crisprOn respercitively for Knockout dataset). While `CRISPRedict_SHAP_Results`, `predictions_shap_values_with_all_features`, `Predicted_Efficiencies_Perfect_Match_Final` are the results for Hanna dataset resperctively.

---

##  How to Run

## Requirements
Python version: 3.7.12
Required libraries for crisprEdict, crisprAidit, deepHF and crisprOn  are listed in requirements.txt
Citation:
**CRISPRedict, CRISPRAidit, DeepHF and CRISPROn (original tools):**  
1. Konstantakos, V., Nentidis, A., Krithara, A., & Paliouras, G. (2022). *CRISPRedict: a CRISPR‑Cas9 web tool for interpretable efficiency predictions*.
2. Heng Zhang, Jianfeng Yan, Zhike Lu and Lija Ma et al. (2023).  *Deep sampling of gRNA in the human genom and deep-learning-informed prediction of gRNA activities*.
3. Daqi Wang, Chengdong Zhang et al. (2019).  *Optimized CRISPR guide RNA design for two high-fidelity Cas9 variants by deep learning *.
4. Xi Xiang, Zhangying Dong, Lijun Liu et al. (2021). *Enhancing CRISPR-Cas9 gRNA efficiency prediction by data integration and deep learning*. 

Acknowledgments

Developed by Faiza Hasin for explainability analysis of CRISPR-Cas9 cleavage prediction.
Special thanks to the authors of CRISPRedict, CRISPRAidit, deepHF and CRISPROn.

suport:
If you have any other questions, please contact us at
faiza.hasin@uniba.it or faizamaqsood782@gmail.com



