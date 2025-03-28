# ❤️ Predicting Extramarital Affairs Using TidyModels in R

This project uses logistic regression and k-nearest neighbours (k-NN) classification to predict whether an individual is likely to engage in an extramarital affair, using data from a 1969 Psychology Today survey.

---

## 📁 Dataset: `affairs.csv`

Contains personal data of 601 individuals including:
- Age, gender, years married (ym)
- Marital rating, religious score, education, occupation
- Child status
- Affair status (yes/no)

Source: R. C. Fair, 1978, *Journal of Political Economy*

---

## 🧪 Objective

Build predictive models for the binary target `affair`:
- Exploratory analysis
- Preprocessing (dummy encoding, normalization, downsampling)
- Classification with:
  - Logistic Regression (baseline)
  - k-NN (tuned with 5-fold cross-validation)

---

## 🛠 Tools & Packages
- `tidymodels`, `themis`, `recipes`, `yardstick`, `kknn`, `ggplot2`
- Cross-validation, ROC analysis, hyperparameter tuning

---

## 🔍 Key Results

| Model                | Accuracy | Sensitivity | Specificity | AUC   |
|---------------------|----------|-------------|-------------|-------|
| Logistic Regression | ~0.65    | **0.686**   | 0.515       | 0.673 |
| k-NN (k = 37)        | ~0.66    | 0.686       | **0.667**   | 0.672 |

- Logistic model selected as final model based on higher AUC and interpretability.
- ROC plots confirm better generalization of logistic regression.

---

## 📈 Visuals
- Proportion of affair vs gender and child
- ROC curves for model comparison
- Confusion matrices for test set performance

---

## 📌 Skills Demonstrated
- Data wrangling and exploratory analysis
- Preprocessing pipelines with `recipes`
- Handling class imbalance with `step_downsample`
- Binary classification and model tuning
- Evaluation with AUC, sensitivity/specificity, confusion matrix
- Reporting results in a clear, client-focused format

---

## 📄 Report
- See `Assignment5_data_taming_a1899824_.pdf` for full analysis.

---

## 🧠 Future Work
- Try ensemble models like Random Forest or Gradient Boosting
- Add SHAP values for model explainability
