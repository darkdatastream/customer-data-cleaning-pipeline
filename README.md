# Customer Data Cleaning Pipeline (Polars)

Cleaning and validating messy customer CRM data using Polars. Removing invalid records, fixing categories, and preparing data for analysis.

## Problem

Real-world customer data is often messy and unreliable:
- invalid values (e.g. impossible birth years)
- extreme outliers (e.g. unrealistic income)
- inconsistent categorical values (e.g. "YOLO", "Absurd")
- data that cannot be used directly for analysis or marketing

This makes decision-making difficult and leads to incorrect results.

---

## Solution

This project demonstrates a structured data cleaning pipeline using **Polars**.

The pipeline:
- detects invalid and suspicious records
- separates invalid vs review-worthy data
- removes clearly incorrect records
- keeps potentially valid but ambiguous data for manual review
- validates every step to ensure correctness

---

## Cleaning Steps

### 1. Data validation
- checked schema and data types
- verified dataset structure

### 2. Quality checks
- detected invalid birth years (<1900)
- detected extreme income outliers (>200000)
- detected invalid categorical values ("YOLO", "Absurd")

### 3. Data classification
- invalid records → removed
- ambiguous records (e.g. "Alone") → kept for review

### 4. Safe filtering
- records removed using explicit ID list
- ensured deterministic and auditable cleaning

---

## Results

- removed **7 invalid records**
- eliminated impossible values
- cleaned categorical inconsistencies
- dataset is now ready for analysis or CRM usage

---

## Output

- cleaned dataset: `cleaned_leads.csv`

---

## Tech Stack

- Python
- Polars

---

## Key Insight

Data cleaning is not about guessing values.

It is about:
- identifying invalid data
- applying clear rules
- validating results at every step
- ensuring reproducibility

---

## Use Case

This pipeline can be applied to:
- CRM systems
- marketing datasets
- customer databases
- lead generation data

---

## Author

Data cleaning project focused on real-world business problems.
