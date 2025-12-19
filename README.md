# Python Data Cleaning Portfolio

This project showcases an end-to-end data cleaning and preprocessing workflow in Python,
built using a fully synthetic marketing dataset.

The notebook simulates common real-world data quality issues and demonstrates how to
systematically clean, validate, and enrich raw data before analysis or modeling.

## Project Overview

The goal of this project is to illustrate practical data cleaning techniques that are
frequently required when working with real business datasets.

The workflow includes both data standardization and logical validation steps, going beyond
basic null handling.

## Key Steps Covered

- Synthetic data generation (no external data sources required)
- Column name standardization
- Currency and numeric type conversion
- Categorical value normalization
- Boolean value cleaning
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

