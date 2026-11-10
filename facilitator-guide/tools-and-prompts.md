# Tools & Prompts per Module

A facilitator reference: for every problem scenario in the course, which AI tool to use, why, and the prompts to demonstrate and hand to groups. Pair it with `../resources/tool-stack.md` (what the tools are) and the module briefs in `../modules/` (what the session does).

## How to use this document
- **Pre-test every prompt** on the day's actual tool version. Outputs drift between model updates; a prompt that produced a clean table last cohort may not this time.
- **Synthetic data only.** Every prompt below assumes the dataset pasted in is from `synthetic-data/`. Wherever a prompt says "paste the table", the facilitator pastes the synthetic file, never anything real.
- **Prompts are starting points.** Groups should adapt them. The learning is in the adapting and the checking, not in copying.
- **Tool labels used here:**
  - **GPA** = general-purpose assistant (ChatGPT, Claude). Default for drafting, reasoning, and explaining.
  - **GPA-protected** = a paid, enterprise, or team tier of a GPA with data not used for training. Required wherever the real-world version of the task involves confidential data.
  - **Citation-first** = live-search assistant that cites sources (Perplexity). For public regulatory and tax questions.
  - **Sheet-AI** = spreadsheet-embedded assistant (Copilot in Excel, Gemini in Sheets). For formulas, pivots, cleaning inside the sheet.
  - **Ledger-AI** = assistant inside the accounting platform (QuickBooks, Xero). Only where the organisation already uses it.
- **Free-tier cohorts:** every module can be run on a free GPA alone. The Sheet-AI and Ledger-AI entries are "show if available".

## The two prompts that go in every module
Keep these on the wall or in the shared doc.

**Grounding prompt (prefix to any task):**
```
You are assisting a non-profit finance professional. Use only the data and documents I provide. If something is not in what I gave you, say "not in source" rather than guessing. Show your working for any number. List any assumptions you made at the end.
```

**Self-check prompt (suffix after any output):**
```
Now review your own answer above. List every number, rule, or fact you stated, and for each one say whether it came from my input or from your general knowledge. Flag anything that should be verified by a person before use.
```

---

## Module 0 — Orientation & AI foundations *(1.5 hrs)*
**Problem:** Two AI outputs are projected. One is right; one has a plausible wrong total and an invented donor regulation. Which do you trust?

**Tool:** GPA (free tier is fine). The point is to show the model's behaviour, so use the plainest tool.

**Facilitator prep prompt** (to generate the two outputs before class, then edit one to plant the errors):
```
Summarise the following grant budget in five lines for a programme manager, including the total and the share spent on staff costs. [paste synthetic budget table]
```

**Participant prompt (run by everyone, same wording, compare results):**
```
A project has these expense lines: Staff 48,250; Travel 7,980; Supplies 12,415; Partner grants 36,700; Indirect at 7% of direct costs. What is the total budget? Show your working.
```
Debrief: how many different totals appeared in the room? Which were arithmetic slips, which were the indirect-cost base being interpreted differently?

**Demonstration of hallucination:**
```
What does the [invent a plausible donor name] cost-eligibility policy say about charging staff gratuity to a grant? Quote the clause.
```
The model will usually produce a confident, cited-looking answer for a donor that does not exist. That moment is the module.

---

## Module 1 — Verification & data protection *(2 hrs)*
**Problem:** A colleague pasted the full grant budget, salaries and beneficiary list into a free consumer AI. What is exposed, and what should the organisation do?

**Tool:** GPA for the analysis. Also open the privacy or data-use settings page of the free tool on screen so participants see what the default actually says. Contrast with a GPA-protected tier.

**Prompts:**

Exposure analysis:
```
A finance officer at an NGO pasted a document containing staff names with salaries, a list of beneficiary names and villages, and donor budget figures into a free consumer AI chatbot. List the categories of data exposed, the realistic risks for each category, the immediate actions the organisation should take in the next 48 hours, and the structural controls to prevent recurrence. Separate "immediate" from "structural".
```

De-identification practice (the core hands-on):
```
Here is a budget table. Rewrite it so it can be safely shared with an external tool: replace every person's name with a role code (e.g. STAFF-01), replace beneficiary names with IDs, round salaries to the nearest thousand, and keep all totals and structure intact. Then list each change you made so I can reverse it later. [paste synthetic budget]
```
Verification: did the model leave a name in a comment column or a footnote? It frequently does.

Building the red-line card:
```
Draft a one-page "never paste into AI" card for a non-profit finance team. Group items under: personal data, salary and HR, donor-confidential, banking and payment, legal and safeguarding. Add a two-question gate the person asks before every prompt.
```

---

## Module 2 — Budgets *(2 hrs)*
**Problem:** Proposal budget due in 48 hours. You have a donor template, a scope of work and a grade scale. Blank sheet.

