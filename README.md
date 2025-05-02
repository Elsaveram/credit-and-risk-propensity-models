# Credit Risk & Product Propensity Modeling

This repository provides a reproducible demonstration of two client-level predictive models, complete with workflows, model artifacts and a slide deck:

- **Credit Risk Model**  
  Flags clients unlikely to fulfill contractual conditions (minimize defaults).

- **Product Propensity Model**  
  Predicts which clients will choose Product 2 vs. Product 1 (maximize targeted sales).

Both models share a common data-preparation and feature-engineering pipeline—including:
- Missing-value imputation  
- Categorical encoding  
- Temporal & behavioral feature creation  
- Undersampling of the majority class  

Additional analyses:
- **Fairness Audit** using the 4/5-Rule Disparate Impact  
- **Temporal Drift Validation** proposal (out-of-time testing & PSI)

A PowerPoint deck (`modelos_riesgo_y_propension.pptx`) at the repository root walks through the business context, methods, key results and next steps.

---

## Repository Structure

- **notebooks/**  
  Contains `risk_propensity_audit.ipynb`, a self-contained workflow covering data prep, feature engineering, model training, fairness checks and drift-analysis approach.

- **Dockerfile & docker-compose.yml**  
  Define a container with all required dependencies so you can run the notebook in a reproducible environment.

- **modelos_riesgo_y_propension.pptx**  
  Slide deck summarizing the project narrative, results and recommendations.

- **README.md**  
  This file.

---

## Prerequisites

- Docker Desktop installed

---

## Project Execution

1. **Clone the repository**  
   ```bash
   git clone <repo-url>
   cd <repo>


2. Launch the Jupyter Notebook service:

    ```sh
    docker compose up jupyter
    ```

    Open the URL printed in your terminal (e.g. http://127.0.0.1:8888).

3. Run the analysis
In Jupyter, open notebooks/risk_propensity_audit.ipynb and execute the cells in order.
---

Note: Developed as part of a technical challenge. All code is provided “as is” for demonstration purposes.


