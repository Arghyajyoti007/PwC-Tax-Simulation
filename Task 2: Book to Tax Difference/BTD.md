# PwC Tax Virtual Experience (Forage) — Task 2: Book-to-Tax Differences (BTDs) & Depreciation M-Adjustments

## 📌 Project Overview

**Client:** ABC Inc. (Fitness & Retail Company)

**Role:** Tax Associate (Tax & Data Analytics Perspective)

**Objective:** Bridge GAAP financial statement income (**Book Income**) to IRS tax return income (**Taxable Income**) by classifying **Permanent vs. Temporary** Book-to-Tax Differences (BTDs), determining **Favorable vs. Unfavorable** M-adjustment directions, and modeling multi-year **Bonus Depreciation** schedules (2025–2029) under **IRS Publication 946**.

---

## 🎯 Business & Tax Analytics Context

Corporate tax compliance requires reconciling financial accounting records (GAAP) against Internal Revenue Code (IRC) rules before computing tax liability:

$$\text{Taxable Income} = \text{Book Income} + \text{Unfavorable Adjustments} - \text{Favorable Adjustments}$$

* **Permanent Differences:** Discrepancies between GAAP and IRS rules that **never reverse** in future periods (e.g., tax-exempt income or statutory expense disallowances).
* **Temporary (Timing) Differences:** Differences in **when** revenue or expenses are recognized across periods that **fully reverse** over time (net cumulative impact $= \$0$).
* **Favorable vs. Unfavorable M-Adjustments:**
  * **Favorable (`-`):** Subtracts from Book Income $\rightarrow$ **decreases** Taxable Income (e.g., tax-exempt municipal bond interest, accelerated Year 1 tax depreciation).
  * **Unfavorable (`+`):** Adds back to Book Income $\rightarrow$ **increases** Taxable Income (e.g., non-deductible fines, social club dues, or later-year depreciation reversals).

---

## 📊 Part 1 & Part 2: Classification of Book-to-Tax Differences

| Book-to-Tax Difference Item | Part 1: Difference Type | Part 2: M-Adjustment Direction | Tax & Accounting Rationale |
| :--- | :--- | :--- | :--- |
| **Federal Income Tax Expense** | Permanent | Unfavorable | Federal income taxes expensed on GAAP books are non-deductible on the federal return. |
| **Municipal Bond Interest** | Permanent | Favorable | Tax-exempt interest included in GAAP revenue is subtracted to arrive at taxable income. |
| **Meals and Entertainment** | Permanent | Unfavorable | Entertainment is $100\%$ disallowed and qualifying meals are subject to statutory limits (IRC §274 / Pub. 463). |
| **Fines and Penalties** | Permanent | Unfavorable | Statutory fines paid for legal violations are permanently non-deductible. |
| **Membership Dues (Social Organization)** | Permanent | Unfavorable | Social, athletic, or country club dues are permanently disallowed under IRS rules. |
| **Depreciation Expense** | Temporary | Varies | Accelerated tax depreciation exceeds book depreciation in Year 1 (**Favorable**) and reverses in subsequent years (**Unfavorable**). |
| **Accrued Compensation** | Temporary | *Timing* | Deductible for tax when paid/economically performed rather than when accrued for GAAP. |
| **Accrued Bonus** | Temporary | *Timing* | Reverses once paid within statutory post-year-end windows. |
| **Accrued Vacation** | Temporary | *Timing* | Timing difference between GAAP accrual and tax deductibility upon payout. |
| **Prepaid Rent** | Temporary | *Timing* | Capitalized as a GAAP asset and amortized over lease periods vs. tax deductibility timing rules. |
| **Prepaid Insurance** | Temporary | *Timing* | GAAP amortization over coverage term vs. tax timing rules. |
| **Deferred Revenue** | Temporary | *Timing* | Cash received in advance is recognized for tax earlier than GAAP revenue recognition upon service delivery. |

---

## 🧮 Part 3 & Part 4: Fixed Asset Depreciation M-Adjustment Schedule (2025–2029)

### Asset Parameters (IRS Publication 946)
* **Acquisition / Placed-in-Service Date:** January 1, 2025
* **Cost Basis:** $\$50,000$ (Qualified Property)
* **Book Depreciation Method:** Straight-Line over 5 years ($\frac{\$50,000}{5} = \$10,000/\text{year}$)
* **Tax Depreciation Method:** $100\%$ Bonus Depreciation in Year 1 ($\$50,000$ deducted in 2025; $\$0$ remaining tax basis for 2026–2029)
* **BTD Formula:** $\text{Book Depreciation} - \text{Tax Depreciation}$

### 5-Year Book-to-Tax Reconciliation Table

| Year | Book Depreciation | Tax Depreciation | Book-to-Tax Difference (BTD) | M-Adjustment Direction | Tax Impact Explanation |
| :---: | :---: | :---: | :---: | :---: | :--- |
| **2025** | $\$10,000.00$ | $\$50,000.00$ | `($40,000.00)` | **Favorable** | $100\%$ bonus depreciation exceeds straight-line book expense, reducing 2025 taxable income by $\$40,000$. |
| **2026** | $\$10,000.00$ | $\$0.00$ | $\$10,000.00$ | **Unfavorable** | Full tax basis was recovered in 2025; $\$10,000$ book expense is added back, increasing taxable income. |
| **2027** | $\$10,000.00$ | $\$0.00$ | $\$10,000.00$ | **Unfavorable** | Timing reversal continues; book expense exceeds $\$0$ tax depreciation. |
| **2028** | $\$10,000.00$ | $\$0.00$ | $\$10,000.00$ | **Unfavorable** | Timing reversal continues; book expense exceeds $\$0$ tax depreciation. |
| **2029** | $\$10,000.00$ | $\$0.00$ | $\$10,000.00$ | **Unfavorable** | Final year of book depreciation; cumulative BTD across 2025–2029 nets to **$\$0.00$**. |
| **Total** | **$\$50,000.00$** | **$\$50,000.00$** | **$\$0.00$** | **Temporary (Net Zero)** | Confirms complete reversal over the 5-year useful life. |

---

## 🔍 Key Takeaways for Tax & Data Analytics

1. **Zero-Sum Proof for Temporary Differences:** Validating that cumulative Book Depreciation ($\$50,000$) equals cumulative Tax Depreciation ($\$50,000$) acts as a built-in data integrity check for multi-year tax schedules.
2. **Schedule M-1 / M-3 Readiness:** Categorizing adjustments by **Permanent vs. Temporary** and **Favorable vs. Unfavorable** mirrors the exact logic required to populate **IRS Form 1120 (Schedule M-1 / M-3)** and compute **Deferred Tax Assets / Liabilities (ASC 740)**.
3. **Authoritative IRS Research:** Applied **IRS Publication 946** (Depreciation), **Publication 463** (Meals & Entertainment), and **Publication 334** (Small Business Tax Guide).

---

## 🛠️ Skills Demonstrated

* GAAP-to-Tax Reconciliation (Schedule M-1 / M-3 Logic)
* Fixed Asset & Bonus Depreciation Modeling (IRS Pub. 946)
* Permanent vs. Temporary Timing Analysis
* Financial Modeling & Audit Trail Documentation in Microsoft Excel
