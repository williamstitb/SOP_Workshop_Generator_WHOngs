# S&OP Workshop Generator: "The Broken Chain"

## 1. Project Overview
This repository contains a Python-based simulation engine designed to generate data and visuals for a **Sales & Operations Planning (S&OP) Workshop**. 

**The Goal:** To simulate a realistic business conflict where a high-growth product is secretly destroying profitability and brand value. The data is engineered to force participants to move beyond "Revenue Growth" and make hard decisions based on "Profitability" and "Reliability."

**Target Audience:** Supply Chain Directors, Finance Managers, Sales Leads, and Operations Planners.

## 2. The Business Scenario
The simulation creates a 3-year history for a fictional personal care brand ("Halo") with two conflicting product lines:

| Product | Profile | The Problem |
| :--- | :--- | :--- |
| **Halo Core (Local)** | High Volume, Low Price, High Margin. | Boring. Sales ignores it. |
| **Halo Gold (Import)** | Low Volume, High Price, Low Margin. | The "Shiny Object." Sales loves the revenue growth, but it suffers from a **50% Stockout Rate** due to logistics failures. |

The script generates data that proves **Halo Gold** is an "Empty Calorie" product: it drives top-line revenue but erodes the bottom line and damages Net Promoter Scores (NPS).

## 3. Capabilities
Running the notebook generates a complete folder (`SOP_Workshop_Repo_Final`) containing:

### A. Master Data (For Student Analysis)
* `SOP_Master_Training_Data.csv`: 3 years of weekly transactions (Sales, Margin, Stock status).
* `SOP_Consumer_Feedback_Raw.csv`: Customer reviews and NPS scores.

### B. Workshop Exhibits (PNG Visuals)
* **Exhibit 1 (Revenue):** Shows strong growth for Halo Gold (The "Vanity Metric").
* **Exhibit 1B (Unit Economics):** Shows the P&L truth—Import costs kill Halo Gold's margin.
* **Exhibit 2 (Risk):** Shows a 50% failure rate for Halo Gold.
* **Exhibit 2B (Root Cause):** Proves the failure is external (Port Congestion), not internal.
* **Exhibit 4 & 4B (Brand):** Voice of Customer analysis showing logistics are driving customers away.
* **Exhibit 5A & 5B (The Promo Trap):** Shows that Promotions drive Revenue (5A) but crash Margins to 10% (5B).

### C. Facilitator Answer Keys (CSV)
* Aggregated data tables used to validate student findings.

## 4. Technical Stack
* **Python 3.13.9**
* **Pandas:** For data structuring and financial calculations.
* **NumPy:** For deterministic logic (forcing specific failure rates).
* **Seaborn / Matplotlib:** For generating the workshop slide deck.

## 5. How to Run
1.  Clone this repository.
2.  Ensure you have the required libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
3.  Open the Jupyter Notebook (`SOP_Workshop_Generator.ipynb`).
4.  Run all cells.
5.  Check the `SOP_Workshop_Repo_Final` folder for the output files.

## 6. Logic & "The Secret Sauce"
This simulation does not use random data. It uses **deterministic logic** to ensure the workshop outcome is consistent every time.

* **The 50% Failure Rule:** The script forces Halo Gold to stock out exactly every other shipment.
* **The Promo Trap:** When a promo flag is active, Volume multiplies by 4x, but Gross Margin is hard-coded to drop to 10%.
* **Signal vs. Noise:** The Consumer Feedback generator creates a specific Pareto distribution. 60% of complaints are about "Logistics" (Signal), while 40% are about "Product Quality" (Noise), teaching students to focus on structural issues.

## 7. Facilitator Guide
When presenting this data, guide the team through this narrative arc:
1.  **Sales:** "Look at the Revenue Growth in Exhibit 1!"
2.  **Ops:** "Look at the Stockouts in Exhibit 2. We can't ship it."
3.  **Finance:** "Look at Exhibit 5B. When we ship it, we lose money."
4.  **Marketing:** "Look at Exhibit 4B. When we don't ship it, customers hate us."
5.  **Decision:** Rationalize the SKU or fix the supply chain.

---
*Generated for S&OP Training Purposes.*
