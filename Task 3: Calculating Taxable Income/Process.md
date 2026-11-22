# PwC Tax Virtual Experience (Forage) — Task 3: Calculating Federal Taxable Income

## 📌 Project Overview

**Client:** ABC Inc. (Fitness & Retail Company)  
**Tax Period Ended:** December 31, 2025  
**Role:** Tax Associate (Tax & Data Analytics Perspective)  
**Objective:** Reconcile ABC Inc.’s GAAP **Net Income** to **Pre-Tax Book Income**, apply **Permanent** and **Temporary** Book-to-Tax Differences (BTDs) supported by Provided-by-Client (PBC) documentation and IRS guidance, and compute **Federal Taxable Income** and **Corporate Tax Liability** at the $21\%$ US statutory rate.

---

## 🎯 Business & Tax Analytics Pipeline

In corporate tax compliance, raw book net income must pass through a deterministic rule-based transformation pipeline before computing tax owed:

$$
\text{Pre-Tax Book Income} = \text{GAAP Net Income} + \text{Federal Income Tax Expense Add-Back}
$$

$$
\text{Federal Taxable Income} = \text{Pre-Tax Book Income} + \text{Net Permanent Differences} + \text{Net Temporary Differences}
$$

$$
\text{Total Federal Tax Liability} = \text{Federal Taxable Income} \times 21\%
$$

* **Unfavorable Adjustments (`+`):** Increase taxable income relative to book income (e.g., disallowed expenses or deferred tax deductions).
* **Favorable Adjustments (`-`):** Decrease taxable income relative to book income (e.g., tax-exempt income or accelerated tax deductions).

---

## 📑 PBC Evidence & IRS Tax Research Applied

| Account / Item | PBC Evidence & Authoritative Rule | Book vs. Tax Treatment | M-Adjustment (`+/-`) |
| :--- | :--- | :--- | :---: |
| **Federal Income Tax Expense** | Book Net Income ($\$2,800,000$) is after-tax; add back federal tax provision ($\$598,200$) to establish Pre-Tax Book Income. | Non-deductible for federal tax purposes; added back to Net Income. | **`+$598,200`** *(Add-Back)* |
| **Meals & Entertainment** | Controller email confirms Account `5003` Meals ($\$115,000$ business meals) and Account `5004` Entertainment ($\$212,000$ social/recreation events). Under **IRC §274 / IRS Pub. 463**, entertainment is $100\%$ disallowed (`+$212,000` model key baseline; under strict statutory 50% meal limitation, an additional `+$57,500` applies for a total of `+$269,500`). | Entertainment is permanently non-deductible (`+$212,000` in model key; `+$269,500` including 50% business meal disallowance). | **`+$212,000`** *(Model Key)* / **`+$269,500`** *(IRC §274)* |
| **Club Dues** | Trial Balance Account `5017` shows $\$115,000$ paid to a social organization solely for social events (**IRS Pub. 334 / §274**). | Social club dues are permanently disallowed for tax. | **`+$115,000`** *(Unfavorable)* |
| **Fines & Penalties** | PBC confirmation states $\$0$ incurred during FY 2025. | No adjustment required. | **`$0`** |
| **Tax-Exempt Interest** | PBC confirmation shows $\$15,000$ municipal bond interest income (**IRC §103**). | Included in GAAP income but exempt from federal tax; subtracted out. | **`($15,000)`** *(Favorable)* |
| **Depreciation** | Provided fixed asset schedule BTD from accelerated/bonus tax depreciation exceeding straight-line book depreciation. | Tax deduction exceeds book expense in 2025. | **`($216,400)`** *(Favorable)* |
| **Accrued Bonus** | Year-end accrual was $\$234,000$; $\$200,000$ was paid on March 15, 2026 (within the **2½-month window** under **Treas. Reg. §1.404(b)-1T**). | Only the unpaid balance after March 15 ($\$234,000 - \$200,000 = \$34,000$) is deferred/added back in 2025. | **`+$34,000`** *(Unfavorable)* |
| **Accrued Vacation** | Year-end accrual was $\$314,000$; all $\$314,000$ was paid out by March 15, 2026 (**Treas. Reg. §1.404(b)-1T**). | $100\%$ paid within $2.5$ months of year-end; fully deductible in 2025 (`$0` BTD). | **`$0`** |
| **Prepaid Rent** | Paid $\$60,000$ on `12/31/2025` for Jan–Mar 2026 (3 months $\le 12$ months). Qualifies for the **12-Month Rule (IRS Pub. 538 / Treas. Reg. §1.263(a)-4)**. | Capitalized as a GAAP asset (`$0` book expense) but immediately deductible for tax in 2025. | **`($60,000)`** *(Favorable)* |
| **Prepaid Insurance** | Paid $\$9,500$ on `12/31/2025` for Jan 1–Dec 31, 2026 (12 months $\le 12$ months). Qualifies for the **12-Month Rule (IRS Pub. 538)**. | Capitalized as a GAAP asset (`$0` book expense) but immediately deductible for tax in 2025. | **`($9,500)`** *(Favorable)* |

