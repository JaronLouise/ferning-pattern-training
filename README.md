Simple Stage 1 Ferning Training (Jupyter Notebook)
==================================================

This folder is a **minimal, notebook-first** version of your Stage 1 binary classification pipeline.

What’s included
---------------
- `stage1_training.ipynb`: a self-contained notebook that:
  - Loads your existing `master_patch_index.csv` and `fold_splits.csv`
  - Uses a simple `.npy` data generator
  - Builds an EfficientNetB3-based model
  - Trains with cross-validation and saves metrics to `outputs/all_results.csv`
- `requirements.txt`: minimal dependencies needed to run the notebook.

Expected project layout
-----------------------
This repo assumes you keep the same data layout you already have:

- This folder: `simple_notebook_repo/`
- Data (reused from your original project):
  - `../local/data/master_patch_index.csv`
  - `../local/data/fold_splits.csv`
  - `../local/data/dataset/dataset/...` (the `.npy` files referenced in `master_patch_index.csv`)

As long as you keep that structure, the notebook will find the data automatically.

How to run the notebook
-----------------------
1. Create and activate a virtual environment (recommended).
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open `stage1_training.ipynb` and run the cells from top to bottom.

GitHub setup
------------
If you want this folder to be its own GitHub repository:

```bash
cd simple_notebook_repo
git init
git add .
git commit -m "Initial simple notebook training setup"
```

Then create a new empty repository on GitHub (e.g. `simple-stage1-notebook`) and add it as a remote:

```bash
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git branch -M main
git push -u origin main
```

You can now work primarily inside the notebook and push changes like any normal repo.

