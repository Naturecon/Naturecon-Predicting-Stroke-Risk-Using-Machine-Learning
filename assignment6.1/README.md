# Assignment 6.1 — Results And Conclusion: Stroke Risk Prediction

This folder contains all materials for Assignment 6.1, including model evaluation results, conclusions, 
interpretation, performance analysis, and clinical implications.

Folder Structure

assignment6.1/
│
├── code/              # Python scripts for evaluation
├── notebook/          # Jupyter Notebook version of Assignment 6.1
├── figures/           # Learning curves, model performance graphs
├── report/            # Official Assignment 6.1 draft (PDF)
└── README.md          # (This file)

Assignment Overview

The purpose of Assignment 6.1 is to:

- Evaluate machine learning models on a real-world imbalanced test dataset  
- Compare Logistic Regression, Random Forest, and XGBoost  
- Interpret learning curves, overfitting, underfitting  
- Analyze feature importance  
- Provide conclusions regarding real-world applicability  

This assignment represents the final results and discussion phase of the project.

Summary of Results (Imbalanced Test Set)

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|------|-----------|-----------|--------|-----|---------|
| Logistic Regression | 0.75 | 0.14 | 0.80 | 0.24 | 0.786 |
| Random Forest | 0.91 | 0.17 | 0.22 | 0.19 | 0.791 |
| XGBoost | 0.61 | 0.10 | 0.86 | 0.18 | 0.730 |

 Interpretation

Logistic Regression achieved the *best recall*, identifying most stroke patients but with many false positives.
Random Forest had the *highest accuracy* but missed most stroke cases.
XGBoost achieved extremely high recall but very poor precision.

Because stroke is rare (≈4–5%), these trade-offs are expected.

 Key Conclusion

Machine learning can learn meaningful stroke-related patterns, but:

No model achieved a clinically acceptable precision–recall balance.  
False positives and false negatives remain too high for deployment.  

More data, cost-sensitive techniques, and additional clinical variables are needed.**

Files Included

- Assignment6.1 PDF report  
- code for evaluation  
- Optional Jupyter Notebook  
- Figure (loss curves, accuracy curves, confusion matrices)

 References

- Fedesoriano (2021). *Healthcare Stroke Prediction Dataset*.  
- WHO (2023). Stroke: Key Facts.  
- O’Donnell et al. (2016). Global impact of stroke risk factors.

Contributors

Team 09 — MSAAI 590 IN1  
- Balubhai Sukani  
- Paritosh Umesan  
