# NCAA March Machine Learning Mania 2026

A machine learning project for the [Kaggle March Machine Learning Mania 2026](https://www.kaggle.com/competitions/march-machine-learning-mania-2026) competition, which challenges participants to predict the outcomes of the NCAA Men's and Women's Basketball Tournaments.

## Overview

This project builds and evaluates multiple predictive models for NCAA March Madness game outcomes, ultimately producing win-probability predictions for all possible tournament matchups.

## Models Explored

- **LightGBM** — gradient boosting with Elo ratings as features
- **XGBoost** — gradient boosting baseline and tuned variants
- **Random Forest** — ensemble tree baseline
- **Elo Rating System** — standalone Elo model and feature for ensemble methods

## Key Files

| File | Description |
|------|-------------|
| `final model 2025.ipynb` | Main pipeline: feature engineering, model training, and final prediction generation |
| `EDA.ipynb` | Exploratory data analysis of historical NCAA game data |
| `elo.ipynb` | Elo rating system implementation |
| `final submission.ipynb` | Final submission notebook |
| `shaurya_final_6.csv` | Final prediction submission (win probabilities for all possible matchups) |

## Approach

1. **Feature Engineering** — historical win rates, Elo ratings, season stats, and seed differentials for both men's and women's tournaments
2. **Model Training** — trained on 2013–2024 tournament data
3. **Ensemble** — combined LightGBM + Elo for the final submission
4. **Evaluation** — optimized for Brier score (log loss on win probabilities)

## Results

Final predictions are in `shaurya_final_6.csv`, covering all possible game matchups for both the men's and women's 2026 NCAA tournaments.

## Requirements

```
lightgbm
xgboost
scikit-learn
pandas
numpy
matplotlib
seaborn
jupyter
```

## Usage

Open `final model.ipynb` in Jupyter and run all cells. Kaggle competition data should be placed in the working directory.
