# ml_classification_anjana
# Title: Heart Disease Classification Project
**Author:** Anjana Dhakal  
**Date:** November 10, 2025

## Overview: 

Healthcare providers often rely on predictive models to identify heart disease risks early, enabling timely interventions. This project uses machine learning classification to predict heart disease presence from the UCI Heart Disease Dataset (Cleveland database), which includes 303 samples and 13 clinical features like age, sex, chest pain type, blood pressure, and cholesterol. The target is binarized (0: no disease, 1: disease present) for binary classification.
This analysis showcases classification techniques applied to a medical dataset. Key steps include:

- Loading and exploring the dataset for patterns and anomalies.
- Preprocessing: Handling missing values, encoding categoricals, scaling numerics, and binarizing the target.
- Selecting clinically relevant features.
- Training and evaluating Logistic Regression and Random Forest models.
- Comparing performance metrics and interpreting results for healthcare insights.
- Documenting findings in a Jupyter Notebook with reflections on challenges and improvements.


## Project Objectives

- **Explore Data:** Load the dataset, inspect for missing values or anomalies, and visualize feature distributions.  
- **Prepare Data:** Clean missing values, encode categorical variables, scale numerical features, and engineer the binary target. 
- **Select Features:** Choose impactful predictors (e.g., age, chest pain type, max heart rate) based on domain knowledge and exploratory analysis.  
- **Train & Evaluate Models:** Implement Logistic Regression and Random Forest, measure accuracy, precision, recall, F1-score, and visualize confusion matrices.
- **Compare Approaches:** Benchmark models to identify the best performer and discuss interpretability vs. performance trade-offs.  
- **Reflect & Document:** Summarize insights, address challenges like class imbalance, and suggest HR-like interventions for patient risk management.  


## Key Findings

Summary table :

| Model               | Dataset | Accuracy | Precision | Recall | F1-Score |
|--------------------|---------|---------|-----------|--------|----------|
| Logistic Regression | Train   | 0.848   | 0.854     | 0.807  | 0.830    |
| Logistic Regression | Test    | 0.833   | 0.846     | 0.786  | 0.815    |
| Random Forest       | Train   | 1.000   | 1.000     | 1.000  | 1.000    |
| Random Forest       | Test    | 0.850   | 0.880     | 0.786  | 0.830    |


- **Top Drivers of Attrition:** Chest pain type (cp), maximum heart rate (thalach), ST depression (oldpeak), and exercise-induced angina (exang) are the strongest predictors, with older age, higher cholesterol, and elevated blood pressure also contributing significantly. 
- **Model Performance:** Random Forest slightly edged out Logistic Regression on test accuracy (85% vs. 83%) and F1-score (0.83 vs. 0.81), but Logistic Regression offers better interpretability for clinical use. Both models show low overfitting risk. 
- **Imbalanced Data Challenge:** Mild class imbalance (54% no disease vs. 46% disease) was managed via stratified splitting, but recall highlights potential misses in detecting diseased cases—critical for medical applications.
- **Actionable Insights for Healthcare:** Prioritize screening for patients with asymptomatic chest pain (cp=4), low max heart rate, or high ST depression to improve early detection and reduce false negatives.  
- **Interpretability:** Using a concise set of 13 clinical features ensures models are explainable to stakeholders, balancing accuracy with practical deployment.  

## Project links

First dataset

-  **Dataset:** [Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)
- **GitHub:** [github link](https://github.com/anjana-codes/ml_classification_anjana)
- **Classification Notebook:** [classification_anjana.ipynb](https://github.com/anjana-codes/ml_classification_anjana/blob/main/notebooks/classification_anjana.ipynb)   
- **Peer Review Notes:** [peer_review.md](https://github.com/anjana-codes/ml_classification_anjana/blob/main/notebooks/peer_review.md)   
- **Repository Overview:** [README.md](https://github.com/anjana-codes/ml_classification_anjana/blob/main/README.md)
  
Second dataset
   
 - **Dataset:** [Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
 - **GitHub:** [github link](https://github.com/anjana-codes/ml_classification_anjana)
 - **Classification Notebook:** [classification1_anjana.ipynb](https://github.com/anjana-codes/ml_classification_anjana/blob/main/notebooks/classification1_anjana.ipynb) 
 - **Repository Overview:** [README.md](https://github.com/anjana-codes/ml_classification_anjana/blob/main/docs/README.md)

## Set Up
## 1. Set Up Machine

Proper setup is critical.
Complete each step in the following guide and verify carefully.

- [SET UP MACHINE](./SET_UP_MACHINE.md)

---

## 2. Set Up Project

After verifying your machine is set up, set up a new Python project by copying this template.
Complete each step in the following guide.

- [SET UP PROJECT](./SET_UP_PROJECT.md)

It includes the critical commands to set up your local environment (and activate it):

```shell
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
```

**Windows (PowerShell):**

```shell
.\.venv\Scripts\activate
```

**macOS / Linux / WSL:**

```shell
source .venv/bin/activate
```

---

## 3. Daily Workflow

Please ensure that the prior steps have been verified before continuing.
When working on a project, we open just that project in VS Code.

### 3.1 Git Pull from GitHub

Always start with `git pull` to check for any changes made to the GitHub repo.

```shell
git pull
```

### 3.2 Run Checks as You Work

This mirrors real work where we typically:

1. Update dependencies (for security and compatibility).
2. Clean unused cached packages to free space.
3. Use `git add .` to stage all changes.
4. Run ruff and fix minor issues.
5. Update pre-commit periodically.
6. Run pre-commit quality checks on all code files (**twice if needed**, the first pass may fix things).
7. Run tests.

In VS Code, open your repository, then open a terminal (Terminal / New Terminal) and run the following commands one at a time to check the code.

```shell
git pull
uv sync --extra dev --extra docs --upgrade
uv cache clean
git add .
uvx ruff check --fix
uvx pre-commit autoupdate
uv run pre-commit run --all-files
git add .
uv run pytest
```

### 3.5 Git add-commit-push to GitHub

Anytime we make working changes to code is a good time to git add-commit-push to GitHub.

1. Stage your changes with git add.
2. Commit your changes with a useful message in quotes.
3. Push your work to GitHub.

```shell
git add .
git commit -m "describe your change in quotes"
git push -u origin main
```

This will trigger the GitHub Actions workflow and publish your documentation via GitHub Pages.

### 3.6 Modify and Debug

With a working version safe in GitHub, start making changes to the code.

Before starting a new session, remember to do a `git pull` and keep your tools updated.

Each time forward progress is made, remember to git add-commit-push.
 

