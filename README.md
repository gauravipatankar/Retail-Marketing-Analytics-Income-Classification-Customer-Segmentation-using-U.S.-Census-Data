# Retail-Marketing-Analytics-Income-Classification-Customer-Segmentation-using-US-Census-Data  

## Overview: 
This project simulates a real-world data science project for a **retail client** seeking actionable marketing insights from population data.  
It consists of two major components:  

1. **Income Classification Model** – Predicts whether an individual earns **more or less than $50,000 per year** using 40 demographic and employment-related variables.  
2. **Customer Segmentation Model** – Performs **unsupervised clustering** to identify distinct socio-demographic segments and generate interpretable population personas for targeted marketing.  

Both analyses are built on **U.S. Census Bureau Current Population Survey (1994–1995)** data, demonstrating end-to-end handling of real-world, messy demographic data:  
**data cleaning → feature engineering → modeling → evaluation → insight generation.**

---

##  Repository Structure  
```
├── deliverable-1-classification-model.ipynb
├── deliverable-2-segmentation-model.ipynb
├── deliverable-1-classification-model.pdf
├── deliverable-2-segmentation-model.pdf
├── census-bureau.data
├── census-bureau.columns
└── README.md
```

- The `.ipynb` notebooks contain the complete, executable code and results.  
- The `.pdf` files are exported notebooks for review.  
- The dataset files must be present in the same directory to reproduce the analysis.  

---

## Environment Setup  

1. Create and activate a virtual environment  
```bash
python -m venv env
source env/bin/activate       # macOS/Linux
env\Scripts\activate          # Windows
```
2. Install dependencies

If `requirements.txt` is available:
```
pip install -r requirements.txt
```
Otherwise, manually install the key libraries:
```
pip install pandas numpy matplotlib seaborn scikit-learn \
imbalanced-learn xgboost lightgbm catboost feature-engine \
scipy plotly
```

- Python 3.9+ recommended

---
## Data
Place both files in the project root directory:
- `census-bureau.data`
- `census-bureau.columns`

They are loaded as:
```
with open("census-bureau.columns") as f:
    columns = [line.strip() for line in f.readlines()]

df = pd.read_csv("census-bureau.data", names=columns, header=None)
```
---
## To Run:
1. Launch Jupyter Notebook
   ```
   jupyter notebook
   ```
2. Open and run:
  - `deliverable-1-classification-model.ipynb`
  - `deliverable-2-segmentation-model.ipynb`
3. Execute all cells sequentially (**Cell → Run All**) to reproduce full results.


