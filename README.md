# H1N1_vaccine_prediction
Predicting H1N1 vaccination using people's information on their backgrounds, opinions, and health behaviors - Moringa School Phase 3 Project
# Project Overview
This project uses data science to predict the likelihood of individuals receiving the H1N1 and seasonal flu vaccines based on demographic, behavioral, and opinion-based features.

By identifying key factors influencing vaccine uptake, we aim to support public health outreach and reduce vaccine hesitancy.

# Business Goal
To develop a predictive model that accurately identifies people likely to receive the H1N1 and seasonal flu vaccines using:

Personal health behavior
Beliefs and risk perception
Socio-demographic characteristics

# Data Source

This project uses data from the [2009 H1N1 Flu Vaccine Prediction](https://www.drivendata.org/competitions/66/flu-shot-learning/data/) competition on DrivenData.

The dataset includes:
- `training_set_features.csv`
- `training_set_labels.csv`
- `test_set_features.csv`
- `submission_format.csv`

# Exploratory Data Analysis (EDA)
EDA focused on:

Vaccine uptake by age, sex, income, education Perceived risk and belief in effectiveness

# Key findings:

Higher uptake among older adults, females, and educated individuals

Belief in vaccine effectiveness strongly influenced uptake

Income and access barriers affected H1N1 vaccine behavior more than seasonal

## Modeling Approach

We used a multi-label classification setup to predict both `h1n1_vaccine` and `seasonal_vaccine` uptake using two models:

| Metric              | Logistic Regression | Random Forest       |
|---------------------|---------------------|---------------------|
| H1N1 Accuracy       | 84.5%               | 85.1%               |
| Seasonal Accuracy   | 78.2%               | 78.4%               |
| H1N1 AUC Score      | 0.8451              | 0.8576              |
| Seasonal AUC Score  | 0.8503              | 0.8528              |

**Observations**:
- Random Forest slightly outperformed Logistic Regression across most metrics, especially in H1N1 prediction.
- Both models struggled with class imbalance (fewer vaccinated individuals), leading to lower recall for class 1.
- Logistic Regression served as a strong baseline; Random Forest offered marginal improvements in both accuracy and AUC.
  
# Strategic Recommendations
1. Target Low-Income and Less-Educated Groups - Tailor communication and access efforts to underserved communities.
2. Build Trust in Vaccine Effectiveness - Emphasize evidence-based safety and benefits in campaigns.
3. Use Risk Perception as a Leverage Point - Highlight real consequences of flu to motivate vaccination.
4. Segment by Age and Sex - Younger adults and males are less likely to get vaccinated —focus messaging here.
5. Deploy Predictive Models - These models can help identify populations needing outreach, improving campaign efficiency.
