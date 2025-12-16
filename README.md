# Ml_project-premium-prediction
# Health Insurance Premium Price Prediction – Streamlit App

🔗 **Live App:** [https://ml-project-premium-price-prediction.streamlit.app/](https://ml-project-premium-price-prediction.streamlit.app/)

## 📌 Overview

This project is an **end-to-end Machine Learning application** that predicts **health insurance premium prices** based on user demographics, lifestyle choices, employment details, and medical history.

The application uses **separate ML models for young and adult applicants** to better capture age-specific risk patterns and delivers real-time predictions through a **Streamlit web interface**.

---

## 🚀 Features

* Interactive Streamlit UI
* Premium prediction in real time
* Separate models for:

  * **Young applicants (Age ≤ 25)**
  * **Adult applicants (Age > 25)**
* Automatic feature engineering and scaling
* Medical risk normalization

---

## 🧠 Model Architecture

* **Algorithms:** Regression models (age-segmented)
* **Scaling:** Pre-fitted scalers per age group
* **Artifacts:** Stored using `joblib`

### Why two models?

Health insurance risk behaves very differently for young vs older individuals. Splitting models improves prediction accuracy and realism.

---

## 🗂️ Project Structure

```
├── main.py                     # Streamlit application
├── prediction_helper.py        # Preprocessing & prediction logic
├── artifacts/
│   ├── model_young.joblib      # Model for age ≤ 25
│   ├── model_rest.joblib       # Model for age > 25
│   ├── scaler_young.joblib     # Scaler for young users
│   └── scaler_rest.joblib      # Scaler for adult users
├── requirements.txt
├── README.md
```

---

## 📥 Input Features

The model uses the following inputs:

* Age
* Number of Dependants
* Income (in Lakhs)
* Genetical Risk Score
* Insurance Plan (Bronze / Silver / Gold)
* Employment Status
* Gender
* Marital Status
* BMI Category
* Smoking Status
* Region
* Medical History

---

## ⚕️ Medical Risk Normalization

Medical history is converted into a **normalized medical risk score** based on conditions such as:

* Diabetes
* Heart Disease
* High Blood Pressure
* Thyroid
* Combination of multiple conditions

This score is scaled between **0 and 1** and used as a numerical risk feature.

---

## 🛠️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/insurance-premium-prediction.git
cd insurance-premium-prediction
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Streamlit app

```bash
streamlit run main.py
```

---

## 📦 Tech Stack

* Python
* Streamlit
* Scikit-learn
* Pandas
* NumPy
* Joblib

---

## 🌐 Deployment

The application is deployed on **Streamlit Cloud**:
👉 [https://ml-project-premium-price-prediction.streamlit.app/](https://ml-project-premium-price-prediction.streamlit.app/)

---

## ⚠️ Disclaimer

This project is intended for **educational and portfolio purposes only**. It should not be used for real-world insurance pricing or underwriting decisions.

---

## 🙌 Acknowledgements

Inspired by real-world insurance analytics and ML deployment practices.

---

## 📬 Contact

For improvements such as model explainability (SHAP), API deployment, or advanced ensembles, feel free to reach out.
