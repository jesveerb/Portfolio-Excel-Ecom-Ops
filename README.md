# E-Commerce Operations Data Standardization

## The Objective
To ingest, clean, and standardize a raw, error-filled e-commerce dataset to ensure accurate downstream revenue reporting.

## Execution
*   **Data Validation:** Handled missing categorical data (order statuses) without deleting rows, preserving total revenue metrics.
*   **Text Cleaning:** Utilized nested `PROPER` and `TRIM` functions to standardize customer name strings.
*   **Primary Key Generation:** Created sequential surrogate keys for missing Order IDs to maintain database integrity.
*   **Date Formatting:** Enforced a strict `DD-MMM-YYYY` schema to prevent regional parsing errors in future ETL pipelines.
