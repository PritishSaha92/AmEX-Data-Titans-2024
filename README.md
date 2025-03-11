# American Express Data Titans 2024 - T20 Match Prediction

This repository contains my solution for the American Express Campus Challenge 2024, where I ranked in the top 10 among over 1000 teams from premier institutions like IITs and IIMs. The goal was to predict T20 cricket match outcomes by building a high-accuracy predictive model.

## Project Overview

In this hackathon, I developed a machine learning solution to predict the outcomes of T20 cricket matches. The approach involved extensive feature engineering, careful data preprocessing, feature selection using statistical methods, and implementation of various boosting algorithms.

## Dataset

The dataset consisted of several components:
- Match-level scorecard data
- Batsman-level scorecard data
- Bowler-level scorecard data
- Training data with sample features
- Test data with sample features

The training dataset contained 948 data points with various cricket match statistics.

## Methodology

### 1. Data Preprocessing

- Handled missing values in the dataset
- Cleaned and structured the data for feature engineering
- Split the dataset into three parts: training, feature selection, and testing for unbiased model development

### 2. Feature Engineering

Engineered 14 novel features that captured various aspects of T20 cricket matches, including:
- Team performance metrics (win ratios, historical performance)
- Run-related features (team_runs_ratio_last10, team_count_50runs_last15)
- Wicket-related features (team_wickets_ratio_last10)
- Strike rate features (team_srrate_ratio_last10)
- Ground-specific performance metrics (ground_avg_runs_last15)
- Head-to-head performance statistics (team1_winp_team2_last15)
- Day/night match performance ratios

### 3. Feature Selection

Applied a two-pronged approach to feature selection:
- **Mutual Information Analysis**: Used to identify features with high predictive power for the target variable
- **Variance Inflation Factor (VIF)**: Applied to eliminate multicollinearity among features
- Selected the optimal feature subset that maximized prediction accuracy while minimizing redundancy

### 4. Model Development

Implemented and compared multiple boosting algorithms:

- **XGBoost**: Achieved the best performance with 64% predictive accuracy
- **CatBoost**: Strong performance with categorical features
- **Gradient Boosting Machine (GBM)**: Provided complementary predictions
- **LightGBM**: Efficient implementation with good accuracy

### 5. Hyperparameter Optimization

- **Bayesian Optimization**: Used to efficiently search through the hyperparameter space
- **Grid Search CV**: Employed for fine-tuning model parameters
- Cross-validation was used throughout to ensure model robustness

### 6. Ensemble Methods

Experimented with ensemble techniques to improve model performance:
- Voting classifiers combining predictions from multiple models
- Weighted averaging of model predictions
- Stacking ensemble approaches

## Results

- Achieved 64% predictive accuracy on the training dataset using XGBoost
- Feature importance analysis revealed that team_count_50runs_last15, team_runs_ratio_last10, and team_wickets_ratio_last10 were the most influential features
- The CatBoost model was used for the final submission due to its robust performance

## Future Improvements

Potential areas for improvement include:
- Incorporating more advanced temporal features
- Deep learning approaches for sequence modeling
- More sophisticated ensemble techniques
- Additional external data sources

## Tools and Technologies

- Python for data processing and model development
- Pandas and NumPy for data manipulation
- Scikit-learn for preprocessing and evaluation
- XGBoost, CatBoost, LightGBM for building predictive models
- Bayesian Optimization for hyperparameter tuning

This project demonstrates a robust approach to sports data analysis, leveraging advanced machine learning techniques and feature engineering to drive actionable insights in cricket match prediction.
