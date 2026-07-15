# E-Commerce Operations Data Standardization

## The Objective
To ingest, clean, and standardize a raw, error-filled e-commerce dataset to ensure accurate downstream revenue reporting.

## Execution
*   **Data Validation:** Handled missing categorical data (order statuses) without deleting rows, preserving total revenue metrics.
*   **Text Cleaning:** Utilized nested `PROPER` and `TRIM` functions to standardize customer name strings.
*   **Primary Key Generation:** Created sequential surrogate keys for missing Order IDs to maintain database integrity.
*   **Date Formatting:** Enforced a strict `DD-MMM-YYYY` schema to prevent regional parsing errors in future ETL pipelines.

*   
## Day 2: Relational Mapping & Logic Processing
* **Relational Mapping:** Replaced brittle `VLOOKUP` functions with `INDEX/MATCH` to dynamically map Unit Prices from a Product Master table to the daily transaction log.
* **Dynamic Logic:** Engineered nested `IF` statements to automatically apply tiered discount multipliers based on promotional codes.
* **Error Quarantining:** Wrapped revenue calculations in `IFERROR` functions to catch unmapped SKUs, outputting $0 to prevent `#VALUE!` errors from crashing downstream aggregations.

* ## Foundational Analytics: Arithmetic & Conditional Aggregation
* **Descriptive Statistics:** Utilized `SUM`, `AVERAGE`, and `COUNT` to establish baseline metrics for employee headcount and total payroll liabilities.
* **Conditional Analysis:** Engineered `SUMIFS`, `AVERAGEIFS`, and `MAXIFS` formulas to dynamically extract region-specific and department-specific insights from a larger raw dataset.
