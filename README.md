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
   - Machine learning models (**LightGMB**, **RandomForest**) for predicting biological activity (**pIC50**)  
   - Hyperparameter optimization with **Optuna**, **GridSearch**  

4. **Molecule Generation**  
   - Integration with external tools like **REINVENT4 (Mol2Mol)** to create new molecular structures  

5. **Virtual Screening & Selection**  
   - Multi-stage filtering of candidates:  
     - Programmatic filters (**QED**, **SA Score**)  
     - ML-based activity prediction  
     - Final ADME/toxicity assessment via **SwissADME**  

---

## Core Technologies & Libraries
1. Cheminformatics: RDKit, Mordred
2. Machine Learning: Scikit-learn, LightGBM, RandomForest, Optuna, GridSearch
3. Data Processing: Pandas, NumPy

## CONCLUSION
Our models achieved relatively R²<0.5 scores, which is likely due to the need for more thorough validation on the generated molecules dataset. Improving the validation process should help refine model performance and reliability, as well as take a more thorough approach to choosing the hyperparameter space.
