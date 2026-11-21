# PwC Tax Virtual Experience (Forage) — Task 1: Trial Balance & Chart of Accounts Mapping

## 📌 Project Overview
**Client:** ABC Inc. (Fitness & Retail Company offering monthly gym memberships, personal training, and gym apparel/accessories)  
**Role:** Tax Associate (Data & Tax Analytics Perspective)  
**Objective:** Standardize ABC Inc.’s unmapped Trial Balance into PwC’s structured **Chart of Accounts (CoA)** by assigning standardized 4-digit account codes, classifying each line item into core accounting elements, and mapping each account to its appropriate financial statement (**Balance Sheet** vs. **Income Statement**) prior to Senior Associate review and downstream tax analysis.

---

## 🎯 Business & Data Analytics Context
When onboarding a new tax client, raw general ledger / trial balance extracts often arrive with inconsistent naming conventions and no standardized hierarchy. Before performing tax adjustments (such as Book-to-Tax reconciliations) or building automated financial models, the data must be normalized:

1. **Standardized 4-Digit Account Schema:** Enables deterministic grouping, SQL/BI roll-ups, and automated ingestion into tax compliance software.
2. **Account Type Classification:** Separates permanent standing balances from periodic operating activity.
3. **Financial Statement Assignment:** Routes permanent accounts to the **Balance Sheet** and temporary period accounts to the **Income Statement**.

---

## 🗂️ Chart of Accounts (CoA) Architecture

| Account Prefix | Account Category | Financial Statement | Accounting Definition |
| :--- | :--- | :--- | :--- |
| **`1000 – 1999`** | **Asset** | Balance Sheet | Economic resources owned or controlled by the business (including contra-asset valuation accounts). |
| **`2000 – 2999`** | **Liability** | Balance Sheet | Present financial or service obligations owed to external parties or employees. |
| **`3000 – 3999`** | **Equity** | Balance Sheet | Residual ownership interest in the business ($\text{Equity} = \text{Assets} - \text{Liabilities}$). |
| **`4000 – 4999`** | **Revenue** | Income Statement | Income generated from core operations and investment returns during the reporting period. |
| **`5000 – 5999`** | **Expense** | Income Statement | Direct and operating costs incurred to generate revenue during the reporting period. |

---

## ✅ Final Standardized Chart of Accounts Mapping (41 Accounts)

| Account # | Account Description | Account Type | Financial Statement |
| :---: | :--- | :--- | :--- |
| 1001 | Cash | Asset | Balance Sheet |
| 1002 | Accounts Receivable | Asset | Balance Sheet |
| 1003 | Allowance For Doubtful Accounts | Asset *(Contra-Asset)* | Balance Sheet |
| 1004 | Inventory | Asset | Balance Sheet |
| 1005 | Fixed Assets | Asset | Balance Sheet |
| 1006 | Prepaid Rent | Asset | Balance Sheet |
| 1007 | Prepaid Insurance | Asset | Balance Sheet |
| 1008 | Machinery And Equipment - Gym Appliances | Asset | Balance Sheet |
| 1009 | Computer Equipment | Asset | Balance Sheet |
| 1010 | Accumulated Depreciation | Asset *(Contra-Asset)* | Balance Sheet |
| 2001 | Accounts Payable | Liability | Balance Sheet |
| 2002 | Accrued Bonus | Liability | Balance Sheet |
| 2003 | Accrued Commissions | Liability | Balance Sheet |
| 2004 | Taxes Payable | Liability | Balance Sheet |
| 2005 | Accrued Vacation | Liability | Balance Sheet |
| 2006 | Other Accruals | Liability | Balance Sheet |
| 2007 | Deferred Revenue | Liability | Balance Sheet |
| 3001 | Retained Earnings | Equity | Balance Sheet |
| 4001 | Sales Revenue | Revenue | Income Statement |
| 4002 | Service Revenue | Revenue | Income Statement |
| 4003 | Interest Revenue | Revenue | Income Statement |
| 4004 | Other Revenue | Revenue | Income Statement |
| 4005 | Municipal Bond Interest | Revenue | Income Statement |
| 5001 | Cost Of Goods Sold | Expense | Income Statement |
| 5002 | Bad Debt Expense | Expense | Income Statement |
| 5003 | Meals | Expense | Income Statement |
| 5004 | Entertainment | Expense | Income Statement |
| 5005 | Travel | Expense | Income Statement |
| 5006 | Rent Expense | Expense | Income Statement |
| 5007 | Salaries and Wages | Expense | Income Statement |
| 5008 | Commissions | Expense | Income Statement |
| 5009 | General and Administrative | Expense | Income Statement |
| 5010 | Vacation Expense | Expense | Income Statement |
| 5011 | Bonus | Expense | Income Statement |
| 5012 | Utilities & Electricity | Expense | Income Statement |
| 5013 | Depreciation Expense | Expense | Income Statement |
| 5014 | Donations | Expense | Income Statement |
| 5015 | Advertising Expense | Expense | Income Statement |
| 5016 | Office Supplies | Expense | Income Statement |
| 5017 | Memberships and Dues | Expense | Income Statement |
| 5018 | Taxes | Expense | Income Statement |

---

## 🔍 Key Accounting & Tax Takeaways
* **Accruals vs. Prepaids:** `Prepaid Rent` (`1006`) and `Prepaid Insurance` (`1007`) represent future economic benefits paid in advance (**Assets**), whereas `Deferred Revenue` (`2007`) and `Accrued` employee obligations (`2002`–`2006`) represent unfulfilled obligations (**Liabilities**).
* **Contra-Asset Accounts:** `Allowance For Doubtful Accounts` (`1003`) and `Accumulated Depreciation` (`1010`) act as valuation offsets paired with `Accounts Receivable` (`1002`) and `Fixed Assets` (`1005`) on the **Balance Sheet**.
* **Tax-Sensitive Account Granularity:** Separating accounts such as `Municipal Bond Interest` (`4005`), `Meals` (`5003`), `Entertainment` (`5004`), and `Donations` (`5014`) establishes the clean audit trail required for downstream **Book-to-Tax adjustments** (e.g., tax-exempt income and partial/non-deductible expenses).

---

## 🛠️ Skills Demonstrated
* Financial Data Normalization & Schema Mapping
* Trial Balance Classification (Balance Sheet vs. Income Statement)
* US Corporate Tax Readiness & Audit Trail Structuring
* Microsoft Excel Data Organization
