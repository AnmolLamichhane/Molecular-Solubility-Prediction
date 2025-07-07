# 📘 Molecular Solubility Prediction

This project focuses on building predictive models to estimate the **aqueous solubility (LogS)** of molecules using machine learning, based on molecular structure and computed chemical descriptors. Accurate solubility prediction is vital in pharmaceutical chemistry, as solubility influences drug absorption, bioavailability, and formulation.

---

## 🎯 Project Objective

The goal is to predict the **logarithm of solubility (LogS)** from molecular descriptors using regression models and compare their performance. The project assesses model accuracy, generalization, and predictive behavior using evaluation metrics and visual insights.

---

## 🧰 Tools & Technologies Used

- **Programming Language**: Python  
- **Libraries**:  
  - `pandas` – data handling  
  - `scikit-learn` – model training and evaluation  
  - `matplotlib`, `seaborn` – data visualization  
- **Environment**: Jupyter Notebook

---

## 🤖 Models Used

- **Linear Regression** – a baseline model assuming a linear relationship between descriptors and solubility  
- **Random Forest Regressor** – an ensemble learning method capable of modeling complex, non-linear relationships  

---

## 📊 Model Evaluation Summary

| Model                | Training MSE | Training R² | Test MSE | Test R² |
|----------------------|--------------|-------------|----------|---------|
| **Linear Regression** | 1.007536     | 0.764505      | 1.020695   | 0.789162  |
| **Random Forest**     | 0.124508     | 0.970898      | 0.652047   | 0.865311  |

**Key Insight:**
- The **Random Forest Regressor** significantly outperforms Linear Regression on both training and testing data as depth is 10.
- Its lower MSE and higher R² suggest better predictive accuracy and generalization.
- Linear Regression performs decently, but fails to capture complex patterns in the data as effectively.

---

## 📈 Scatter Plot Analysis

Two scatter plots were generated for both models showing **actual vs. predicted solubility (LogS)**:

- In the **Random Forest** plot, predicted values align closely along the diagonal, indicating more accurate predictions.
- In the **Linear Regression** plot, data points are more **scattered**, especially at higher or lower LogS values, reflecting **higher prediction error**.

**Visual Insight:**  
> The scatter plot confirms that Random Forest predictions are tighter and more accurate across the entire range, while Linear Regression tends to underfit certain regions.

---

## 📚 Dataset Reference

This project uses a dataset originally published by **John S. Delaney** in his 2004 study:

> **Delaney, J. S.** (2004). *ESOL: Estimating aqueous solubility directly from molecular structure*. Journal of Chemical Information and Computer Sciences, 44(3), 1000–1005.  

The dataset includes molecular **SMILES strings**, experimental **LogS values**, and precomputed **descriptors**, making it ideal for solubility prediction tasks.

---

## 📌 Conclusion

This project demonstrates that:
- Random Forest is more effective than Linear Regression in predicting molecular solubility.
- Proper use of molecular descriptors and ensemble learning leads to highly accurate, generalizable models.
- Visual and metric-based evaluation together provide a clear understanding of model performance.

