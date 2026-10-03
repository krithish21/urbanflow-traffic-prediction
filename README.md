# Traffic Prediction Using Machine Learning

## Project Overview

This project focuses on predicting traffic volume using machine learning techniques. It includes traffic data, trained model files, and a Streamlit application for interacting with the traffic prediction system.

## Project Structure

```text
Traffic-Prediction-main/
├── app/
│   └── xgboost_model.pkl
├── traffic.csv
├── traffic_prediction_model.pkl
├── requirements.txt
├── traffic_app.py
├── .dvc/
├── .dvcignore
├── traffic.csv.dvc
├── traffic_prediction_model.pkl.dvc
└── app/
    └── xgboost_model.pkl.dvc
```

*Note: The `.dvc` files are metadata files used to track data and model files. Your actual data and model files should remain in place.*

## Technologies Used

* Python
* Machine Learning
* Streamlit
* Git
* DVC (Data Version Control)

## Setup

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd Traffic-Prediction-main
```

### 2. Create and activate a virtual environment

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```powershell
python -m pip install -r requirements.txt
```

### 4. Run the application

```powershell
streamlit run traffic_app.py
```

## Data and Model Versioning with DVC

DVC is used to track the dataset and trained model files, while Git tracks the source code and DVC metadata.

### Files tracked by DVC

| File                           | Purpose                  |
| ------------------------------ | ------------------------ |
| `traffic.csv`                  | Traffic dataset          |
| `traffic_prediction_model.pkl` | Trained prediction model |
| `app/xgboost_model.pkl`        | XGBoost model            |

### Initialize DVC

DVC has already been initialized in this project using:

```bash
git init
dvc init
```

### Track data and model files

The following commands were used:

```bash
dvc add traffic.csv
dvc add traffic_prediction_model.pkl
dvc add app/xgboost_model.pkl
```

These commands create `.dvc` metadata files and update `.gitignore` so that large data and model files are not directly added to Git.

### Save DVC metadata in Git

```bash
git add -A
git commit -m "Track traffic dataset and models with DVC"
```

## Important Notes

* Keep the original CSV and model files in their locations.
* Commit the generated `.dvc` files and `.gitignore` to Git.
* Do not manually edit the generated `.dvc` metadata files.
* DVC tracking is initialized locally. A shared DVC remote has not yet been configured.
* To share the actual dataset and model files with other team members, configure a DVC remote and run `dvc push`.

## Future Work

* Configure a shared DVC remote for team collaboration.
* Continue improving and evaluating traffic prediction models.
* Enhance the application interface and prediction visualizations.

## Author

**G. Krithish**
