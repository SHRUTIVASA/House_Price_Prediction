# House Price Prediction Web App

A complete machine learning-powered **Flask web application** that predicts house prices based on user inputs such as area, BHK, location, etc. It uses advanced ensemble techniques including **Stacking** and **Voting Regressors**, and also provides a built-in **Loan Calculator** to help estimate monthly EMIs.

---

##  Features

-  Predicts house prices based on real estate input data
-  Trained using ensemble learning models (Voting & Stacking)
-  Loan calculator to estimate EMI based on user input
- Uses `.pkl` files for loading trained models and scalers
- Simple and responsive UI using HTML and CSS
- Integrated with Flask for smooth backend functionality

---

## Project Structure

```

housePricePrediction/
├── app.py                        # Flask backend
├── house\_price\_model.pkl         # Trained model for price prediction
├── scaler.pkl                    # Scaler used in preprocessing
├── m1.pkl                        # Another optional model
├── .gitattributes                # Git LFS tracking file
│
├── templates/                    # HTML templates
│   ├── main.html                 # House price prediction form
│   ├── loan\_calculator.html      # Loan calculator form
│   └── rew\.html                  # Optional results page
│
├── static/                       # CSS files
│   ├── style.css
│   ├── new\.css
│   └── style\_loan\_calculator.css
│
├── requirements.txt              # Python dependencies
└── README.md                     # You're here!

````

---

##  Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/simonisavani/housePricePrediction.git
cd housePricePrediction
````

### 2. Create and Activate Virtual Environment (Recommended)

```bash
python -m venv venv
# Activate it:
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is missing, install manually:

```bash
pip install flask scikit-learn pandas xgboost numpy
```

### 4. Run the App

```bash
python app.py
```

Then open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

---

## Machine Learning Models

The backend uses multiple regression models:

* Linear Regression
* Ridge Regression
* Decision Tree Regressor
* Random Forest Regressor
* XGBoost Regressor
* **Voting Regressor** (ensemble)
* **Stacking Regressor** (ensemble)

These were trained on a dataset of real estate listings and saved as `.pkl` files. Input data is scaled using `scaler.pkl` for consistency.

---

## Loan Calculator

Accessible via `/loan_calculator`, this page lets users:

* Input property price, interest rate, loan tenure
* Get estimated EMI using the standard formula:

```
EMI = [P x R x (1+R)^N] / [(1+R)^N - 1]
```

---

## Sample Inputs

* Area in sq. ft
* Number of bedrooms (BHK)
* Bathrooms
* Parking availability
* Location
* Furnishing type
* Transaction type (new/resale)

---

## Model Evaluation (Offline)

Trained models were evaluated using:

* R² Score
* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE)

**Voting Regressor** showed higher accuracy overall, but **Stacking Regressor** performed better in some scenarios.

---

## Background (Optional)

This project is based on an academic research study:

> **"Analyzing Stacking and Voting Regressors for House Price Prediction: A Comparative Approach"**
>  *Anvesak*, Vol. 53, Issue-03, July–Dec 2023
>  UGC Care-1 | Peer Reviewed | Impact Factor: 6.6

---

## UI Preview

>  Main Form (main.html)
>  Loan Calculator (loan\_calculator.html)
>  Styled with custom CSS under `static/`