**Tools:** GPA for structure, assumptions and narrative. Sheet-AI for formulas and totals once the structure is in the sheet. Rule: the AI never produces the final arithmetic; the spreadsheet does.

**Prompts:**

Structure from scope of work:
```
Here is a scope of work and a donor budget template with its cost categories. Propose a line-item budget structure: for each template category, list the lines we will need, the unit, the likely quantity driver, and any item that commonly gets forgotten. Do not invent amounts. [paste scope of work and template headings]
```

Pressure-test as a sceptical reviewer:
```
Act as a sceptical donor budget reviewer. Here is our draft budget and the scope of work. Identify: lines that look unrealistic relative to the activities, missing cost categories, items likely to be unallowable, ratios a reviewer would question (staff vs activity, indirect vs direct, travel per person-trip). Rank by seriousness. [paste draft budget]
```

Justification narrative:
```
Write budget justification notes for these lines in the donor's required style: one short paragraph per line explaining the basis of estimate (unit, quantity, rate, source of the rate). Use only the figures given. [paste budget lines with basis]
```

Sheet-AI prompt (inside Excel or Sheets):
```
Add a formula in column G that multiplies quantity (D) by unit cost (E) by number of units (F), and a subtotal row for each category, and a grand total. Explain each formula.
```
Verification: recompute two subtotals and the grand total by hand or with a plain SUM.

---

## Module 3 — Donor financial reports & narratives *(2 hrs)*
**Problem:** Figures are final. The variance narrative and the plain-language summary for a programme lead are not.

**Tool:** GPA. Use GPA-protected in real life because actuals are donor-confidential.

**Prompts:**

Variance identification:
```
Here is a budget-vs-actual table for Q2. Calculate the variance and percentage variance for each line, then list the five lines that most need explanation, stating for each whether it is over or under spend and by how much. Use only the table. [paste table]
```

Three-audience narrative (the core hands-on):
```
Using the variance table and the explanations I give below, write three versions of the variance commentary:
1. For the donor: formal, every number traceable, one paragraph per material variance, referencing budget line codes.
2. For the board: half a page, plain language, focused on risks and what management is doing.
3. For the programme team: five bullet points, no jargon, telling them what it means for the next quarter.
Explanations for the variances: [facilitator provides the "reasons" so AI does not invent them]
```
Verification: for every number in each narrative, find it in the table. Every "because" statement must match the reasons given, not an invented cause.

Summarising long donor guidance:
```
Here is the donor's financial reporting guideline. Extract: the report due dates, the required templates, the variance threshold that requires explanation, the currency and exchange-rate rule, and the sign-off requirement. Quote the clause number for each. If something is not stated, say "not stated". [paste guideline excerpt]
```

---

## Module 4 — Excel & messy-data wrangling *(2.5 hrs)*
**Problem:** A ledger or bank export with merged cells, mixed date formats, and duplicates. Reconciliation is tomorrow.

**Tools:** Sheet-AI for in-place cleaning and formulas where available. GPA to write and explain formulas, plan cleaning steps, or generate a small script. Both work; the GPA route is the free-tier fallback.

**Prompts:**

Cleaning plan:
```
Here are the first 30 rows of a ledger export. Diagnose the data-quality problems you can see (mixed date formats, merged header cells, duplicate rows, trailing spaces, numbers stored as text, etc.) and give me a numbered cleaning plan I can follow in Excel, with the exact function or menu action for each step. [paste sample rows]
```

Formula writing with explanation:
```
In Excel, write a formula that converts dates stored as text in the formats "03/07/2026", "7-Mar-26" and "2026-03-07" into a real date in column B. Then explain the formula part by part so I could rewrite it myself.
```

Duplicate detection:
```
Write a formula or step that flags rows where the date, amount and reference match another row, and explain how to review the flagged rows rather than deleting them automatically.
```

Pivot by plain language (Sheet-AI):
```
Summarise this table by budget line and month, showing total amount, and add a column comparing to the budget column in the Budget sheet.
```

Recipe capture (end of session):
```
Here is the list of cleaning steps we performed and the formulas we used. Turn it into a reusable checklist titled "Monthly export cleaning recipe", with a verification step after each stage. [paste steps]
```
Verification: test every formula on three known rows before trusting it on 3,000.

---

## Module 5 — Compliance & policy interrogation *(2.5 hrs)*
**Problem:** A programme wants to charge a cost that may be unallowable under donor rules and may carry a local VAT/TDS implication. Defensible answer by end of day.

**Tools:** Citation-first for public regulatory and tax questions (to find the current provision). GPA with the actual document pasted in for the eligibility reasoning. The second step is the one that matters: retrieval over recall.

