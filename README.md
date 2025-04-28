# ICS435 Final Project
ICS435 Machine Learning Project - Kaggle Predict Podcast Listening TImes

By: Christian Dela Cruz, Kyler Okuma, Sean Flynn

# Podcast Listening Time Prediction

## Overview

This project aims to predict the total listening time (in minutes) for podcast episodes based on structured metadata features such as episode length, sentiment, guest popularity, and publication day.  
The project is based on the Kaggle Playground Series S5E4 competition: [Playground Series - Season 5 Episode 4](https://www.kaggle.com/competitions/playground-series-s5e4/overview).

We built models using Linear Regression, Ridge Regression, Lasso Regression, Multi-Layer Perceptrons (MLPs), LightGBM, XGBoost, CatBoost, and several ensemble strategies to maximize predictive performance.

## Dataset

- Training set: ~30,000 podcast episodes with listening time labels (`train.csv`).
- Test set: ~10,000 episodes without labels (`test.csv`).
- Features included both categorical metadata (e.g., Publication Day, Episode Sentiment) and numerical metadata (e.g., Episode Length, Guest Popularity).
- Additional feature engineering was performed to create interaction terms and derived features.

**Important:**  
The data files (`train.csv`, `test.csv`, and `final_results_cleaned.csv`) must be located in the **same folder** as the `435_final_project.ipynb` notebook, or you must adjust the file paths inside the notebook accordingly.  
This ensures that data loading works without additional path modification.

## Requirements

All required Python libraries are listed in `requirements.txt`.

To install dependencies, run:

```bash
pip install -r requirements.txt
```

Python 3.10 or higher is recommended for full compatibility.

## Installation and Running

Clone the repository:

```bash
git clone https://github.com/your-username/podcast-listening-time.git
cd podcast-listening-time
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Open and run the final notebook:

```bash
jupyter notebook 435_final_project.ipynb
```

Follow the notebook cells sequentially to preprocess data, train models, optimize hyperparameters, and evaluate results.

## Results

The best-performing model was a Tree-Based Ensemble, averaging LightGBM, XGBoost, and CatBoost predictions, achieving:

- **Validation RMSE:** 12.696 minutes
- **Validation MAE:** 9.248 minutes
- **Validation R² Score:** 0.7809

Ensemble methods significantly outperformed single models by reducing both bias and variance.

## Project Structure

```
435_final_project.ipynb   # Main notebook for preprocessing, modeling, and evaluation
requirements.txt          # Python dependencies
README.md                 # Project overview and instructions
/data                     # Folder containing training, test, and results CSVs
/visuals                  # Folder containing result plots and evaluation figures
/slides                   # (Optional) Presentation slides for project defense
```

## Acknowledgements

- Kaggle for hosting the original competition dataset.
- Libraries used: Scikit-Learn, LightGBM, XGBoost, CatBoost, PyTorch, Optuna, and Scikit-Optimize.

---
