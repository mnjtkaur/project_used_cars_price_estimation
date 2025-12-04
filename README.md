# Used Cars Price Estimation

A clean, reproducible project for estimating the market price of used cars using a public Kaggle dataset. The notebooks and data in this repository document the full workflow: data ingestion, cleaning, exploratory analysis, model training, and result evaluation.

Key goals
---------
- Provide reproducible preprocessing and feature engineering for used car pricing.
- Compare several machine learning models (linear regression, KNN, random forest, XGBoost) and report performance.
- Share findings and recommendations for model selection and improvement.

Dataset
-------
The project uses the "Used Car Price Prediction" dataset from Kaggle:

- https://www.kaggle.com/datasets/taeefnajib/used-car-price-prediction-dataset

Local data files (in `Data/`):

- `used_cars.csv` — original dataset (downloaded from Kaggle)
- `Cleaned_data.csv` — cleaned and preprocessed data used for EDA
- `data_model.csv` — final dataset prepared for model training and evaluation

Repository layout
-----------------
- `Data/` — raw and processed CSV files
- `Notebook/` — Jupyter notebooks with the analysis and model experiments
	- `data_cleaning.ipynb` — step-by-step data cleaning and preprocessing
	- `EDA.ipynb` — exploratory data analysis and visualization
	- `Testing Models/` — per-model notebooks: `modeling_linear_reg.ipynb`, `modeling_KNN.ipynb`, `modeling_random_forest.ipynb`, `modeling_XGB.ipynb`, etc.
- `Model Testing Results/` — saved evaluation results and comparison tables
- `Executive Summary/` — concise findings and recommendations suitable for stakeholders

Quick start
-----------
1. (Optional) Create and activate a Python virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install required packages (adjust versions as needed):

```bash
pip install -r requirements.txt
```

Install the common packages used by the notebooks:

```bash
pip install jupyter pandas numpy scikit-learn matplotlib seaborn xgboost
```

3. Start Jupyter and open the notebooks:

```bash
jupyter notebook
```

4. Recommended order to reproduce results:
	- Run `Notebook/data_cleaning.ipynb` to generate cleaned datasets in `Data/`.
	- Open `Notebook/EDA.ipynb` for analysis and visual checks.
	- Run the model notebooks in `Notebook/Testing Models/` to train and evaluate models.

Reproducibility notes
---------------------
- Notebooks expect the CSV files in `Data/` to match the names listed above. If your versions differ, update the paths inside the notebooks.
- For consistent results, pin package versions in `requirements.txt`. You can create one from your environment with `pip freeze > requirements.txt`.

Contributing
------------
- If you add new preprocessing steps or models, please include a short README or notebook describing the change and any new dependencies.
- Open an issue or submit a pull request for improvements or bug fixes.

Contact & license
-----------------
Repository owner: `mnjtkaur`.

This repository currently does not include a license. Add a `LICENSE` file if you plan to publish or share the work.
