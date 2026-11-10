# AI for Finance Professionals — Non-Profit Sector

A **20-hour, problem-based learning (PBL)** course that teaches non-profit finance professionals to use AI tools with discipline — accelerating real finance work while protecting data and verifying every output. Designed for in-person or virtual delivery.

> Built for finance officers, accountants, grants-finance managers, and finance/operations directors in NGOs, INGOs, and community organisations.

---

## Why this course exists

Across the non-profit sector, AI use is now near-universal but rarely transformative — a documented "efficiency plateau." In finance specifically, two risks dominate: **hallucinated numbers treated as fact**, and **"shadow AI"** (staff pasting donor, salary, or beneficiary data into free tools with no controls).

This course does not teach "AI in general." It teaches a small set of high-value finance workflows, each with a built-in **verify-before-you-trust** step and a **data-protection reflex** — the "narrow-and-governed" pattern that distinguishes high-impact adopters.

The guiding rule throughout: **AI drafts, the professional signs.**

---

## Repository structure

```
AI-in-Finance/
├── README.md                     ← you are here
├── LICENSE                       ← CC BY 4.0 (curriculum content)
├── .gitignore                    ← keeps real financial data OUT of the repo
├── course-design/
│   ├── course-design.md          ← the full v1.0 course design (master document)
│   └── delivery-methodology.md   ← PBL methodology, cadence, session rhythm, in-person vs virtual
├── modules/
│   ├── module-0-foundations.md
│   ├── module-1-verification-and-data-protection.md
│   ├── module-2-budgets.md
│   ├── module-3-donor-reports.md
│   ├── module-4-excel-data-wrangling.md
│   ├── module-5-compliance-policy.md
│   ├── module-6-reconciliation-audit.md
│   ├── module-7-forecasting-cashflow.md
│   └── module-8-capstone-playbook.md
├── facilitator-guide/
│   ├── README.md                 ← how to run the course
│   ├── preparation-checklist.md
│   ├── tools-and-prompts.md      ← which AI tool + which prompts for each module's problem
│   └── synthetic-data/README.md  ← how to build safe fake datasets (real data never committed)
├── assessment/
│   ├── rubric.md
│   └── portfolio-and-capstone.md
└── resources/
    ├── tool-stack.md             ← recommended tools (verify currency before each cohort)
    ├── ai-use-playbook-template.md
    └── data-red-line-card.md
```

---

## How to use this repo

- **Facilitators:** start with `course-design/course-design.md` for the full picture, then `facilitator-guide/README.md` to run it. Each `modules/*.md` file is a standalone brief you can hand to a co-facilitator.
- **Programme leads:** `course-design/delivery-methodology.md` explains the pedagogy and the three cadence options; `assessment/` covers how competence is evidenced.
- **Participants:** you'll be given the relevant module brief and the resources in `resources/` as you go.

---

## A note on data safety

This repository contains **curriculum only**. No real financial, donor, salary, or beneficiary data belongs here — the course itself teaches why. The `.gitignore` is configured to block common data-file types as a safeguard, and all in-class exercises use **synthetic data** (see `facilitator-guide/synthetic-data/`).

---

## Publishing this to GitHub

This repo is already initialised with git, committed on `main`, and pointed at
`https://github.com/Lhakpa-88/AI-in-Finance`. After signing in to GitHub on your computer
(`gh auth login`, or GitHub Desktop), publish with:

```bash
cd ai-for-finance-professionals
git push -u origin main
```

If the GitHub repo was created with a README or licence already in it, run
`git pull origin main --allow-unrelated-histories` first, then push.

---

## Status & licence

- **Status:** Draft v1.0 (August 2026) — see open questions in `course-design/course-design.md` §10.
- **Licence:** Curriculum content under [CC BY 4.0](LICENSE) by default — attribution required, adaptation encouraged. Change this if your organisation's policy differs.

*Maintained by NAAMII operations. Tool references were verified as of August 2026 and should be re-checked before each delivery, as the AI-tools landscape shifts quarterly.*
