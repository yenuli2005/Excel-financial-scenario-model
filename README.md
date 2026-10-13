# 📊 Advanced Financial Scenario & Amortization Model

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Finance](https://img.shields.io/badge/Domain-Corporate_Finance-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Project-Milestone_1-orange?style=for-the-badge)

A dynamic, single-sheet Excel financial model built as my **very first hands-on portfolio project**. This model integrates dynamic data lookups, multi-scenario sensitivity tables, and a complete 60-period loan amortization schedule.

---

## 📸 Dashboard Overview & Preview

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/e982c96d-a6de-475f-9b69-b6e74603aba9" />

---

## 🎯 Project Purpose & Objectives

As a first-year Finance undergraduate, this project served as my practical sandbox to translate theoretical corporate finance concepts into dynamic spreadsheet logic. Rather than relying on static tables, the objective was to design a flexible financial tool using native Excel functions and clean modeling architecture.

### Key Tools & Skills Tested:
* **Dynamic Lookups:** Querying corporate revenue records across multiple hypothetical entities (`Alpha Corp`, `Beta Inc`, `Gamma LLC`, `Delta Co`, `Omega Ltd`).
* **Financial Modeling Functions:** Calculating periodic debt servicing obligations using `PMT`.
* **Sensitivity & Scenario Analysis:** Evaluating monthly cash outflow variances across floating interest rate environments ($5.00\%$ to $9.00\%$).
* **Automated Schedule Design:** Constructing a 60-period schedule with self-balancing ending principals.

---

## 📂 Model Architecture & Structure

```
Advanced_Financial_Scenario_Model.xlsx
│
└── 📊 Sheet 1: Financial Dashboard
    ├── 🏢 1. Company Revenue Directory & Dynamic Lookup Matrix
    ├── 🔀 2. Multi-Scenario Parameter Engine (Scenarios X, Y, Z)
    ├── 📥 3. Core Loan Assumptions & Monthly Repayment Output
    ├── 📈 4. Interest Rate Sensitivity Matrix ($5.00\%$ - $9.00\%$)
    └── 🗓️ 5. 60-Period Amortization Schedule
```

---

## 🛠️ Excel Tools, Formulas & Mathematical Mechanics

### 1. Dynamic Debt Service (`PMT`)
The monthly payment is calculated using Excel's built-in financial logic based on principal ($P$), nominal monthly interest rate ($r$), and total compounding periods ($n$):

$$\text{Monthly Payment} = \text{PMT}\left(\frac{\text{Annual Rate}}{12},\, \text{Tenure (Years)} \times 12,\, -\text{Principal Amount}\right)$$

* **Base Model Parameters:**
  * **Loan Principal ($P$):** $\$10,000.00$
  * **Annual Interest Rate ($I$):** $7.00\%$
  * **Tenure ($N$):** 5 Years (60 Months)
  * **Calculated Monthly Obligation:** $\$198.01$

---

### 2. 60-Month Amortization Schedule Mechanics

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/006bfd7a-a065-41fd-b9e4-cad36a608da6" />

For every period $t$ (from Month $1$ to $60$), the table updates dynamically using absolute and relative cell referencing:

1. **Beginning Balance ($B_t$):** Equals the Ending Balance of the prior period ($E_{t-1}$).
2. **Interest Expense ($I_t$):** Calculated as:
   $$I_t = B_t \times \left(\frac{\text{Annual Interest Rate}}{12}\right)$$
3. **Principal Repayment ($P_t$):** Calculated as:
   $$P_t = \text{Monthly Payment} - I_t$$
4. **Ending Balance ($E_t$):** Calculated as:
   $$E_t = B_t - P_t$$
   *(Reconciles to exactly $\$0.00$ at period $60$)*

---

## 💡 Key Takeaways & Lessons Learned

1. **Absolute vs. Relative Cell Locking (`$`):** Mastered locking constant input values (e.g., `$C$4` for annual interest rate) while allowing timeline parameters to increment down the schedule.
2. **Dynamic Auditing & Error Handling:** Verified that total principal paid across 60 periods sums up precisely to the initial $\$10,000.00$ outlay.
3. **User-Centric Design:** Formatted output fields with proper currency indicators (`$`), percentage signs (`%`), and clear visual hierarchy to present financial data effectively.

---

## ⚙️ How to Run & Test the Model

1. **Download:** Clone or download `Advanced_Financial_Scenario_Model.xlsx` from this repository.
2. **Launch:** Open the file using Microsoft Excel 2016+, Office 365, or Google Sheets.
3. **Interact:**
   * Modify the base **Loan Amount**, **Annual Interest Rate**, or **Tenure** in the input section.
   * Observe how the **Sensitivity Analysis Table** and all 60 rows of the **Amortization Schedule** recalculate automatically in real time.

---

## 🔒 Confidentiality & Data Disclaimer

> **Note on Data Integrity:** This model utilizes purely hypothetical / dummy financial data generated specifically for demonstration, learning, and skill-testing purposes. It does not represent any real-world commercial entity or financial institution.

---

### 👩‍💻 Author
**Yenuli Withanage**  
*B.Sc. in Finance Undergraduate | University of Sri Jayewardenepura (USJ)*  
*AAT SL Level 3 Candidate*  

[LinkedIn Profile](https://www.linkedin.com/in/yenuli-withanage) • [GitHub Repository](https://github.com/)
