# PwC Tax Virtual Experience (Forage) — Task 4: Client Tax Summary & Process Automation Advisory

## 📌 Project Overview

**Client:** ABC Inc. (Fitness & Retail Company)  
**Recipient:** Autumn (Finance Controller, ABC Inc.) — drafted for PwC Tax Partner Matthew  
**Tax Period:** Year Ended December 31, 2025  
**Objective:** Translate the technical work from Tasks 1–3 into a clear, executive-friendly client email summarizing ABC Inc.’s FY2025 federal tax return results, and propose practical automation and AI improvements to streamline future tax compliance cycles.

---

## 🎯 Communication & Advisory Goals

A strong tax deliverable doesn't just get the numbers right—it explains what those numbers mean for the client and shows how to make next year easier:

1. **Executive Clarity:** Summarize the Book-to-Tax reconciliation and final tax liability without burying the client in spreadsheet mechanics.
2. **Actionable Value-Add:** Recommend realistic, PwC-approved automation tools (**Alteryx**, **UiPath RPA**, **Tableau**, and **AI agents**) tied directly to bottlenecks observed in ABC Inc.’s engagement.

---

## 📊 Key FY2025 Tax Findings Communicated

| Metric | Amount (`$`) | Key Takeaway for Client |
| :--- | :---: | :--- |
| **GAAP Net Income** | `$2,800,000` | Starting after-tax book profit for FY2025 |
| **Pre-Tax Book Income** | `$3,398,200` | Reflects `$598,200` federal income tax expense add-back |
| **Net Permanent Adjustments** | `+$312,000` *(Unfavorable)* | Driven by non-deductible entertainment (`$212,000`) and social club dues (`$115,000`), offset by tax-exempt municipal bond interest (`-$15,000`) |
| **Net Temporary Adjustments** | `-$251,900` *(Favorable)* | Driven by `100%` bonus depreciation (`-$216,400`), deductible prepaid rent (`-$60,000`) and prepaid insurance (`-$9,500`) under the 12-month rule, and `$34,000` unpaid accrued bonus past the 2½-month cutoff |
| **Federal Taxable Income** | **`$3,458,300`** | Final taxable base for FY2025 |
| **Corporate Tax Rate** | **`21%`** | US federal statutory corporate tax rate |
| **Total Federal Tax Liability** | **`$726,243`** | Total federal tax owed for the year ended `12/31/2025` |

---

## ⚙️ Automation & AI Value-Add Recommendations

To reduce manual spreadsheet work and improve accuracy as ABC Inc. scales, the advisory email highlights targeted ways to modernize the tax workflow:

1. **Automated Trial Balance Scrubbing & Account Mapping (`Alteryx` + `UiPath RPA`):**
   * Use **UiPath RPA** to extract trial balance exports from ABC Inc.’s accounting system and validate prior-period carryforwards.
   * Use **Alteryx** workflows to standardize raw account names, map new general ledger accounts into the 4-digit Chart of Accounts automatically, and apply recurring cutoff checks (such as the March 15 accrued bonus deadline).
2. **Fixed Asset & Depreciation Tracking (`Alteryx`):**
   * Replace manual multi-year depreciation schedules with repeatable **Alteryx** workflows that track book vs. tax asset bases, apply bonus depreciation rules, and calculate multi-year timing reversals automatically.
3. **AI-Assisted PBC Review & Tax Visibility (`AI Agents` + `Tableau`):**
   * Use **AI agents** to review incoming client support emails and invoices (flagging entertainment vs. meal splits or prepaid policy windows early) and **Tableau** dashboards to give ABC Inc.’s finance leadership clear visibility into effective tax rates and projected cash taxes.

---

## ✉️ Final Client Summary Email

```text
To: Autumn (ABC Inc. Finance Controller)
Subject: ABC Inc. Tax Return Updates & Insights

Good morning Autumn,

We wanted to update you on the progress of your FY2025 federal tax return and share a few ways PwC can add value by making your tax reporting process more efficient going forward.

First, we mapped your trial balance accounts and calculated your permanent and temporary book-to-tax adjustments to determine your taxable income. Overall, you had unfavorable permanent adjustments totaling $312,000 and favorable temporary adjustments totaling $251,900. Your federal taxable income for the year ended 12/31/2025 is $3,458,300. Applying the 21% federal corporate tax rate, your total federal tax liability is $726,243.

Looking ahead, we see two immediate opportunities to streamline your tax compliance process using Alteryx:

1. Trial Balance Scrubbing & Account Mapping: As ABC Inc. grows and adds new accounts to its trial balance, Alteryx workflows can automatically clean, standardize, and map account balances for tax software ingestion—eliminating manual mapping work.
2. Fixed Asset & Depreciation Management: Fixed assets involve many moving parts across multiple tax years. Using Alteryx to automate book-to-tax depreciation schedules will save significant time and reduce manual tracking errors in future cycles.

Please let me know if you have any questions on anything covered in this update.

Best,
Arghyajyoti Samui
Tax Team, PwC
```

---

## 🔍 Key Takeaways

* **Client-Ready Communication:** Distilling a multi-tab tax reconciliation into a concise, jargon-free email builds trust with busy finance leaders.
* **Practical Automation Mindset:** Pairing accounting domain knowledge with tools like **Alteryx**, **UiPath**, and **AI-assisted document checks** turns one-off compliance work into a scalable, repeatable data pipeline.

## 🛠️ Skills Demonstrated

* Executive Client Communication & Tax Reporting
* Tax Process Automation Design (**Alteryx**, **UiPath RPA**, **AI Agents**, **Tableau**)
* End-to-End US Corporate Tax Compliance (Trial Balance $\rightarrow$ BTDs $\rightarrow$ Taxable Income $\rightarrow$ Client Advisory)
