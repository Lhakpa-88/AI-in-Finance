# Synthetic Datasets

**Real financial, donor, salary, or beneficiary data must never be used in this course.** The course teaches exactly why. All exercises run on realistic-but-fake data you prepare in advance.

## What to prepare
| Module | Dataset needed |
|---|---|
| 0 | Two AI outputs (one correct, one with a wrong total + invented rule) |
| 1 | A fake grant budget containing plausible salaries + a beneficiary list (to practise de-identifying) |
| 2 | A scope of work + staff grade scale + blank donor budget template |
| 3 | A budget-vs-actual table with interesting variances |
| 4 | A deliberately messy ledger/bank export (merged cells, bad dates, duplicates) |
| 5 | A public donor cost-principle excerpt + a local tax provision |
| 6 | A synthetic transaction extract with embedded anomalies |
| 7 | Opening cash position + inflow/outflow assumptions |
| 8 | A mixed capstone brief with a data-protection trap embedded |

## How to build it safely
- Invent names, amounts, and IDs. Keep them realistic (right order of magnitude, plausible donors).
- Base structures on real templates, but never real values.
- Seed the deliberate errors — catching them is the learning.

## What goes in version control
Only **clearly synthetic** datasets, and only if you're certain they contain nothing real. When in doubt, keep them out of the repo and distribute via the shared drive. The `.gitignore` blocks common data extensions as a backstop.
