# Adverse Drug Event Analysis

Exploratory data analysis and machine learning project examining patterns in FDA adverse event reports for prescription opioids and controlled substances.

## Project Structure
```
adverse-drug-event-analysis/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/
│   │   └── drug_events.csv           # Original raw data from FDA API
│   └── cleaned/
│       └── fda_cleaned_data.csv      # Cleaned and processed data
│
├── notebooks/
    ├── phase2_data_curation.ipynb
    ├── phase3_linear_polynomial_regression.ipynb
    └── phase4_logistic_regression.ipynb
```

## Research Questions

1. Are there demographic trends (age, gender) linked to higher risk of adverse drug events?
2. What are the most common adverse reactions reported for prescription opioids and controlled substances?
3. Can we predict the seriousness of a reported adverse event using patient and drug features?

## Data Source

- **API:** FDA OpenFDA Drug Event API
- **Drugs:** OXYCODONE, HYDROCODONE, FENTANYL, ALPRAZOLAM, AMPHETAMINE
- **Records:** ~4,000 adverse event reports after cleaning

## Key Findings

### Phase 2: Exploratory Analysis
- Ages 51-65 experience the highest rates of adverse events
- Females consistently report more adverse events than males
- Drug abuse, toxicity, and ingestion are the most common reactions

### Phase 3: Regression Models
- Linear regression models showed poor predictive power (R² < 0.001)
- Polynomial regression slightly improved results (R² = 0.0032)
- Demographic features alone insufficient for predicting reaction counts

### Phase 4: Classification
- Logistic regression for predicting serious vs. non-serious events
- [Add your Phase 4 results here]

## Technologies

- Python 3.x
- NumPy, Pandas
- Scikit-learn
- Matplotlib, Seaborn
- FDA OpenFDA API

## Setup
```bash
pip install -r requirements.txt
jupyter notebook
```

## Usage

1. Open `notebooks/phase2_data_curation.ipynb` to see data collection and cleaning
2. Open `notebooks/phase3_linear_polynomial_regression.ipynb` for regression analysis
3. Open `notebooks/phase4_logistic_regression.ipynb` for classification models

## Author

Kangho - Northeastern University
Data Science Course Project
```

---

## **Step 4: Create requirements.txt**

Create a file called `requirements.txt`:
```
numpy
pandas
requests
matplotlib
seaborn
scikit-learn
scipy
jupyter
```

---

## **Step 5: Create .gitignore**

Create a file called `.gitignore`:
```
# Jupyter Notebook
.ipynb_checkpoints/
*/.ipynb_checkpoints/*

# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python

# Data files (if too large)
*.csv
data/raw/*

# OS
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/

