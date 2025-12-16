# Transfer Learning with Graph Neural Networks for Solubility Prediction


## 📌 Project Overview

This project aims to predict the aqueous solubility of chemical compounds, a critical physicochemical property in drug discovery and development. The workflow leverages a curated solubility dataset containing molecular structures (SMILES, InChI) and computed molecular descriptors.

The primary objective is to prepare data for **Transfer Learning** using **Graph Neural Networks (GNNs)**, addressing common challenges in chemical datasets such as imbalanced regression targets.

## 📂 Dataset

The project uses the **Curated Solubility Dataset** (`curated-solubility-dataset.csv`), which includes **9,982** chemical compounds.

* **Target Variable:** `Solubility` (LogS, aqueous solubility).
* **Structural Identifiers:** `SMILES`, `InChI`, `InChIKey`.
* **Molecular Descriptors (26 Features):**
    * **Physical:** Molecular Weight (`MolWt`), LogP (`MolLogP`).
    * **Structural:** Ring counts, Rotatable bonds, Atom counts (Heavy, Hetero).
    * **Electronic:** TPSA (Topological Polar Surface Area), Valence Electrons.
    * **Topological:** BalabanJ, BertzCT.

## 🚀 Key Features & Methodology



1.  **Data Ingestion & Cleaning:**
    * Loading curated chemical data.
    * Verification of null values and data integrity.
2.  **Handling Imbalanced Regression (`smogn`):**
    * Installation and setup of the **SMOGN** (Synthetic Minority Over-Sampling Technique for Regression) library to handle skewed solubility distributions, ensuring the model generalizes well across rare solubility ranges.
3.  **Feature Engineering:**
    * Separation of non-numeric identifiers (SMILES, Names) from numeric physicochemical descriptors.
4.  **Exploratory Data Analysis (EDA):**
    * Statistical summary of the `Solubility` target.
    * **Correlation Analysis:** A heatmap visualization to understand collinearity between features like `MolWt`, `HeavyAtomCount`, and `LabuteASA`.

## 🛠️ Tech Stack

* **Python**
* **Pandas & NumPy:** Data manipulation and algebra.
* **Matplotlib & Seaborn:** Visualization and heatmaps.
* **Smogn:** Advanced over-sampling for regression.
* **Scikit-Learn:** Data utilities.





* Implementation of Graph Neural Network (GNN) architecture (e.g., GCN, GAT).
* Transformation of SMILES strings into molecular graphs (Nodes=Atoms, Edges=Bonds).
* Model evaluation using RMSE and $R^2$ metrics.
