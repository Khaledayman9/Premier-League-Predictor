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

# Usage
After setting up the environment, you can run the Jupyter Notebook provided to execute the analysis and view the results.


# Conclusion
This model provides insights into the predictive capabilities of regression techniques in sports analytics. By understanding team performance metrics, stakeholders can make informed decisions regarding team strategies, player acquisitions, and more.
