# Premier-League-Predictor
A predictive modeling project aimed at forecasting the ranks and points of football teams in the Premier League based on various performance metrics. The model employs two regression techniques: Linear Regression and Random Forest Regression, enabling a comparative analysis of their effectiveness in predicting team performance.

# Objectives
- Predict Team Ranks: Utilize historical statistics to accurately predict the ranks of football teams in the league.
- Forecast Points: Estimate the total points a team is likely to earn based on their performance metrics.
- Residual Analysis: Evaluate the accuracy of predictions through residuals, helping to identify teams that are over- or under-performing relative to expectations.

# Features
- Data Processing: Import and preprocess team statistics, including goals scored, goals conceded, wins, draws, losses, and goal difference.
- Model Training: Implement Linear Regression and Random Forest models to train on the dataset.
- Prediction and Evaluation: Generate predictions for ranks and points, and evaluate model performance using metrics like Mean Absolute Error (MAE) and R-squared values.
- Residual Analysis: Analyze residuals to identify the teams with the highest prediction errors, providing insights into model performance and potential areas for improvement.
- Visualization: Create plots to visualize actual vs. predicted ranks, as well as highlight teams with the highest residuals for both models.

# Dataset
- The dataset[^1] used in this project consists of team statistics from the 2024 Premier League season, including:
  - Team name
  - Goals scored
  - Goals conceded
  - Wins, draws, and losses
  - Points
  - Goal difference
  - Current rank

[^1]: [Premier League Season 2024](https://www.kaggle.com/datasets/abdelrahmanemad594/premier-league-season-2024)

# Installation
```bash
git clone https://github.com/Khaledayman9/Premier-League-Predictor.git
cd Premier-League-Predictor
pip install -r requirements.txt
```

# Results
## Linear Regression

**Rank Prediction:**
- **Mean Absolute Error (MAE):** 0.93
- **R² Score:** 0.94
- **Cross-Validated MAE:** 1.15

**Residuals for Rank:**
| Team                      | Rank Residuals |
|---------------------------|----------------|
| Manchester City           | 3.24           |
| West Bromwich Albion      | 1.46           |
| Nottingham Forest         | 0.91           |
| Leicester City            | -0.84          |
| Arsenal                   | 0.80           |
| Bournemouth               | -0.80          |
| Fulham                    | -0.74          |
| Brentford                 | -0.73          |
| Burnley                   | -0.71          |
| Brighton and Hove Albion  | 0.68           |



**Points Prediction:**
- **Mean Absolute Error (MAE):** 3.27e-14
- **R² Score:** 1.00
- **Cross-Validated MAE:** 9.52e-15

---

## Random Forest

**Rank Prediction:**
- **Mean Absolute Error (MAE):** 1.10
- **R² Score:** 0.96
- **Cross-Validated MAE:** 2.37

**Residuals for Rank:**
| Team                      | Rank Residuals |
|---------------------------|----------------|
| Manchester City           | -1.98          |
| Southampton               | -1.14          |
| Leeds United              | 1.09           |
| Everton                   | -1.05          |
| West Bromwich Albion      | 0.97           |
| Bournemouth               | -0.80          |





**Points Prediction:**
- **Mean Absolute Error (MAE):** 9.21
- **R² Score:** 0.91
- **Cross-Validated MAE:** 11.55

---

## Top 5 Team with Highest Residuals

![Residuals](https://github.com/user-attachments/assets/7cf33f55-c9f1-4fe4-8c7a-a240abba803a)

---

## Predictions

### Linear Regression Predictions:
| Team                      | Actual Rank | Predicted Rank (Linear) | Predicted Points (Linear) |
|---------------------------|-------------|--------------------------|----------------------------|
| Manchester City           | 1           | -2.24                    | 177                        |
| Liverpool                 | 2           | 1.96                     | 151                        |
| Arsenal                   | 3           | 2.20                     | 150                        |
| Manchester United         | 4           | 4.42                     | 134                        |
| Chelsea                   | 5           | 5.42                     | 130                        |

![Rank](https://github.com/user-attachments/assets/14ab5034-fbda-4b13-afd4-7ff293ef7da6)

![Points](https://github.com/user-attachments/assets/00330bb6-d0b0-4219-bed9-5ad198468abc)


### Random Forest Predictions:
| Team                      | Actual Rank | Predicted Rank (RF)     | Predicted Points (RF)     |
|---------------------------|-------------|--------------------------|----------------------------|
| Manchester City           | 1           | 2.98                     | 147                        |
| Liverpool                 | 2           | 2.65                     | 148                        |
| Arsenal                   | 3           | 3.40                     | 146                        |
| Manchester United         | 4           | 4.65                     | 131                        |
| Chelsea                   | 5           | 5.01                     | 129                        |

![Points 2](https://github.com/user-attachments/assets/c70e6580-b06b-41f4-beca-5715379befdb)

![Rank 2](https://github.com/user-attachments/assets/f334d885-0dd8-4b54-a9a3-56b52675c8ee)

---
The results indicate that both models perform well in predicting the ranks of the teams, with Linear Regression showing a slightly higher R² score for rank prediction, while Random Forest excels in points prediction. The residual analysis provides insights into the accuracy of each model's predictions for different teams, highlighting areas where the models may require improvement.

# Usage
After setting up the environment, you can run the Jupyter Notebook provided to execute the analysis and view the results.

# Conclusion
This model provides insights into the predictive capabilities of regression techniques in sports analytics. By understanding team performance metrics, stakeholders can make informed decisions regarding team strategies, player acquisitions, and more.


# Technologies
- Kaggle Notebook
- Python
- Scikit-learn
