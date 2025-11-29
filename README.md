# Abalone Sex Classification (PyCaret)

This project uses machine learning to predict the **sex of an abalone** (Male, Female, or Infant) from its physical measurements.

---

## 1. Project Overview

- **Goal:** Predict the abalone's sex from its physical measurements.
- **Type of problem:** Multiclass classification (`M`, `F`, `I`).
- **Tools:** Python, Jupyter Notebook, PyCaret (classification), pandas, scikit-learn.

All of the code and experiments are in **`abalone_project.ipynb`**.

---

## 2. Dataset

- Based on the UCI Abalone dataset.
- Example input features (columns):
  - Length
  - Diameter
  - Height
  - Whole weight
  - Shucked weight
  - Viscera weight
  - Shell weight
  - Rings (optional, depending on the setup you used)

The target variable is **Sex** (`M`, `F`, or `I`).

---

## 3. Methods

1. Load and clean the Abalone dataset.
2. Use **PyCaret’s classification module** to:
   - set up the experiment,
   - compare multiple models,
   - choose the best-performing model.
3. Evaluate the final model on a test set.
4. Save the trained model for deployment.

---

## 4. How to Run the Notebook

```bash
# 1. Clone this repository
git clone https://github.com/z1abbasi/abalone-project.git
cd abalone-project

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook abalone_project.ipynb
