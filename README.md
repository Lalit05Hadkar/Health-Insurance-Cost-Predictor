# Health Insurance Cost Predictor

A machine learning project (from Codebasics ML Course) that predicts **health insurance premium** based on user inputs such as age, medical history, income, BMI, region, smoking status, and more.

This project includes a **Streamlit web app**, preprocessing pipeline, ML models, and helper functions.

---

## 🚀 Project Overview

This application predicts the expected **health insurance cost** using trained machine learning models. It uses two separate models:

* **model_young** → for users aged **≤ 25**
* **model_rest** → for users aged **> 25**

The app accepts structured user inputs from a web interface and returns a premium estimate.

---

## 📁 Project Structure

```
├── main.py                 # Streamlit UI application
├── prediction_helper.py    # Preprocessing + Model prediction logic
├── requirements.txt        # Project dependencies
├── artifacts/              # ML models + scalers
│   ├── model_young.joblib
│   ├── model_rest.joblib
│   ├── scaler_young.joblib
│   └── scaler_rest.joblib
├── README.md               # Documentation
└── .gitignore
```

---

## 🛠 Tech Stack

* **Python 3.x**
* **Streamlit** – Web interface
* **Pandas & NumPy** – Data manipulation
* **Scikit-learn** – ML models & scaling
* **XGBoost** – Advanced ML model
* **Joblib** – Model persistence

---

## 🔧 Installation & Setup

Follow these steps to run the project locally:

### 1️⃣ Clone the repository

```
git clone <repository-url>
cd <repository-folder>
```

### 2️⃣ Create a virtual environment (optional but recommended)

```
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate # Mac/Linux
```

### 3️⃣ Install dependencies

```
pip install -r requirements.txt
```

### 4️⃣ Ensure artifacts folder exists

Inside your project directory, create:

```
artifacts/
```

And place the following inside:

* model_young.joblib
* model_rest.joblib
* scaler_young.joblib
* scaler_rest.joblib

### 5️⃣ Run the Streamlit app

```
streamlit run main.py
```

App will launch in your browser:
👉 [http://localhost:8501](http://localhost:8501)

---

## ⚙️ How It Works

### 1️⃣ User enters data about:

* Age
* Income
* Dependants
* Medical history
* BMI category
* Region
* Smoking status
* Insurance plan, etc.

### 2️⃣ Data is preprocessed

* One-hot encoding of categorical values
* Medical risk score normalization
* Age-based model selection
* Scaling based on respective scaler

### 3️⃣ ML model predicts insurance cost

The prediction is displayed immediately on the UI.

---

## 📦 Key Functions

### `predict(input_dict)`

* Chooses appropriate ML model
* Applies preprocessing
* Returns final premium

### `preprocess_input(...)`

* Converts raw user inputs → model‑ready DataFrame

### `calculate_normalized_risk(...)`

* Converts medical history → numeric risk score

---

## 🧪 Example Usage

Once app is running, just fill out the form and click **Predict**.

---


