# Customer Data Cleaning (Polars)

## Problem

Customer/CRM data often contains errors:
- invalid values (e.g. impossible birth years)
- extreme outliers (e.g. unrealistic income)
- inconsistent categories (e.g. "YOLO", "Absurd")

Such data cannot be reliably used for analysis or business decisions.

---

## Solution

This project implements a data cleaning using **Polars**.

It:
- detects invalid records
- separates invalid vs review cases
- removes clearly incorrect data
- validates results at every step

---

## Cleaning Rules

- Birth year < 1900 → removed  
- Income > 200000 → removed  
- Marital status "YOLO" / "Absurd" → removed  
- "Alone" → kept for manual review  

---

## Results

- Original rows: 2240  
- Removed rows: 7  
- Final dataset: 2233  

The dataset is now consistent and ready for analysis.

---

## Output

`cleaned_customer_data.csv`

---

## Tech Stack

- Python  
- Polars  

---

## Use Case

Applicable to:
- CRM systems  
- marketing datasets  
- customer databases  

---

## Key Insight

Data cleaning is not about guessing values.

It is about:
- defining clear rules  
- validating results  
- ensuring data consistency  
