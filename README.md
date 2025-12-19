# Python Data Cleaning Portfolio

This repository showcases an end-to-end data cleaning and preprocessing workflow in Python,
built using a fully synthetic marketing dataset.

The notebook intentionally introduces common real-world data quality issues and demonstrates
how to identify, clean, validate, and enrich raw data before downstream analysis or modeling.

## Project Highlights

- Synthetic dataset generation (fully reproducible, no external data required)
- Column name standardization and formatting
- Currency parsing and numeric type conversion
- Categorical value normalization and consistency mapping
- Boolean value standardization
- Robust date parsing with error handling
- Logical data integrity checks (e.g. clicks vs impressions, invalid date ranges)
- Outlier detection and capping using the IQR method
- Feature engineering using regular expressions

## Tech Stack

- Python
- pandas
- numpy
- Jupyter Notebook

## How to Run

```bash
pip install pandas numpy
jupyter notebook
