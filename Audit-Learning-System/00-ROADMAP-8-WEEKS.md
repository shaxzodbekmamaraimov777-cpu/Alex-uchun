# 8-Week Probation Roadmap

> Your concrete week-by-week plan for the 2-month probation at HLB Tashkent.
> Designed to be done *alongside* your real work, not instead of it.

---

## How this plan works

- **~1.5 to 2 hours of study per workday** (split: morning Excel drill + evening theory).
- **One bigger session on the weekend** (3–4 hours) for catch-up and a mini-project.
- Each week has: a **theme**, **Excel goals**, **ACCA/audit goals**, and a **"prove it" task**.
- The "prove it" task is a small deliverable you could actually show a senior.

> Adjust freely. If work gets busy, protect the **Excel** and **AA** items first — they
> matter most for keeping the job.

---

## Quick overview

| Week | Theme | Excel focus | Knowledge focus |
|------|-------|-------------|-----------------|
| 1 | Survive & set up | Navigation, shortcuts, basic formulas | FA: double entry + the 3 statements |
| 2 | Excel for real work | Cell references, SUMIF, IF, formatting | FA: trial balance, accruals, adjustments |
| 3 | Lookups & reconciliations | VLOOKUP/XLOOKUP, reconciliations | AA: what audit is, the process, evidence |
| 4 | Data & summaries | PivotTables, charts, filtering | AA: risk, materiality, working papers |
| 5 | The audit file | CaseWare/firm software, referencing | FR: key IFRS standards (revenue, leases, PPE) |
| 6 | Analysis & ratios | Analytical procedures in Excel | FR + FM: ratios, interpretation |
| 7 | Costing & performance | Power Query intro, large data | MA + PM: costing, variances, budgets |
| 8 | Polish & certify | Power BI intro, recap | Recap + book a certification exam |

---

## WEEK 1 — Survive & set up

**Mindset:** Your only job this week is to not be lost. Set up your tools and learn the absolute basics.

**Excel goals:**
- Learn to navigate fast: `Ctrl+Arrow`, `Ctrl+Shift+Arrow`, `Ctrl+Home`, freeze panes.
- Basic formulas: `=SUM`, `=AVERAGE`, `=COUNT`, `=A1+B1`, `=A1*B1`.
- Format like a pro: number formatting, borders, column width, cell styles.
- Save/version files properly. Learn the firm's file-naming convention (ask a senior).
- *Reference: `Tools/Excel-for-Auditors.md` sections 1–3.*

**Knowledge goals:**
- `ACCA/01-FA-Financial-Accounting.md`: the accounting equation, debits & credits, the three financial statements (SOFP, SOPL, cash flow) — what each one shows.

**Set-up checklist:**
- [ ] Work laptop, email, and software logins all working.
- [ ] Ask: "Which audit software do we use?" (CaseWare? something else?)
- [ ] Ask: "Where are the file-naming and folder conventions documented?"
- [ ] Ask your buddy/mentor what a typical week looks like.

**Prove-it task:** Build a clean Excel sheet that lists 10 transactions and shows their debit/credit effect on the accounting equation, with totals that balance.

---

## WEEK 2 — Excel for real work

**Excel goals:**
- Relative vs **absolute references** (`$A$1`) — critical, you'll use this constantly.
- `IF`, `SUMIF`, `SUMIFS`, `COUNTIF`, `COUNTIFS`.
- `ROUND`, `ABS`, basic text functions (`LEFT`, `RIGHT`, `TRIM`, `&`).
- Conditional formatting to highlight outliers.
- *Reference: `Tools/Excel-for-Auditors.md` sections 4–5.*

**Knowledge goals:**
- `ACCA/01-FA`: trial balance, accruals & prepayments, depreciation, the journal → ledger → trial balance → statements flow.

**Prove-it task:** Take a messy list of expenses and use `SUMIFS` to summarise total spend by category and month, with conditional formatting flagging anything over a threshold.

---

## WEEK 3 — Lookups & reconciliations

**Excel goals:**
- `VLOOKUP` and the modern `XLOOKUP`. Understand exact vs approximate match.
- `IFERROR` to handle missing matches cleanly.
- Build a **two-list reconciliation** (e.g., does the ledger match the bank?).
- *Reference: `Tools/Excel-for-Auditors.md` section 6 + reconciliation walkthrough.*

**Knowledge goals:**
- `ACCA/06-AA-Audit-and-Assurance.md` sections 1–3: what assurance is, why audits exist, the stages of an audit, types of audit evidence, the assertions.

**Prove-it task:** Reconcile two lists (sales ledger vs cash receipts) and produce a short note listing every difference and a possible reason for each.

---

## WEEK 4 — Data & summaries

