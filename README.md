# IC50-Forge: A Workflow for IC50 Prediction in Cancer Drug Discovery

1) Objective:
This project develops and validates two complementary ligand-based QSAR pipelines for predicting EGFR inhibitor potency (pIC₅₀), using cleaned ChEMBL bioactivity data to train machine-learning models for IC₅₀ prediction for a key oncology target.
2) Key Features:
- Computes Morgan Fingerprints(radius = 2)/ECFP4 using RDKit,from SMILES strings of a ChEMBL EGFR bioactivity dataset. 
- Two Random Forest regression models were trained using different molecular representations:
i) Structure-based model using Morgan fingerprints (ECFP4) to capture substructural features of molecules.
ii) Property-based model using physicochemical descriptors (Molecular Weight, LogP, H-bond donors/acceptors, TPSA).
- Model interpreted using SHAP (SHapley Additive exPlanations) to quantify feature importance and visualize how each descriptor influences predicted activity.
- Activity cliff analysis performed to identify structurally similar molecule pairs (Tanimoto similarity ≥ 0.85) with large potency differences (ΔpIC₅₀ ≥ 1.0).

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



