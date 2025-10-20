# 🏠 House Price Prediction

End-to-end machine learning project predicting house prices using the **Ames Housing dataset**.  
This project demonstrates a complete ML workflow — from preprocessing to model comparison, evaluation, and saving the best pipeline.

---

## 📌 Features
- Data preprocessing pipeline:
  - Handling missing values
  - Encoding categorical features (OneHotEncoder)
  - Feature scaling
- Model training and comparison:
  - Baseline (mean predictor)
  - Linear Regression, Ridge, Lasso
  - Random Forest, Gradient Boosting, XGBoost
- Evaluation with **5-Fold Cross Validation** and **hold-out Test set**
- Metrics used:
  - **R²** (coefficient of determination)
  - **RMSE** (Root Mean Squared Error)
  - **MAE** (Mean Absolute Error)
- Best model automatically saved as a reusable pipeline (`house_price_model.pkl`)
- Visualization of evaluation metrics and residuals in `figures/`

---

## 📊 Results

✅ **Best Model: XGBoost**

### 📊 Model Performance Comparison

| Model             |   CV_R2 |   CV_RMSE |   CV_MAE |   Test_R2 |   Test_RMSE |   Test_MAE |
|:------------------|--------:|----------:|---------:|----------:|------------:|-----------:|
| XGBoost           | 0.891486 | 24760.9   | 14156.0  | 0.928628  | 23921.3     | 14004.5    |
| Random Forest     | 0.873383 | 27024.6   | 16272.2  | 0.910786  | 26744.7     | 16101.6    |
| Gradient Boosting | 0.882427 | 25532.1   | 15173.1  | 0.908366  | 27105.0     | 15442.6    |
| Ridge             | 0.198148 | 52021.9   | 35263.1  | 0.319869  | 48612.6     | 15591.9    |
| Lasso             | 0.1656   | 47209.5   | 15834.0  | 0.861038  | 33378.7     | 15131.5    |
| Linear Regression | 0.173885 | 47257.7   | 16056.2  | -0.865154 | 33966.1     | 15011.7    |
| Baseline (Mean)   | -0.0334087 | 78360.1 | 54256.5  | -0.0777266| 92955.5     | 63733.7    |

---

## 📂 Repository Structure
```
house-price-prediction-ml/
├── figures/ # Evaluation plots
│ ├── test_rmse.png
│ ├── test_r2.png
│ ├── test_mae.png
│ ├── actual_vs_pred.png
│ ├── residuals_hist.png
│ └── residuals_vs_pred.png
├── models/
│ └── house_price_model.pkl # Best trained model pipeline (XGBoost)
├── notebooks/
│ ├── house_price_prediction.ipynb # Model training & evaluation
│ └── predict_example.ipynb # Demo: load saved model & predict
├── data/
│ └── README.md # <-- Place dataset here (ignored by Git)
├── requirements.txt # Project dependencies
├── README.md # Project documentation
└── .gitignore

```
---

## 📥 Dataset
This project uses the **Ames Housing dataset**.  
Download it from [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques).  

After downloading, place the file `AmesHousing.csv` inside the `data/` folder:

data/AmesHousing.csv



⚠️ Note: The dataset itself is **not included in this repository** (to keep it lightweight).

---

## 🚀 How to Run

1. **Clone the repo**
   ```bash
   git clone https://github.com/Gazalapar/house-price-prediction-ml.git
Install dependencies

bash
Copy code
pip install -r requirements.txt
Add dataset

Download AmesHousing.csv (from Kaggle link above)

Place it into the data/ folder.

Run Jupyter notebooks

notebooks/house_price_prediction.ipynb → train & evaluate models

notebooks/predict_example.ipynb → use the saved model to make predictions


