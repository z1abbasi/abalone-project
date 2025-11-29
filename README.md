# Abalone Sex Classification (PyCaret)

This project predicts the **sex of an abalone** (M, F, I) from its physical measurements using machine learning.

## Methods
- Load the UCI Abalone dataset with `ucimlrepo` and combine features + target into one DataFrame.
- Use PyCaret Classification (`setup`, `compare_models`) to train and select the best model.
- Repeat the experiment with a reduced set of 5 numeric features.
- Evaluate the final model (`evaluate_model`, `predict_model`) and save it with `save_model` for later use.

## Files
- `abalone_project.ipynb` – main notebook with all code and analysis.
- `requirements.txt` – Python dependencies.

## How to run
```bash
pip install -r requirements.txt
jupyter notebook abalone_project.ipynb
