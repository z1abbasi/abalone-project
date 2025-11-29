# Abalone Sex Classification (PyCaret)

This project builds a machine learning model to predict the **sex of an abalone** (Male, Female, or Infant) from its physical measurements. The work was done as a machine learning final project using Python, Jupyter Notebook, and PyCaret.

---

## Project Overview

- **Goal:** Predict the abalone’s sex from numeric features such as size and weight.
- **Type of problem:** Multiclass classification (`M`, `F`, `I`).
- **Main tools:** Python, Jupyter Notebook, PyCaret (classification), pandas, seaborn, matplotlib.

All code is contained in the main notebook  
**`abalone_project.ipynb`** (filename may appear slightly different in the repo).

---

## Dataset

- The data is taken from the classic **Abalone** dataset (UCI Machine Learning Repository).
- It is loaded using the `ucimlrepo` package.
- Input features include various physical measurements such as:
  - Length  
  - Diameter  
  - Height  
  - Whole weight  
  - Shucked weight  
  - Viscera weight  
  - Shell weight  
  - Rings  

The target variable is **Sex**, with three classes: `M`, `F`, and `I`.

---

## Methods

The notebook follows these main steps:

1. **Load and prepare data**
   - Load the Abalone dataset using `ucimlrepo`.
   - Combine features and target into a single pandas DataFrame.
   - Perform a simple check of class balance for the target `Sex`.

2. **Full-feature classification with PyCaret**
   - Initialize a PyCaret classification setup using all available numeric features and `Sex` as the target.
   - Use `compare_models()` to train and compare multiple algorithms.
   - Select a best-performing baseline model and inspect feature importance.

3. **Exploratory analysis**
   - Compute a correlation matrix for the numerical features (excluding `Sex`).
   - Visualize correlations using a heatmap to understand relationships between physical measurements.

4. **Reduced-feature experiment**
   - Create a smaller dataset using a selected subset of five “smart” features:
     - `Viscera_weight`, `Whole_weight`, `Shucked_weight`, `Height`, `Diameter`
   - Run a new PyCaret setup on this reduced dataset.
   - Use `compare_models()` again to find the best model using only these five features.

5. **Model evaluation and saving**
   - Evaluate the final 5-feature model using PyCaret’s evaluation tools.
   - Generate predictions on the hold-out set.
   - Save the trained pipeline with `save_model()` so it can be reloaded later for deployment.

---

## Files in this Repository

- `Machine Learning Final Project.ipynb` – main notebook with data loading, modeling, and evaluation.
- `requirements.txt` – list of Python dependencies needed to run the notebook.
- (Optional) `abalone_sex_model.pkl` – saved PyCaret model pipeline, if exported.

---

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/z1abbasi/abalone-project.git
cd abalone-project

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook "Machine Learning Final Project.ipynb"