---

## 🧮 Taxable Income & Tax Liability Reconciliation Schedule (FY 2025)

| Reconciliation Line Item | Model Key Amount (`$`) | Notes / Formula |
| :--- | ---: | :--- |
| **GAAP Net Income (Loss)** | `$2,800,000` | Provided from FY 2025 financial statements |
| **Add Back: Federal Income Tax Expense** | `$598,200` | Reconciles after-tax Net Income to Pre-Tax Book Income |
| **Pre-Tax Book Income (Loss)** | **`$3,398,200`** | `= $2,800,000 + $598,200` |
| **Permanent Differences:** | | |
| Meals & Entertainment | `$212,000` | Non-deductible entertainment (`$269,500` if applying 50% limit on `$115k` meals) |
| Club Dues | `$115,000` | Social organization membership dues (`Account 5017`) |
| Fines & Penalties | `$0` | None incurred in FY 2025 |
| Tax-Exempt Interest | `($15,000)` | Municipal bond interest excluded from taxable income |
| **Total Permanent Differences** | **`$312,000`** | `= $212,000 + $115,000 + $0 - $15,000` |
| **Temporary Differences:** | | |
| Depreciation | `($216,400)` | Provided accelerated tax depreciation BTD |
| Accrued Bonus | `$34,000` | Unpaid portion after March 15, 2026 (`$234,000 - $200,000`) |
| Prepaid Rent | `($60,000)` | Deductible in 2025 under the IRS 12-Month Rule |
| Prepaid Insurance | `($9,500)` | Deductible in 2025 under the IRS 12-Month Rule |
| Accrued Vacation | `$0` | Fully paid on March 15, 2026 (within $2.5$-month window) |
| **Total Temporary Differences** | **`($251,900)`** | `= -$216,400 + $34,000 - $60,000 - $9,500 + $0` |
| **Federal Taxable Income** | **`$3,458,300`** | `= $3,398,200 + $312,000 - $251,900` |
| **Corporate Tax Rate** | **`21%`** | Flat US federal corporate income tax rate (IRC §11) |
| **Total Federal Tax Liability** | **`$726,243`** | `= $3,458,300 × 21%` |

---

## 🔍 Key Takeaways for Tax & Data Analytics

1. **Rule-Based Feature Engineering:** Tax compliance transforms accounting balances using statutory cutoff rules—such as **date-delta checks** (`payment_date <= year_end + 2.5 months` under Reg. §1.404(b)-1T) and **coverage-window checks** (`benefit_months <= 12` under the Pub. 538 12-Month Rule).
2. **Sign-Convention Discipline:** Enforcing strict sign hygiene (`+` for Unfavorable add-backs, `-` for Favorable deductions) prevents double-taxing tax-exempt municipal interest or reversing valid prepaid deductions.
3. **Audit Trail & PBC Traceability:** Every line item links directly to client emails, Trial Balance accounts, or IRS code sections, ensuring audit-ready documentation for Senior Associate and Manager review.

---

## 🛠️ Skills Demonstrated

* US Corporate Income Tax Computation (Form 1120 Logic)
* PBC Document Review & Audit Trail Verification
* IRS Tax Research (**Pub. 538**, **Pub. 463**, **Pub. 334**, **Treas. Reg. §1.404(b)-1T**)
* Dynamic Financial Reconciliation Modeling in Microsoft Excel
