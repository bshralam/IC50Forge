# IC50-Forge: A Workflow for IC50 Prediction in Cancer Drug Discovery

1) Objective:
This project is a self-directed study to build and validate a machine-learning model for predicting IC50 values for EGFR inhibitors, a key oncology target. 

2) Key Features:
- Computes Morgan Fingerprints(radius = 2)/ECFP4 using RDKit,from SMILES strings of a ChEMBL EGFR bioactivity dataset. 
- Trains a Random Forest regression model to predict pIC50 values.
- Validates the model and visualizes performance with SHAP analysis.
- Computes activity cliffs based on Tanimoto similarity.

3) Tools used:
Python, RDKit, Pandas, Scikit-learn, Matplotlib.

4) EGFR QSAR Performance and SAR Interpretability:

i) Predicted vs experimental pIC₅₀ (parity plot) for the ECFP4-based Random Forest regression model on EGFR inhibitors.

<img width="589" height="590" alt="image" src="https://github.com/user-attachments/assets/9527da6b-29e8-48bb-bd38-ce3bc5730c81" />

ii) SHAP beeswarm plot showing global interpretability for the descriptor-based Random Forest model trained on EGFR pIC₅₀ prediction.

<img width="753" height="340" alt="image" src="https://github.com/user-attachments/assets/6096dd96-9708-4b08-ad26-2208fc7009e6" />

iii) Mean absolute SHAP value ranking for the Random Forest model trained on physicochemical descriptors.

<img width="790" height="340" alt="image" src="https://github.com/user-attachments/assets/fa8f5e3b-fe83-457f-953b-03db65a3e45c" />

iv) Activity cliff structural pairs identified from ECFP4 Tanimoto similarity (≥ 0.85) and large potency disparity (ΔpIC₅₀ ≥ 1.0) in the ChEMBL EGFR dataset.

<img width="600" height="1500" alt="image" src="https://github.com/user-attachments/assets/5f1c6515-50e1-4029-8bd3-09410c330b0f" />



