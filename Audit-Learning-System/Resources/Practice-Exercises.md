# Practice Exercises — Turn Knowledge into Skill

> Reading teaches you *about* auditing. Doing makes you *able* to audit. Work through these
> drills and mini-projects. Each maps to a roadmap week and a system file. Do them in real
> Excel with real-ish data.

> **Get practice data:** Maven Analytics Data Playground (mavenanalytics.io/data-playground),
> Kaggle datasets (kaggle.com/datasets), or build small datasets yourself (even 20–50 rows
> is enough to learn the technique).

---

## How to use these

1. Read the linked system file section first.
2. Attempt the exercise **without** looking at notes.
3. Check yourself against the "Done right when…" criteria.
4. Log any struggle in your **error log** and redo it the next week.

---

## A. Excel drills (do daily — 20–30 min each)

### A1. Navigation race (Week 1 · Excel §1)
Open any large dataset. Using **only the keyboard**:
- Jump to the last row of data, select the whole used range, jump back to A1.
- **Done right when:** you do it in under 10 seconds without the mouse.

### A2. Formatting a schedule (Week 1 · Excel §2)
Take a raw list of 20 transactions. Add a proper header block (client, year-end, preparer,
date, purpose, data source), format numbers with separators and bracketed negatives,
freeze the header row, and total the amounts.
- **Done right when:** a stranger could understand what the sheet is and where the data came from.

### A3. SUMIFS summary (Week 2 · Excel §5)
From a list of expenses (Category, Month, Amount), build a summary table of total spend
by category and by month using `SUMIFS`. Add conditional formatting to flag any single
expense over a threshold you choose.
- **Done right when:** the summary totals tie back to the grand total of the raw data.

### A4. Lookup matching (Week 3 · Excel §6)
Given two lists (a master price list and a sales list), use `XLOOKUP` (or VLOOKUP) wrapped
in `IFERROR` to pull the standard price onto each sale, then compute the expected revenue
and compare to actual.
- **Done right when:** unmatched items clearly read "NOT IN LIST" and you can explain each.

### A5. PivotTable dashboard (Week 4 · Excel §7)
From 500+ transaction rows, build a PivotTable of amount by account by month, group dates
into quarters, add a slicer, and insert a line PivotChart of the monthly trend.
- **Done right when:** you can answer "which month had the biggest spike and in which account?" in 5 seconds.

### A6. Data cleaning (Week 7 · Excel §10)
Take a deliberately messy list (mixed case, extra spaces, numbers stored as text,
duplicates). Clean it with `TRIM`, `PROPER`, `VALUE`, Text-to-Columns, and Remove Duplicates.
- **Done right when:** the cleaned column sums correctly and has no duplicates.

---

## B. Audit working-paper mini-projects (weekend tasks)

### B1. Accounting equation tracker (Week 1 · FA §1–2)
Build a sheet listing 10–15 business transactions. For each, show the debit, the credit,
and the effect on Assets / Liabilities / Equity. Add totals that prove the equation balances.
- **Done right when:** total assets = total liabilities + equity after every transaction.

### B2. Bank reconciliation (Week 3 · FA §6 · Excel §6.1)
You have a cash book balance and a bank statement balance that differ. Create a reconciliation
identifying unpresented cheques, outstanding lodgements, and bank charges to explain the gap.
- **Done right when:** the reconciled cash book and bank balances agree, with each difference labelled.

### B3. Two-list reconciliation (Week 3 · Excel §6.1 · AA §3)
Reconcile a sales ledger to a list of cash receipts. Produce a difference column and a short
written note listing every difference with a likely cause (timing, error, missing item).
- **Done right when:** every non-zero difference has an explanation — that's a real working paper.

### B4. Receivables circularisation simulation (Week 4 · AA §10)
You have a list of customer balances. Select a sample (say the 5 largest + 5 random),
document *why* you chose them, and draft the columns you'd track: balance per ledger,
amount confirmed, difference, follow-up.
- **Done right when:** your sampling rationale is written down and the schedule is review-ready.

### B5. Leadsheet (Week 5 · Excel §8.1 · AA §8)
Build a leadsheet for one balance (e.g. trade receivables): opening balance, movements,
closing balance — each figure cross-referenced to a supporting schedule, closing balance
agreeing to a trial balance figure.
- **Done right when:** every number references its source and the closing balance ties to the TB.

### B6. Analytical review (Week 6 · Excel §9 · FR §5 · PM §5)
From two years of summarised accounts, build a ratio table (margins, current ratio,
receivables days, gearing) with a % change column. Write one sentence per significant
movement explaining what it suggests and what an auditor should investigate.
- **Done right when:** you've flagged the 3 biggest changes and proposed a procedure for each.

### B7. Variance analysis (Week 7 · MA §6 · PM §4)
Given budgeted and actual figures for materials and labour, calculate the price/rate and
usage/efficiency variances, label each Favourable or Adverse, and write a short note on the
likely business reason and how variances might be linked.
- **Done right when:** variances reconcile budget to actual and your explanations are plausible.

### B8. Power Query consolidation (Week 7 · Tools §2)
Combine three monthly transaction files into one clean table using Power Query's *append*,
remove duplicates, fix data types, then summarise with a PivotTable. Refresh after editing
a source file to prove it updates.
- **Done right when:** one refresh rebuilds the whole combined summary with no manual steps.

---

## C. Knowledge self-tests (use the ACCA files)

Each ACCA file ends with self-test questions and answers. Schedule:

| Week | File | Section to drill |
|------|------|------------------|
| 1–2 | 01-FA | Self-test §9; redo until 5/5 |
| 3–4 | 06-AA | Self-test §16; the audit risk model and report opinions table |
| 5 | 04-FR | Self-test §7; name 8 IFRS standards and what each covers |
| 6 | 05-FM | Self-test §8; the cash cycle and NPV calculation |
| 7 | 02-MA / 03-PM | Self-tests; break-even and variances |

**Active recall technique:** cover the answers, write your response, then check. Re-do any
you got wrong after 2 days, then after a week (spaced repetition).

---

## D. On-the-job application (the most valuable practice)

Every real task you're given at HLB is the best exercise there is. For each one:
1. **Name it:** which system file/section covers this? (e.g. "this is an existence test on PPE → AA §10").
2. **Read** that section the same evening.
3. **Do it well** in Excel/the audit software using the techniques you've learned.
4. **Log** anything a senior corrects, and review your log weekly.

> This loop — real task → relevant theory → clean execution → error log — is what turns an
> intern into someone the firm wants to keep and pay more.

---

## E. Weekly review ritual (15 minutes, every Friday)

- [ ] Which 3 things did I learn this week?
- [ ] Which exercise/task did I struggle with? (→ redo next week)
- [ ] What did a senior correct? (→ add to error log)
- [ ] What's my focus for next week (per the roadmap)?
- [ ] Am I on track for my certification timeline?

---

## F. Mock-exam practice (for ACCA & MOS)

- **ACCA:** do the **specimen exams** on accaglobal.com and OpenTuition mocks under timed
  conditions. Review examiner reports for common mistakes.
- **MOS Excel:** use **GMetrix** practice tests; aim to finish each project task quickly
  and accurately, mirroring the live test format.

---

*You now have the full system. Start with `00-ROADMAP-8-WEEKS.md`, Week 1 — and do exercise
A1 today.*
