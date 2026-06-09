# Titanic Survival Prediction

## About
This project predicts whether a passenger survived the Titanic disaster, based on features like age, sex, ticket class and fare. 
It is based on the [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic/overview)
One of the most well-known beginner machine learning datasets. 

It was built as part of my studies in Applied Computer Science at Vives University of Applied Sciences. 

**Kaggle public score: 0.763**

## What I did
- Performed thorough Exploratory Data Analysis: identifying variable types, 
  missing values, outliers, correlations, and survival patterns across multiple features.
- Applied Feature Engineering, extracted passenger titles from names, 
  created a family-size feature, handled missing values using training 
  statistics to avoid data leakage.
- Trained and compared three classification models,  Logistic Regression, 
  Random Forest and Gradient Boosting, using Stratified K-Fold cross-validation 
  to account for class imbalance.
- Tuned hyperparameters using GridSearchCV
- Evaluated the final model using a classification report and a confusion matrix 
  and feature importance analysis.

  ## Results
| Model | CV Accuracy | Std Dev |
|---|---|---|
| Logistic Regression (baseline) | 81.9% | 0.006 |
| Random Forest | 82.2% | 0.014 |
| Gradient Boosting | **84.5%** | 0.008 |

**Final Model**: Gradient Boosting (learning rate 0.05, max depth 3, 200 estimators)

## Key Insight
The strongest predictors of survival were **Title**, **Fare** and **Pclass**,  
all reflecting the social hierarchy aboard the Titanic. Passengers with higher 
social status had significantly better access to lifeboats and higher survival rates.

## Files
- `Farah_Yakoubi.ipynb` — main notebook (blog style, full workflow)
- `train.csv` — training data
- `test.csv` — test data
- `submission_final.csv` — final Kaggle submission

## Sources
- Kaggle Titanic dataset: https://www.kaggle.com/competitions/titanic
- Pandas documentation: https://pandas.pydata.org/docs
- Scikit-learn documentation: https://scikit-learn.org/stable
- Hall, W. (1986). Social class and survival on the S.S. Titanic. 
  Social Science & Medicine, 22(6), 687-690.
  https://pubmed.ncbi.nlm.nih.gov/3520835/
- AI assistance: Claude (Anthropic) and ChatGPT used for guidance 
  on data cleaning, feature engineering, model building and evaluation
