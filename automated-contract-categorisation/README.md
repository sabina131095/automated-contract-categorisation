# Automated Contract Categorisation

This repository packages dissertation notebook into a reproducible project.

## What’s inside
- `notebooks/Automated_Contract_Categorisation.ipynb` — your original notebook.
- `src/contract_classifier/` — place modular Python code here (data loading, preprocessing, training, inference).
- `scripts/` — CLI entry points (e.g., `train.py`, `predict.py`). 
- `configs/` — YAML configs for experiments (e.g., model type, paths, hyperparameters).
- `tests/` — add unit tests (pytest).
- `data/` — local data only (gitignored). Use Git LFS *only if* you need to version large assets.
- `models/` — saved model artifacts (gitignored by default).
- `docs/` — project documentation.
- `.github/workflows/` — CI templates (optional to fill later).

## Quick start
```bash
# 1) Create & activate a virtual environment (example with venv)
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# 2) Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# 3) Launch Jupyter
python -m ipykernel install --user --name contract-cat
jupyter notebook  # or jupyter lab
```

## Converting notebook to scripts (optional)
You can factor stable code into modules:
```bash
jupyter nbconvert --to script notebooks/Automated_Contract_Categorisation.ipynb   --output src/contract_classifier/notebook_export.py
```
Then split functions into files like `data.py`, `preprocess.py`, `model.py`, `train.py`, `predict.py`.

## Recommended repo flow
- Keep data in `data/` out of git; commit small samples only.
- Track large models/artifacts via Git LFS (optional).
- Add unit tests as you stabilize modules.
- Use `configs/*.yaml` to record experiment settings.

## Pushing to GitHub (local)
```bash
git init
git add .
git commit -m "Initial commit: dissertation starter"
git branch -M main
git remote add origin https://github.com/USER/automated-contract-categorisation.git
git push -u origin main
```

## Pushing from Google Colab
In a Colab cell:
```python
!git config --global user.email "you@example.com"
!git config --global user.name "Your Name"
!git init
!git add .
!git commit -m "Initial commit"

# Replace TOKEN and USER/REPO below; keep the token secret!
!git remote add origin https://TOKEN@github.com/USER/automated-contract-categorisation.git
!git branch -M main
!git push -u origin main
```

> **Tip:** Use GitHub **Personal Access Token** (classic) with `repo` scope; never commit it to the repo.

## License
See `LICENSE`. Default is MIT; change if your institution requires something else.
