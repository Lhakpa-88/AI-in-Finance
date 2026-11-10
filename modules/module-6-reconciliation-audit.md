# Module 6 — Bank Reconciliation, Partner Transaction Sampling & Audit Prep
**Duration: 2.5 hours** · Part of *AI for Finance Professionals* (20-hr PBL course)

> Standalone facilitator brief. See `../course-design/delivery-methodology.md` for the session rhythm used in every module. This module runs as three linked parts inside one extended block; the 55-minute "Work it" phase is split across Parts A and B, and Part C runs inside "Verify & critique".

## Problem scenario
The external audit is in three weeks, and the quarter-end bank reconciliation still has unexplained differences. On top of that, three implementing partners have just submitted their quarterly financial reports with ledgers of 400–900 transactions each. As grants accountant you cannot voucher every line, but you must sign off on partner spend and find your own problems before the auditor does.

## Learning objectives
Participants can use AI to:
- structure and speed up a bank reconciliation and explain reconciling items, while recomputing the reconciliation themselves;
- design a defensible **sampling plan** for reviewing partner (sub-grantee) transactions, generate the sample from a ledger, and document the method so an auditor can rely on it;
- build an audit-readiness checklist, surface anomaly leads, and draft management-response language — keeping detection and conclusions human-led.

## Why sampling is in this module
Grants accountants who review partner financial reports face the same tedious job every quarter: hundreds or thousands of transactions, limited time, and full accountability for the sign-off. Looking at every line is neither possible nor what auditors expect. What *is* expected is a documented, risk-based sample with a clear rationale, a consistent testing procedure, and a record of exceptions and follow-up. AI is well suited to the framing, drafting, and bookkeeping around sampling; the judgement about risk, the vouching of documents, and the conclusion stay with the accountant.

---

## Part A — Bank reconciliation with AI as the explainer (≈45 min)

### Concepts
- The four reconciling-item families: outstanding cheques/payments, deposits in transit, bank charges and interest not yet booked, and errors (bank-side or ledger-side).
- Using AI to **match** two lists (bank statement vs. cash book) on amount, date window, and reference, and to list unmatched items on both sides.
- Using AI to **explain** each unmatched item in plain language and to propose the correcting entry — which the accountant then approves or rejects.
- Where ledger-embedded AI (QuickBooks, Xero) already suggests matches, and what it still gets wrong (split payments, FX differences, duplicate references).

### Hands-on
Each group receives a synthetic bank statement and the matching cash-book extract for one month, with seeded differences: two outstanding payments, one deposit in transit, an unbooked bank charge, a transposition error in the ledger, and one genuine duplicate payment. Groups:
1. Ask AI to match the two lists and produce an unmatched-items table for each side.
2. Ask AI to classify each unmatched item and draft the adjusting entry or the "carry forward as outstanding" note.
3. **Rebuild the reconciliation statement themselves** in a spreadsheet: adjusted bank balance = adjusted book balance.

### Verification focus
If the rebuilt reconciliation does not balance to zero, the AI's matching is wrong somewhere — find it. The duplicate payment must be found by a person checking the vouchers, not accepted because the model "thinks" it is an error. Reconciliation data is confidential: only the synthetic set is used, and participants practise what they would redact (payee names, account numbers) before any real use.

---

## Part B — Audit sampling of partner transactions (≈60 min)

### Concepts
- **Population and sampling unit**: the partner ledger for the period; one transaction or one voucher as the unit.
- **Why not 100%**: time, cost, and the fact that reviewing every line does not give proportionately more assurance than a well-designed sample.
- **Sampling approaches** and when each fits:
  - *Judgemental / risk-based* — pick the high-risk lines deliberately (large, round-number, near period-end, new vendors, cash payments, budget lines with history of issues).
  - *Random* — every item has an equal chance; good for the "everything else" layer.
  - *Stratified* — split the ledger into bands (e.g., above a key-item threshold, mid-band, low-value) and sample each band differently.
  - *Monetary unit sampling (MUS)* — probability proportional to value, so large amounts are far more likely to be picked; typical for expenditure verification.
  - *Systematic* — every nth item from a random start; simple to document.