**Excel goals:**
- **PivotTables**: build, group, filter, add calculated summaries.
- PivotCharts and basic charts (column, line) for analytical review.
- Slicers and filtering large datasets.
- *Reference: `Tools/Excel-for-Auditors.md` section 7.*

**Knowledge goals:**
- `ACCA/06-AA` sections 4–6: audit risk model, materiality, internal controls, working papers and documentation standards.

**Prove-it task:** Take a year's transaction extract and build a PivotTable dashboard showing monthly trends, then write 3 sentences on what looks unusual and would deserve audit attention.

---

## WEEK 5 — The audit file

**Excel goals:**
- Cross-referencing between worksheets and files (the audit "tickmark" / referencing system).
- Linking workbooks, tracing precedents/dependents, auditing formulas.
- *Reference: `Tools/Excel-for-Auditors.md` section 8.*

**Software goals:**
- `Tools/Other-Software-Tools.md`: learn your firm's audit software basics (CaseWare or similar) — opening an engagement file, leadsheets, referencing, signing off.

**Knowledge goals:**
- `ACCA/04-FR-Financial-Reporting.md` sections 1–4: the IFRS framework, revenue (IFRS 15), PPE (IAS 16), inventories (IAS 2), leases (IFRS 16) at a high level.

**Prove-it task:** Recreate a simple "leadsheet" in Excel for one balance: opening balance, movements, closing balance, with references to supporting evidence.

---

## WEEK 6 — Analysis & ratios

**Excel goals:**
- Build a ratio-analysis template (profitability, liquidity, gearing, efficiency).
- Year-on-year variance % columns; analytical-review style comparisons.
- *Reference: `Tools/Excel-for-Auditors.md` section 9.*

**Knowledge goals:**
- `ACCA/05-FM-Financial-Management.md` (ratios, working capital) + `ACCA/04-FR` interpretation section.

**Prove-it task:** Build a one-page ratio dashboard from a set of accounts and write a short commentary explaining what the ratios suggest and which areas an auditor should probe.

---

## WEEK 7 — Costing & performance

**Excel goals:**
- **Power Query** intro: import, clean, and combine data without manual copy-paste.
- Remove duplicates, split columns, unpivot, merge queries.
- *Reference: `Tools/Other-Software-Tools.md` Power Query section.*

**Knowledge goals:**
- `ACCA/02-MA-Management-Accounting.md` + `ACCA/03-PM-Performance-Management.md`: cost classification, absorption vs marginal costing, budgeting, variance analysis.

**Prove-it task:** Use Power Query to combine 3 monthly files into one clean table, then summarise with a PivotTable.

---

## WEEK 8 — Polish & certify

**Excel goals:**
- **Power BI** intro (optional but impressive): load data, build a simple visual report.
- Full recap: redo your weakest exercises from earlier weeks without notes.

**Knowledge goals:**
- Recap AA + FA (your two most job-relevant papers).
- Skim every ACCA file's summary section.

**Certification goals:**
- Decide on and **book** your first exam (most likely **MOS Excel Associate (MO-210)** — see `Resources/Courses-and-Certifications.md`).
- Register interest with ACCA and discuss firm sponsorship with your manager.

**Prove-it task:** Produce a short "What I learned in probation" one-pager: list the Excel skills, audit concepts, and tools you can now use. This is gold for your end-of-probation review.

---

## Daily rhythm template

| Time | Activity | Minutes |
|------|----------|---------|
| Morning (before work or commute) | Excel drill — one function/skill | 20–30 |
| Lunch | Read one section of the day's ACCA/AA file | 20 |
| Evening | Apply the day's concept to a real task you saw at work + error log | 40–60 |
| Weekend | Mini-project / "prove-it" task + review error log | 3–4 hrs |

---

## End-of-probation self-check

By week 8 you should be able to say *yes* to most of these:

- [ ] I can navigate Excel quickly with shortcuts and build clean, formatted sheets.
- [ ] I'm comfortable with SUMIFS, IF, XLOOKUP/VLOOKUP, IFERROR, and PivotTables.
- [ ] I can perform a basic reconciliation and document the differences.
- [ ] I understand double entry and how the 3 financial statements connect.
- [ ] I can explain what an audit is, what audit evidence is, and what a working paper is.
- [ ] I know the audit risk model and what materiality means.
- [ ] I can find my way around the firm's audit software.
- [ ] I've named key IFRS standards and what they cover.
- [ ] I've booked (or am ready to book) a certification exam.
- [ ] I keep an error log and review it.

> Bring this checklist to your probation review. Showing structured self-development
> is exactly what makes a firm want to keep you and raise your pay.

---

*Next: open `Tools/Excel-for-Auditors.md` and start Week 1.*