**Prompts:**

Finding the public source (citation-first):
```
What is the current rate and threshold for TDS on payments to contractors in [country], and which section of the Income Tax Act sets it? Give the source link and date of the source.
```
Verification: open the link. Check the date. Check it is the government or a primary source, not a blog.

Grounded eligibility reasoning (GPA, document pasted):
```
Below is the donor's cost-eligibility policy. Answer only from this text. Question: can we charge [describe the cost] to the grant? Give a yes / no / conditional answer, quote the clause that supports it, state any conditions, and say explicitly if the policy does not cover this case. Do not use any knowledge about this donor from outside the text. [paste policy excerpt]
```

Catching the invented rule (the planted trap):
```
Same policy text. Does it allow charging 15% unrestricted overhead on sub-grants? Quote the clause.
```
The pasted excerpt should not contain such a clause. Watch whether the model says "not in source" or invents one.

Combining the two sources:
```
Using (a) the donor policy clause you quoted and (b) the tax provision below, write a one-page eligibility determination: the question, the facts, the donor rule with clause reference, the tax treatment with section reference, the conclusion, and what documentation we must keep. Mark any point where you were uncertain. [paste tax provision]
```

---

## Module 6 — Bank reconciliation, partner transaction sampling & audit prep *(2.5 hrs)*
**Problem:** The bank rec won't balance, three partner ledgers of several hundred lines each have landed, and audit is in three weeks.

**Tools:** GPA (GPA-protected for anything real) for matching, explaining, sampling design, workpapers and memos. Sheet-AI for the reproducible selection formulas. Ledger-AI shown if the organisation has it, for its match suggestions, with its limits pointed out.

### Part A prompts — bank reconciliation

Matching:
```
Here are two lists: the bank statement and our cash book for March. Match them on amount, with a date tolerance of 3 days, and reference where available. Output three tables: matched pairs; items on the bank statement not in the cash book; items in the cash book not on the bank statement. Do not change or merge any amounts. [paste both lists]
```

Classifying and proposing entries:
```
For each unmatched item, classify it as: outstanding payment, deposit in transit, bank charge or interest not yet recorded, bank error, ledger error, or possible duplicate. For each, say what evidence I should check and draft the adjusting journal entry if one is needed. Mark anything you cannot classify from the data alone.
```

Reconciliation statement (participants build it in the sheet; AI drafts the layout):
```
Give me the layout of a bank reconciliation statement starting from the bank balance and from the book balance, listing the adjustments on each side, so the two adjusted balances can be compared. Do not fill in the amounts.
```
Verification: the two adjusted balances must be equal. If not, the matching is wrong somewhere. The duplicate payment is found by checking vouchers, not by the model's opinion.

### Part B prompts — audit sampling of partner transactions

Sampling plan:
```
I am a grants accountant reviewing a partner's quarterly financial report. The ledger has 612 transactions totalling 184,300. The partner is rated medium risk: new to us this year, one minor finding last quarter on missing receipts. I have one working day for the review. Propose a sampling plan: the key-item threshold and why, the sampling approach for items below the threshold (random, stratified, monetary unit, or systematic) and why, the sample size with its rationale, and what I should document. Then show how the plan would change if the partner were high risk.
```
Verification: the model may quote a "standard" sample size or a donor requirement. Ask: "Where does that number come from?" If it cannot cite your donor's expenditure-verification guidance, it is the model's judgement, not a rule.

Stratification:
```
Here is the partner ledger. Group it into these bands: above 5,000; 1,000 to 5,000; below 1,000. For each band give the number of items and the total value. Also list every item that is a cash payment, is dated after 31 March, has a round amount (ends in 000), or has a missing or duplicated voucher reference. [paste ledger]
```

Reproducible selection (prefer the formula route):
```
Write Excel formulas that select a random sample of 30 items from rows 2 to 613 in a way another person can reproduce: a frozen random number column and a rank, with instructions for freezing the values. Then write the formula for a monetary unit sample with a sampling interval, explaining how to choose the random start.
```
If the AI is asked to pick items directly instead, require: "State the method and seed you used so the selection can be reproduced." Then re-run and compare.

Testing workpaper:
```
Create a testing workpaper as a table with one row per sampled item (voucher reference, date, vendor, budget line, amount) and one column per test: supporting document present; approved by authorised person; arithmetically correct; within budget line and period; eligible under donor rules; evidence goods or services received; correctly recorded in ledger. Add columns for result (pass / exception), comment, and follow-up required. Leave the test columns blank.
```

Exceptions summary and follow-up letter:
```
Here are the completed test results for the sample. Summarise: number tested, number of exceptions by type, total value of exceptions, projected error rate for the population if appropriate, and whether the sample should be extended. Then draft a courteous follow-up letter to the partner finance officer listing each exception, the document or explanation needed, and a response deadline. [paste results]
```

