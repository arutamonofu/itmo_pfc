# Generation novel EGFR and prediction EGFR physico-chemical properties for pharmaceutical purposes

A **computational pipeline** designed to find new analogues for already existing pharmaceutical compounds against various types of cancer.  
It automates key steps ranging from **data collection and preprocessing** to **molecule generation, selection, and evaluation**.

---

## About the Project

The project integrates several sequential stages:

1. **Data Collection & Processing**  
   - Automatic download of bioactivity data from **ChEMBL** and **PubChem**  
   - Preprocessing, cleaning, and standardization of raw data  

2. **Descriptor Generation**  
   - Calculation of molecular descriptors and fingerprints  
   - Tools: **RDKit**, **Mordred**, **Morgan fingerprints**  

3. **Predictive Model Training**  
   - Machine learning model (**XGBoost**) for predicting biological activity (**pIC50**)  
   - Hyperparameter optimization with **Optuna**  

4. **Molecule Generation**  
   - Integration with external tools like **REINVENT4 (Mol2Mol)** to create new molecular structures  

5. **Virtual Screening & Selection**  
   - Multi-stage filtering of candidates:  
     - Programmatic filters (**QED**, **SA Score**)  
     - ML-based activity prediction  
     - Final ADME/toxicity assessment via **SwissADME**  

---

## The entire project is managed via a manual consecutive launch of notebooks
1. Data_processing.ipynb
2. Pred_LGBM.ipynb
3. RandomForest.ipynb
4. molecule_selection.ipynb

## Core Technologies & Libraries
1. Cheminformatics: RDKit, Mordred
2. Machine Learning: Scikit-learn, XGBoost, Optuna
3. Data Processing: Pandas, NumPy

## CONCLUSION
Our models achieved relatively low R² scores, which is likely due to the need for more thorough validation on the dataset of generated molecules. Improving the validation process should help refine model performance and reliability.