- **Key items**: anything above a threshold (say 5% of the partner's quarterly spend, or a fixed amount) is tested 100%; sampling applies only below it.
- **Sample size as a judgement**: driven by the partner's risk rating, prior findings, materiality, and the assurance you need — not a magic number. A typical NGO partner review might test all key items plus 25–60 sampled items, scaled up for a high-risk partner.
- **What is tested per sampled item** (the testing procedure): supporting document exists; approved by the right person; arithmetically correct; within budget line and period; eligible under the donor rules; evidence of receipt of goods/services; recorded correctly in the ledger.
- **Documentation**: population size and total, method, threshold, sample size and rationale, the selected items with IDs, test results, exceptions, projected error if any, follow-up and conclusion.

### How AI helps — and where it must not lead
| AI does well | Accountant keeps |
|---|---|
| Drafts the sampling plan from your stated risk rating, materiality, and time budget | Decides the risk rating and the threshold |
| Stratifies the ledger and reports population totals per band | Checks the totals match the partner's report |
| Generates a random or systematic selection from the synthetic ledger (or writes the spreadsheet formula/script to do it) | Confirms the selection is reproducible (fixed seed, documented start point) |
| Produces a blank testing workpaper with one row per sampled item and one column per test | Performs the actual vouching against documents |
| Summarises exceptions and drafts the findings memo and the partner follow-up letter | Decides which exceptions are errors, which are findings, and whether to extend the sample |

### Hands-on
Each group receives a synthetic partner ledger (≈600 lines, one quarter, with budget line, vendor, date, amount, payment method, and voucher reference) plus a one-paragraph partner risk profile. Seeded into the ledger: two transactions above the key-item threshold, a cluster of round-number cash payments to one vendor, three transactions dated after period-end, one duplicated voucher reference, and a handful of lines with missing voucher references. Groups:
1. Ask AI to propose a sampling plan for this partner (approach, threshold, sample size, rationale), then **argue with it** — change the risk rating and see how the plan should change.
2. Ask AI to stratify the ledger and pull the key items plus a random or MUS sample, with the selection method written down so another person could reproduce it.
3. Ask AI to generate the testing workpaper and a one-page sampling memo.
4. "Voucher" a few sampled items against a mini set of synthetic supporting documents, record the results, and ask AI to draft the exceptions summary and the partner follow-up letter.

### Verification focus
- Does the sample actually include the key items and the risky clusters? If the risk-based layer missed the round-number cash cluster, the plan was wrong, whatever the AI said.
- Is the selection reproducible? Re-run it and compare. A sample you cannot reproduce is one an auditor cannot rely on.
- Did the AI invent a "standard" sample size or a donor rule? Ask for the source; if none, treat as unverified.
- Partner ledgers carry vendor and sometimes staff names: practise redacting or pseudonymising before any real-world use, and prefer a data-protected account.

---

## Part C — Anomaly spotting and audit readiness (≈30 min, inside Verify & critique and Share)

### Concepts
- Drafting an audit-readiness checklist from the donor agreement and last year's management letter.
- Describing patterns for AI to look for across the whole ledger (not just the sample): duplicate amounts, weekend postings, split payments just under approval limits, vendors sharing bank details.
- Summarising findings and drafting management-response language.

### Hands-on
Feed AI the same synthetic ledgers and ask it to flag anomalies and explain its reasoning. Then critique which flags are real (seeded) and which are noise.

### Verification focus
AI-flagged "anomalies" are leads, not conclusions. Every flag is investigated, not actioned blindly. The anomaly sweep complements the sample; it does not replace it.

---

## Deliverables
1. A completed bank reconciliation statement with the explained reconciling items and proposed adjusting entries.
2. A **partner transaction sampling pack**: sampling plan and rationale, reproducible selection, testing workpaper, exceptions summary, and partner follow-up letter template.
3. An audit-prep checklist and a template management-response paragraph.

## Facilitator notes
- Build the Part B ledger large enough that no one is tempted to read every line. The tedium is the point.
- Seed the key items and the cash cluster so that a purely random sample is likely to miss the cluster — this makes the case for the risk-based layer.
- Pre-test the selection prompts; models sometimes "randomly" pick the first items or repeat the same ones. Ask for a seed and a method, or have the AI write a spreadsheet formula (e.g., RAND with a frozen column, or a MUS interval formula) instead of picking items itself.
- Localise the testing procedure to the cohort's main donors' expenditure-verification requirements where possible.
