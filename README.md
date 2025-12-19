# Python Data Cleaning (Portfolio)

A concise, end-to-end **data cleaning workflow in Python (Jupyter Notebook)** using a **synthetic marketing campaigns dataset** generated inside the notebook.  
The notebook intentionally creates “messy” data (mixed types, inconsistent formats, logical issues) and then applies a practical cleaning pipeline to make it analysis-ready.

## What’s inside

### Dataset (synthetic)
The notebook generates a CSV (`marketing_campaign_data_messy.csv`) with typical real-world issues, such as:
- **Inconsistent column headers** (spaces, capitalization)
- **Currency-formatted numbers** stored as strings (e.g., `$1,234.56`)
- **Categorical typos / inconsistent labels** (e.g., `Facebok`, `Insta_gram`, `Gogle`, `Tik_Tok`, `E-mail`)
- **Mixed boolean encodings** (`Yes`, `No`, `1`, `0`, etc.)
- **Mixed date formats** and parsing edge cases
- **Logical integrity problems** (e.g., `clicks > impressions`, `end_date < start_date`)
- **Outliers** in numeric fields (winsorization approach)
- **Feature extraction** from strings (e.g., extracting `season` from `campaign_name`)

### Cleaning pipeline (high level)
1. **Header normalization** (trim, lowercase, snake_case)
2. **Type conversion + currency cleaning** for `spend`
3. **Categorical standardization** via mapping for `channel`
4. **Boolean normalization** for `active`
5. **Date parsing** for `start_date` / `end_date`
6. **Logical integrity checks**  
   - Fix impossible values (`clicks > impressions`)
   - Fix time travel (`end_date < start_date`)
7. **Outlier handling** (cap extreme `spend` values using an IQR-based upper bound)
8. **String parsing / feature engineering**  
   - Extract `season` from `campaign_name` with regex

## How to run

### Option A — locally (recommended)
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Open:
- `notebooks/Data_Cleaning_with_Python.ipynb`

### Option B — view only (GitHub)
GitHub renders the notebook directly in the browser.  
A clean (no outputs) version is also included:
- `notebooks/Data_Cleaning_with_Python_clean.ipynb`

## Tech stack
- Python
- Jupyter Notebook
- pandas, numpy

## Notes for reviewers
- The dataset is **synthetic** and generated in the notebook for demonstration purposes.
- The pipeline mirrors common patterns used in real projects (type normalization, integrity rules, outlier treatment, feature extraction).

## Possible next steps
- Add `src/` with reusable functions (e.g., `clean_headers()`, `clean_currency()`, `validate_integrity()`)
- Add lightweight tests for integrity rules
- Add a small EDA notebook to show before/after distributions
