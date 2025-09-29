## Databricks Git Repository Overview

This GitHub repository is linked to a Git folder in the Databricks workspace, enabling seamless version control, 
collaboration, and synchronization of fraud detection assets such as notebooks, SQL queries, and dashboards.

### Purpose

We deployed a tuned XGBoost model in Databricks and created an interactive dashboard to:

- Identify suspicious transactions, cards, and terminals.
- Monitor model performance metrics such as precision, recall, and prediction probabilities over time.
- Track high-level transaction activity across specified date ranges.

### Key Features

- The trained model uses hyperparameters from Python experiments, trained with PySpark and MLflow on synthetic credit card transaction data from the Fraud Detection Handbook in the references.
- Registered the model in the Databricks Model Registry.
- Prediction results are stored in a Delta table in Unity Catalog.
- SQL queries generate datasets for dashboard visualizations.
- Dashboard contains three main sheets:
    1. Most Suspicious Transactions, Cards, and Terminals
    2. Monitoring Model Performance
    3. Transaction Activity Over Time

### Repository Structure

- `.github/workflows/`  
  Contains GitHub Actions workflows for continuous integration and deployment.

- `app/`  
  The FastAPI application source code and supporting files.

- `Dockerfile`  
  Defines container build instructions.

- `requirements.txt`  
  Python package dependencies.

- `.gitignore`  
  Specifies ignored files for git.

### Usage

- This repo serves as the single source of truth for the development and maintenance of the fraud detection dashboard housed in Databricks.
- Dashboards, notebooks, and code sync automatically with the Databricks Git folder for traceability and CI/CD workflows.
- Changes pushed to this repo update the Databricks workspace and vice versa when committed through the Git folder.

For detailed deployment process, SQL queries, and dashboard design, please see the project documentation:  
https://dglassbrenner1.github.io/my-posts-on-fraud-detection/9-Databricks%20deployment.html


## Repository Organization

This repository, `db_fraud_detection`, contains the code and resources for the Databricks interactive dashboard for fraud detection.

The repository is organized as follows:

- `.github/workflows/`  
  Contains GitHub Actions workflows for CI/CD, including automated deployment of the FastAPI app.

- `app/`  
  The main application folder holding the FastAPI app source code and related files (e.g., `app.py`, API routes, Dockerfile).

- `Dockerfile`  
  Defines the Docker container image setup for deployment of the API service.

- `requirements.txt`  
  Lists the Python dependencies required for running the app.

- `.gitignore`  
  Standard git ignore file specifying files and folders to exclude from version control.

This structure supports easy development, testing, and deployment of the fraud detection API and related components.  
The repository is integrated with GitHub Actions for automated testing and deployment workflows.

You can find the latest commits and updates on this repository at:  
https://github.com/dglassbrenner1/db_fraud_detection

## References
Le Borgne, Y.-A., et al. (2022). *Reproducible Machine Learning for Credit Card Fraud Detection – Practical Handbook*. Université Libre de Bruxelles. GitHub Repo

## Contributions
Contributions, feedback, and discussions are welcome to improve the understanding and applications shared in this series.

## Contact
Donna Glassbrenner, Ph.D.
GitHub: dglassbrenner1
Website: https://dglassbrenner1.github.io/my-posts-on-fraud-detection/

