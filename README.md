# Group 10 - Insurance Renewal Prediction App

This project is a **Machine Learning-based Insurance Renewal Prediction Web App** built using **Streamlit**, **scikit-learn** and **Python**.  
The app predicts whether a customer will **renew** their insurance policy based on demographic, behavioral and payment history features.



## Features

- Predict customer renewal probability using a trained **Random Forest model**.
- Interactive **Streamlit** web interface for:
  - Manual data entry
  - Batch CSV upload
- Automatic model and preprocessor loading from **Google Drive**.
- Integrated data preprocessing and derived feature generation pipeline

---

## Tech Stack

| Component | Technology |
|------------|-------------|
| Programming | Python 3.10 / 3.12 |
| Web Framework | Streamlit |
| ML Library | scikit-learn |
| Model Type | Random Forest Classifier |
| Storage | Google Drive (for model & preprocessor) |
| Deployment | Streamlit Cloud |
| Repository | GitHub |

---

## Folder Structure
Group10-insurance_renewal_app/
│
├── group10_streamlitApp.py # Main Streamlit app file
├── pipeline_model.py # Model training & preprocessing pipeline
├── rf_model.pkl # Trained Random Forest model (in google drive)
├── preprocessor.pkl # Preprocessing pipeline (scaler, encoder)(in google drive)
├── requirements.txt # Python dependencies
├── README.md # Deployment documentation (this file)
└── data/ # Sample input datasets

Note: The model file rf_model.pkl was too large to be hosted on Streamlit Cloud.
Since its size (~200 MB) exceeded GitHub’s 100 MB file limit, the model could not be committed to the repository.
Therefore, gdown was used to download the model dynamically from Google Drive at runtime.
---

## Local Setup Instructions

### 1. Clone the Repository

git clone https://github.com/karthikraogg/Group10-insurance_renewal_app.git
cd Group10-insurance_renewal_app


### 2. Create a Virtual Environment

python -m venv venv
source venv/bin/activate       # For Mac/Linux
venv\Scripts\activate          # For Windows

### 3. Install Dependencies

pip install -r requirements.txt

### 4. Run Locally

streamlit run group10_streamlitApp.py

-----------------

## Deployment on Streamlit Cloud

### Step 1: Push code to GitHub
git add .
git commit -m "Added latest Streamlit app"
git pull --rebase origin main
git push origin main

### Step 2: Go to Streamlit Cloud
Visit https://share.streamlit.io
Log in using your GitHub account
Click “Create app”
Select repository: Group10-insurance_renewal_app
Branch: main
Main file path: group10_streamlitApp.py

### Step 3: Configure
Python version: 3.12
Add requirements.txt under Advanced Settings
Click Deploy

### Step 4: Access App
Once deployed successfully, you’ll get a public URL:
https://group10-insurancerenewalapp-group10.streamlit.app/