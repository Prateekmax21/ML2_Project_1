 Youth Drug Use Prediction – ML2 Project

## 📘 Project Overview
This project analyzes patterns of youth drug use using decision tree models on data from the **National Survey on Drug Use and Health (NSDUH) 2023**. We focused on youth under the age of 18, and our goal was to explore how different social and behavioral factors influence marijuana usage behavior.

We used **classification trees**, **random forests**, **bagging**, and **regression trees** to answer three questions:

- **Binary Classification** – Has the youth ever used marijuana?
- **Multi-Class Classification** – How frequently do they use marijuana in a month?
- **Regression** – How many days per year does the youth use marijuana?

## 🔍 Research Questions

| Problem Type | Target Variable | Description |
|--------------|-----------------|-------------|
| Binary Classification | `MRJFLAG` | Predict whether a youth has ever used marijuana |
| Multi-Class Classification | `MRJMDAYS` | Classify past-month marijuana use as Seldom / Sometimes / Frequent |
| Regression | `IRMJFY` | Predict number of days used marijuana in the past year |

## 📊 Methods Used
- Decision Trees (`tree` package)
- Bagging (`randomForest`, with high `mtry`)
- Random Forests (default + tuned `mtry`)
- Cross-validation for pruning (`cv.tree`)
- Data cleaning and transformation in `tidyverse`

## 🗂 Files in This Repo
| File | Description |
|------|-------------|
| `ML2-Proj.Rmd` | Final R Markdown file with all models and output |
| `ML2-Proj.html` | Rendered HTML version of the project for easy viewing |
| `Youth Drug Use Prediction Report.docx` | Final report with interpretations |
| `Youth Drug Use Prediction.pptx` | Final 14-slide presentation with diagrams and results |
| `README.md` | You're here! Describes the project |
| `youth_data.xlsx` | Preprocessed NSDUH data for youth under 18 |

## 💡 Key Insights
- **Peer perception and approval** are top predictors in all models.
- **Parental disapproval** is associated with lower usage frequency.
- **School attendance** (days skipped) is a strong signal of drug use behavior.

## 📈 Model Performance (Test Set)
| Model | Task | Test Error / MSE |
|-------|------|------------------|
| Decision Tree | Binary Classification | 87.79% Accuracy |
| Random Forest | Multi-Class Classification | 49.56% Error |
| Tuned RF (mtry=10) | Regression | MSE = 9480.99 |
