# PwC US Tax Virtual Experience (Forage) — End-to-End Portfolio

## 👋 Overview

**Client:** ABC Inc. (Fitness & Retail Company)  
**Role:** Tax Associate  
**Focus:** Financial Data Normalization, Book-to-Tax Reconciliations, Federal Taxable Income Computation, and Tax Process Automation  

This repository documents my end-to-end work across all four tasks of the **PwC US Tax Job Simulation** on Forage. Working from a data and finance analytics perspective, I took raw general ledger balances for ABC Inc. (`FY2025`) and transformed them into a reconciled corporate tax return computation—followed by an executive client summary and automation roadmap.

---

## 🗂️ Project Walkthrough (Tasks 1–4)

### 1. Trial Balance & Chart of Accounts Mapping (`Task 1`)
* **What I Did:** Standardized 41 raw trial balance accounts into PwC’s 4-digit Chart of Accounts (`1000`–`5999`), classifying each account into **Assets, Liabilities, Equity, Revenue, or Expenses** and mapping them to the **Balance Sheet** or **Income Statement**.
* **Why It Matters:** Clean schema mapping creates a reliable audit trail and separates tax-sensitive accounts (such as municipal bond interest, meals, entertainment, and social club dues) before downstream tax modeling begins.

### 2. Book-to-Tax Differences & Depreciation M-Adjustments (`Task 2`)
* **What I Did:** Categorized common GAAP-to-Tax discrepancies into **Permanent** vs. **Temporary** differences and determined whether each M-adjustment is **Favorable** (lowers taxable income), **Unfavorable** (increases taxable income), or **Varies** across periods. Modeled a 5-year fixed asset schedule (`2025–2029`) for a `$50,000` asset comparing straight-line book depreciation (`$10,000/yr`) against `100%` bonus tax depreciation (`$50,000` in Year 1).
* **Why It Matters:** Confirmed the zero-sum reversal rule for temporary differences (`-$40,000` favorable in 2025 followed by `+$10,000/yr` unfavorable reversals in 2026–2029, netting to `$0`).

### 3. Federal Taxable Income & Tax Liability Computation (`Task 3`)
* **What I Did:** Reviewed Provided-by-Client (PBC) emails, trial balance extracts, and IRS rules to bridge GAAP Net Income (`$2,800,000`) to Federal Taxable Income (`$3,458,300`) and calculate corporate tax owed at `21%`:
  * **Pre-Tax Book Income:** `$2,800,000 + $598,200 (Federal Tax Add-Back) = $3,398,200`
  * **Net Permanent Differences (`+$312,000` Unfavorable):** Non-deductible entertainment (`+$212,000`) and social club dues (`+$115,000`), offset by tax-exempt municipal bond interest (`-$15,000`).
  * **Net Temporary Differences (`-$251,900` Favorable):** Accelerated depreciation (`-$216,400`), deductible prepaid rent (`-$60,000`) and prepaid insurance (`-$9,500`) under the **IRS 12-Month Rule (Pub. 538)**, and `$34,000` unpaid accrued bonus past the **2½-month cutoff (Treas. Reg. §1.404(b)-1T)** (while `$314,000` accrued vacation and `$200,000` bonus paid by March 15 remained deductible).
  * **Final Federal Tax Liability:** `$3,458,300 × 21% = $726,243`

### 4. Client Summary & Automation Advisory (`Task 4`)
* **What I Did:** Drafted a concise, client-ready update to ABC Inc.’s Finance Controller (Autumn) summarizing FY2025 taxable income results and proposing practical automation workflows.
* **Recommendations:** Leveraging **Alteryx** (and **UiPath RPA / AI-assisted PBC checks**) to automate trial balance scrubbing, recurring account mapping as the business scales, and multi-year fixed asset depreciation tracking.

---

## 💡 Key Learnings & Takeaways

* **Tax Compliance Is a Structured Data Pipeline:** Moving from a raw Trial Balance to Form 1120 taxable income follows clear logical rules—date cutoffs (`2.5-month` accrual rule), coverage windows (`12-month` prepaid rule), and sign hygiene (`+` unfavorable vs. `-` favorable).
* **Audit Trail & Sign Discipline Prevent Costly Errors:** Treating tax-exempt municipal bond interest or qualifying prepaid deductions with the wrong sign directly overstates taxable income; verifying every adjustment against PBC evidence keeps workpapers audit-ready.
* **Domain Knowledge + Automation = High Impact:** Combining foundational accounting/tax logic with tools like **Alteryx** turns repetitive manual spreadsheet reconciliation into scalable, error-resistant workflows.

---

## 🛠️ Skills & Tools Applied

* **Accounting & Tax:** Trial Balance Mapping, GAAP-to-Tax Reconciliations (Schedule M-1 / M-3 Logic), Bonus Depreciation (`IRS Pub. 946`), Prepaids (`IRS Pub. 538`), Accrued Compensation (`Treas. Reg. §1.404(b)-1T`), Corporate Tax Computation (`21%`).
* **Analytics & Automation Concepts:** Financial Data Normalization, Audit Trail Verification, Workflow Automation (`Alteryx`, `UiPath RPA`), Executive Client Communication.
