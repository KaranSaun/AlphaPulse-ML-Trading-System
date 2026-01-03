# AlphaPulse – Machine Learning Trading Project

## 📌 Project Overview

AlphaPulse is an **end-to-end Machine Learning project** that applies traditional ML techniques to **financial market data**.  
The goal of this project is to **predict meaningful future price movements** of a stock using historical data and compare multiple ML models.

This project focuses on:
- Correct ML pipeline design  
- Proper problem formulation  
- Model comparison and evaluation  
- Honest and realistic results  

---

## 🎯 Problem Statement

Predicting daily stock price direction is very noisy.  
Instead of predicting every small movement, this project **reframes the problem** to predict **meaningful future returns**.

### Target Definition
- **1 (Positive Class):** Future return > 0.5%  
- **0 (Negative Class):** Otherwise  

This helps reduce noise and makes the prediction task more practical and realistic.

---

## 🧠 Machine Learning Pipeline

The project follows a standard ML pipeline:

1. **Data Collection**  
   - Stock price data downloaded using `yfinance`

2. **Feature Engineering**  
   - Daily returns  
   - Future returns (shifted values)

3. **Target Creation**  
   - Binary classification based on future return threshold

4. **Train–Test Split**  
   - Time-based split (no shuffling to avoid data leakage)

5. **Feature Scaling**  
   - Applied where required (Logistic Regression, KNN, SVM)

6. **Model Training**  
   - Multiple classification models trained independently

7. **Hyperparameter Tuning**  
   - GridSearchCV used for Random Forest

8. **Model Evaluation & Comparison**  
   - Accuracy  
   - ROC-AUC  

9. **Final Model Selection**  
   - Based on generalization and consistency

---

## 🤖 Models Used

The following Machine Learning models were trained and evaluated:

1. Logistic Regression (Baseline Model)  
2. K-Nearest Neighbors (KNN)  
3. Decision Tree  
4. Random Forest (with hyperparameter tuning)  
5. Gradient Boosting  
6. Support Vector Machine (SVM)  

Each model was trained using the **same dataset and split** to ensure fair comparison.

---

## 📊 Evaluation Metrics

The models were evaluated using:

- **Accuracy**  
  - Measures overall correctness  

- **ROC-AUC**  
  - Measures how well the model separates classes  
  - More reliable for imbalanced financial data  

> In financial prediction problems, accuracy close to 50% is common due to market noise.  
> Small improvements over random performance are meaningful.

---

## 🏆 Final Conclusion

- Predicting stock movements is a **challenging and noisy problem**
- All models performed close to random, which is **expected and realistic**
- **Gradient Boosting and Random Forest** showed the most consistent performance
- The most important learning is that **problem formulation matters more than model complexity**

This project demonstrates **sound ML reasoning**, not unrealistic performance claims.

---

## 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- yfinance  
- Jupyter Notebook  

---

## 📂 Project Structure

