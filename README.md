# F1 Podium Predictor

Predicts which drivers will finish in the top 3 of F1 races using 70+ years 
of historical race data. Built with machine learning in Python — includes 
data analysis, visualizations, and 2025 season predictions.

## Overview

This project uses machine learning to predict Formula 1 podium finishes 
(top 3 results) based on historical race data. Two versions of the notebook 
are available — a demo version with sample data that runs instantly with no 
setup, and a full version powered by the real Kaggle F1 dataset with actual 
charts and model outputs rendered.

Feel Free to check it out in Google Colab 2. 
https://colab.research.google.com/github/shaalan171-netizen/F1-podium-predictor/blob/main/f1_podium_predictor.ipynb
## Versions

### Version 1 — Demo (No Setup Required)
**File:** `f1_podium_predictor.ipynb`

This version uses lightweight sample data and is designed to show the 
full project structure and methodology without requiring any downloads. 
It's ideal for quickly understanding the approach and code logic. All 
cells are structured and documented but outputs are not pre-rendered — 
you'll need to run it yourself to see results.

**Best for:** Reviewing code structure, understanding the ML pipeline, 
running quickly in any environment.

### Version 2 — Full Dataset (Real Outputs)
**File:** `f1_podium_predictor_full.ipynb`

This version was run against the complete Formula 1 World Championship 
dataset from Kaggle, covering every race from 1950 to 2023. All cells 
have been executed and outputs are fully rendered — including charts, 
model accuracy scores, confusion matrices, feature importance plots, 
and 2025 season predictions. No setup required to view results, just 
open the notebook on GitHub.

**Dataset:** [Formula 1 World Championship (1950-2023) on Kaggle](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)  
**Best for:** Viewing real results, charts, and predictions without running anything.

## Features

- Exploratory data analysis on 70+ years of F1 race history
- Visual breakdown of podium finishes by driver, constructor, and grid position
- Feature engineering including rolling driver and constructor form metrics
- Side by side comparison of Logistic Regression vs Random Forest models
- Confusion matrix and feature importance visualizations
- 2025 season podium probability predictions for the current driver lineup

## Models Used

| Model | Description |
|-------|-------------|
| Logistic Regression | Baseline classifier, good interpretability |
| Random Forest | Ensemble of decision trees, higher accuracy |

## Key Findings

- Starting grid position is the single strongest predictor of a podium finish
- A driver's recent form (rolling podium rate over last 10 races) is highly predictive
- Constructor quality accounts for nearly as much variance as driver skill
- Random Forest outperformed Logistic Regression on this dataset

## Tech Stack
- Python 3
- pandas — data manipulation
- scikit-learn — ML models
- matplotlib / seaborn — visualizations
- Jupyter / Google Colab — notebook environment

## Running Locally

### Prerequisites
- Python 3.8+
- Jupyter Notebook or Google Colab

### Setup
```bash
git clone https://github.com/YOUR_USERNAME/f1-podium-predictor.git
cd f1-podium-predictor
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
```

### For the Full Dataset Version
1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)
2. Extract the zip and place the CSV files in the project root
3. Open `f1_podium_predictor_full.ipynb` and run all cells

## Running in Google Colab (No Install)
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Open Notebook → GitHub**
3. Paste this repo URL
4. Select your preferred notebook version
5. For the full dataset version, upload the Kaggle CSVs using the Files panel on the left

## Roadmap
- [ ] Add weather data as a feature
- [ ] Include circuit-specific historical performance per driver
- [ ] Try XGBoost and Neural Network models
- [ ] Build a live prediction dashboard with FastAPI + React
- [ ] Add 2025 race-by-race predictions as the season progresses

## License
MIT
