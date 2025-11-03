
# Predicting Medical Insurance Cost

A Streamlit-based web application that predicts a person's medical insurance premium using machine learning models based on personal and health-related inputs.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?logo=python" />
  <img src="https://img.shields.io/badge/Framework-Streamlit-orange?logo=streamlit" />
  <img src="https://img.shields.io/badge/Model-RandomForest|GBM-green" />
</p>

---

## Features

- Predict medical insurance premium based on:
  - Age, BMI, surgeries, chronic diseases, etc.
- ⚙ Compare two ML models: Random Forest & Gradient Boosting
-  Visualize feature importance and distribution
- Explore diabetic vs non-diabetic premium differences
- Trained on sample dataset `Medicalpremium.csv`

---

## Project Structure

```
.
├── app.py                  # Main Streamlit application
├── Medicalpremium.csv      # Input dataset
├── RF_model.pkl            # Random Forest trained model
├── GBM_model.pkl           # Gradient Boosting trained model
├── styles.css              # (Optional) Styling
├── compare.py              # (Optional) model comparison script
└── Pre-processing.ipynb    # Data cleaning / feature engineering notebook
```

---

##  Quick Start

###  1. Clone the repository
```bash
git clone https://github.com/anhtuandante/PredictingMedicalInsuranceCost.git
cd PredictingMedicalInsuranceCost
```

###  2. Install dependencies
We recommend using a virtual environment:
```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install manually:
```bash
pip install streamlit pandas scikit-learn matplotlib seaborn
```

### ▶ 3. Run the app
```bash
streamlit run app.py
```

The app will launch in your browser at `http://localhost:8501`

---

## How It Works

- User inputs health information via sidebar:
  - Age, BMI (auto-calculated from height/weight), surgery history, chronic diseases, etc.
- Two models are loaded from `.pkl` files:
  - `RandomForestClassifier` and `GradientBoostingClassifier`
- Models predict **PremiumPrice**, and both results are compared.
- Tab **Visualizations** allows you to:
  - See top predictive features
  - View confusion matrix
  - Explore distributions by condition (e.g., Diabetes)

---

## Model Training

- Trained using scikit-learn on preprocessed features
- Target variable: `PremiumPrice`
- Models stored as `.pkl` files for deployment

_See `Pre-processing.ipynb` for training pipeline._

---


---