Sampling memo:
```
Write a one-page sampling memo for the audit file covering: population and total, key-item threshold, sampling method and sample size with rationale, how the selection was made and can be reproduced, summary of results, conclusion, and reviewer sign-off line.
```

### Part C prompts — anomaly sweep and audit readiness

Anomaly leads:
```
Scan this ledger and list transactions that match any of these patterns: duplicate amount and vendor within 10 days; payment split into two or more amounts just under 5,000 to the same vendor in one week; weekend or public-holiday posting dates; vendors with the same bank account number; round-number cash payments. For each, give the rows and the reason it was flagged. Present these as leads to check, not conclusions. [paste ledger]
```

Audit-readiness checklist:
```
From this grant agreement's audit clause and last year's management letter, draft an audit-readiness checklist grouped by: documents to have ready, reconciliations to complete, open prior-year findings to close, and people to brief. [paste clause and letter excerpt]
```

Management response:
```
Draft a management-response paragraph for this audit finding: acknowledge the finding, state the root cause, state the corrective action with owner and date, and avoid defensive language. [paste finding]
```

---

## Module 7 — Forecasting, cash flow & scenarios *(2 hrs)*
**Problem:** The board wants a six-month cash projection with a base case and a delayed-disbursement case.

**Tools:** GPA for structure, assumption-listing and narrative. Sheet-AI for the formulas. Drivers and figures are the professional's judgement; the AI frames and explains.

**Prompts:**

Model structure:
```
Design a six-month cash-flow projection layout for a non-profit with three grants and one unrestricted income stream. List the rows (opening cash, inflows by source, outflows by category, closing cash, minimum cash buffer) and the assumption each row depends on. Do not fill in numbers.
```

Assumption interrogation:
```
Here are my assumptions for the base case. For each one, say what would have to be true for it to hold, what the main risk is, and what signal would tell me early that it is wrong. [paste assumptions]
```

Scenario construction:
```
Create a "delayed disbursement" scenario: Donor B's tranche of 60,000 due in month 2 arrives in month 5. Show which rows change and how, keeping everything else as in the base case. State the lowest cash point and the month it occurs. [paste base case table]
```
Verification: recompute closing cash for each month in the sheet. Check the lowest point the model states against the sheet.

Board narrative:
```
Write a one-page board note presenting both scenarios: the question, the key assumptions (labelled as management judgement), the base-case runway, the downside runway, the decisions the board is being asked to make, and the triggers for revisiting. Plain language, no jargon.
```

---

## Module 8 — Capstone & AI-use playbook *(3 hrs)*
**Problem (integrative):** A grant closeout with a budget revision, a donor report, a compliance question, and an embedded data-protection trap.

**Tools:** Groups choose. The choice of tool, and especially the recognition that the trap data must not be pasted anywhere, is part of what is assessed.

**Part A:** groups reuse the prompts from Modules 2, 3, 5 and 6. No new prompts are issued; adapting the toolkit is the test. Facilitators watch for:
- the grounding prefix and the self-check suffix being used without being told;
- the trap data being de-identified or kept out;
- every number traced to source before the presentation.

**Part B prompts — the playbook:**

Use-case selection:
```
Here is a list of finance tasks our team does monthly and quarterly. For each, rate: how much time AI could save, how sensitive the data involved is, how easy the output is to verify. Recommend the three to start with and explain why the others should wait. [paste task list]
```

Playbook draft:
```
Using the template below and our three chosen use cases, draft an organisational AI-use playbook: approved use cases with the tool to use, the data red-lines, the human sign-off step for each use case, who owns and monitors AI use, and a simple log format. Keep it to two pages. [paste template from resources/ai-use-playbook-template.md]
```

Sign-off checklist:
```
For each approved use case, write a five-line sign-off checklist the reviewer completes before the AI-assisted output leaves the finance team.
```

---

## Quick reference: tool by module

| Module | Primary tool | Also show if available | Must be protected tier in real use? |
|---|---|---|---|
| 0 | GPA (free) | — | No |
| 1 | GPA | Privacy settings of the free tool vs protected tier | Yes, this is the lesson |
| 2 | GPA | Sheet-AI for formulas | Mostly no (proposal stage) |
| 3 | GPA | — | Yes (actuals are donor-confidential) |
| 4 | Sheet-AI or GPA | Both | Yes if the export is real |
| 5 | Citation-first + GPA | — | No for public law; yes for internal facts |
| 6 | GPA + Sheet-AI | Ledger-AI | Yes (bank and partner data) |
| 7 | GPA | Sheet-AI | Yes (cash position) |
| 8 | Group's choice | — | Assessed |
