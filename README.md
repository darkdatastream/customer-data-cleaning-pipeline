# Customer CRM Data — Rule-Based Cleaning with Polars

> **Messy customer records cleaned with explicit validation rules, not guesswork.**

---

## The Problem

Customer and CRM datasets often look usable until invalid values, unrealistic outliers, and inconsistent categories start breaking analysis.

This project shows how to clean messy customer data using clear, rule-based validation so the final dataset is safe to use for reporting, segmentation, and downstream analysis.

---

## What Was Wrong in the Data

The raw dataset contained several issues that would reduce trust in any analysis built on top of it:

- impossible birth years
- unrealistic income values
- invalid category values
- ambiguous categories that should be reviewed manually instead of silently altered

Without cleaning these issues first, even a small customer dataset can produce misleading conclusions.

---

## Cleaning Rules

The cleaning logic was intentionally explicit and easy to audit:

- **Birth year < 1900** → removed
- **Income > 200000** → removed
- **Marital status = "YOLO" or "Absurd"** → removed
- **Marital status = "Alone"** → kept for manual review

This is the core principle behind reliable data cleaning:
**clear rules, clear outcomes, no silent guessing.**

---

## Results

| Metric | Value | Why It Matters |
|---|---:|---|
| Original rows | **2240** | Raw input dataset |
| Removed rows | **7** | Clearly invalid records excluded |
| Final rows | **2233** | Cleaned dataset ready for use |
| Review cases | Preserved separately | Ambiguous records not silently overwritten |

---

## Why This Project Matters

This project is small in scale, but it demonstrates an important part of real-world data work:

**good cleaning is not about “fixing everything.”**  
It is about separating clearly invalid records from cases that require review, applying consistent rules, and leaving an audit trail behind.

That approach scales much better than ad-hoc edits.

---

## Tech Stack

- **Python**
- **Polars**
- **Jupyter Notebook**

---

## Repository Contents

- rule-based cleaning notebook
- cleaned output dataset
- validation logic for customer and CRM-style records

---

## Related Project

My main large-scale data quality project:  
**NYC Yellow Taxi — Data Quality Audit at Scale**  
https://github.com/darkdatastream/nyc-yellow-taxi-cleanup

---

## Work With Me

📧 **data.audit.contact@proton.me**

I help clean, validate, and audit messy datasets before they reach dashboards, reports, or decision-making.

---

## License

MIT
