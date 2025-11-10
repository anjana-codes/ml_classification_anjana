# ml_classification_anjana
# Title: HR Employee Attrition Classification Analysis
**Author:** Anjana Dhakal  
**Date:** 11/05/2025 

**Dataset:** [Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
**GitHub:** [github link](https://github.com/anjana-codes/ml_classification_anjana)

## Overview: 

Organizations frequently need to predict employee behavior to support HR decision-making. For example, a company may want to identify employees at risk of leaving to implement targeted retention strategies. Machine learning classification models help automate these decisions by recognizing patterns in historical employee data.  

This project demonstrates your ability to apply classification modeling techniques to a real-world HR dataset. You will:

- Load and explore the IBM HR Analytics Employee Attrition dataset.  
- Analyze feature distributions, handle categorical variables, and engineer new features.  
- Select key features that most influence employee attrition.  
- Train and evaluate classification models (Random Forest and Logistic Regression).  
- Compare model performance and interpret the drivers of attrition.  
- Document the analysis and insights in a structured Jupyter Notebook.  
- Conduct a peer review of a classmate’s project.  


## Project Objectives

- **Explore Data:** Load the dataset, inspect for missing values or anomalies, and visualize feature distributions.  
- **Prepare Data:** Clean the data, encode categorical variables, normalize numerical features, and engineer relevant features (e.g., Tenure-to-Promotion Ratio).  
- **Select Features:** Identify the most impactful predictors of attrition using feature importance and domain knowledge.  
- **Train & Evaluate Models:** Build classification models (Random Forest, Logistic Regression), assess performance using accuracy, precision, recall, F1-score, and confusion matrices.  
- **Compare Approaches:** Benchmark different models to determine which best predicts attrition and interpret their results.  
- **Reflect & Document:** Summarize insights, discuss challenges, and provide actionable recommendations for HR interventions.  


## Key Findings

- **Top Drivers of Attrition:** Overtime, age, tenure-to-promotion ratio, monthly income, and job satisfaction are the most influential predictors of employee attrition.  
- **Model Performance:** Logistic Regression outperformed Random Forest on this dataset, achieving higher precision, recall, and F1-score for predicting the minority class (employees likely to leave).  
- **Imbalanced Data Challenge:** High class imbalance (84% retention) made it difficult to detect actual attrition cases, highlighting the importance of class balancing or sampling techniques.  
- **Actionable Insights for HR:** Focusing on employees with high overtime, low satisfaction, and delayed promotions can help HR target retention strategies effectively.  
- **Interpretability:** Using a limited set of high-impact features simplifies the model, making predictions easier to explain to stakeholders.  


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

## References

- Dataset: (https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

- Scikit-learn documentation: https://scikit-learn.org

- Seaborn visualization library: https://seaborn.pydata.org