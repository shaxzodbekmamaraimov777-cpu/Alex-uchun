# Excel for Auditors — The Daily Skill

> Excel is the tool you'll touch every working hour. This guide is ordered the way the
> 8-week roadmap uses it: navigation → formulas → lookups → reconciliations → PivotTables
> → audit file techniques → analytics. Practise each section *in Excel*, not just by reading.

> **Practice data:** any messy spreadsheet works. Free practice datasets:
> Maven Analytics Data Playground (mavenanalytics.io/data-playground), Kaggle (kaggle.com/datasets),
> or export a trial balance / transaction list from a demo accounting system.

---

## 1. Navigation & shortcuts (Week 1)

Speed comes from never touching the mouse for routine moves. Learn these until automatic:

| Shortcut | Does |
|----------|------|
| `Ctrl + Arrow` | Jump to the edge of a data region |
| `Ctrl + Shift + Arrow` | Select to the edge of a data region |
| `Ctrl + Home` / `Ctrl + End` | Go to A1 / last used cell |
| `Ctrl + Page Up/Down` | Move between worksheets |
| `Ctrl + C / X / V` | Copy / cut / paste |
| `Ctrl + Z / Y` | Undo / redo |
| `Ctrl + S` | Save (do it constantly) |
| `Ctrl + F / H` | Find / Replace |
| `Alt + =` | AutoSum |
| `Ctrl + ;` | Insert today's date |
| `F2` | Edit the active cell |
| `F4` | Repeat last action / toggle `$` absolute reference |
| `Ctrl + 1` | Format Cells dialog |
| `Alt + E, S` then `V` | Paste Special → Values (kills formulas, keeps numbers) |
| `Ctrl + Shift + L` | Toggle filters |
| `Ctrl + T` | Convert range to a Table |

> **Pro habit:** select a column of numbers and glance at the **status bar** (bottom right)
> — it shows Sum, Average, and Count instantly without writing a formula.

---

## 2. Formatting for clean, reviewable work (Week 1)

Auditors are judged on tidy, professional schedules. Rules of thumb:
- **Inputs** in one colour (e.g. blue), **formulas** in black. Never bury a hard-coded number inside a formula.
- Use **number formatting** (`Ctrl+1`): thousands separators, consistent decimals, brackets for negatives.
- **Freeze panes** (View → Freeze Panes) so headers stay visible.
- Use **borders and shading** sparingly to separate sections and totals.
- Add a clear **header block**: client, year-end, preparer initials, date, purpose, source of data.
- Keep one logical thing per sheet; name your sheet tabs.

---

## 3. Basic formulas (Week 1)

```
=SUM(B2:B20)          add a range
=AVERAGE(B2:B20)      mean
=COUNT(B2:B20)        count numbers
=COUNTA(B2:B20)       count non-empty cells
=MAX(B2:B20) / =MIN   largest / smallest
=B2-C2  =B2*C2  =B2/C2  arithmetic
=ROUND(B2,2)          round to 2 decimals
=ABS(B2)              absolute value (useful for differences)
```

**The golden rule:** never type a number you could reference. If tax is 12%, put 12% in a
labelled cell and reference it. This makes every schedule auditable and easy to update.

---

## 4. Cell references — relative vs absolute (Week 2)

This trips up every beginner. Master it early.

- **Relative** `A1` — moves when you copy the formula down/across.
- **Absolute** `$A$1` — locked; never moves.
- **Mixed** `$A1` (lock column) or `A$1` (lock row).
- Press **`F4`** while editing to cycle: `A1 → $A$1 → A$1 → $A1`.

**Example:** to apply a tax rate in `$F$1` to every row:
```
=E2*$F$1     ← copy this down; E2 changes, $F$1 stays put
```

---

## 5. Logical & conditional functions (Week 2)

```
=IF(B2>1000,"Review","OK")                 simple decision
=IF(AND(B2>0,C2="Open"),"Flag","")          two conditions both true
=IF(OR(B2>1000,C2="Cash"),"Check","")        either condition true
=IFS(B2>1000,"High",B2>500,"Med",TRUE,"Low") multiple tiers (modern Excel)

=SUMIF(Category, "Travel", Amount)           sum where one condition met
=SUMIFS(Amount, Category,"Travel", Month,"Jan")  sum with multiple conditions
=COUNTIF(Status,"Open")                       count matching cells
=COUNTIFS(Region,"North", Status,"Open")      count with multiple conditions
=AVERAGEIF / AVERAGEIFS                        conditional averages
```

**Conditional formatting** (Home → Conditional Formatting): highlight cells over a
threshold, duplicate values, or top/bottom items — perfect for spotting outliers in a
ledger.

---

## 6. Lookups — the auditor's workhorse (Week 3)

You'll constantly match one list to another (e.g. ledger to confirmation).

**XLOOKUP** (modern, best — use if available):
```
=XLOOKUP(lookup_value, lookup_array, return_array, "Not found")
=XLOOKUP(A2, Customers[ID], Customers[Name], "Missing")
```
- Works left or right, exact match by default, has a built-in "if not found" argument.

**VLOOKUP** (older, still everywhere):
```
=VLOOKUP(lookup_value, table_array, col_index_number, FALSE)
=VLOOKUP(A2, $D$2:$F$100, 3, FALSE)   ← FALSE = exact match (almost always use FALSE)
```
- Limitation: only looks **right** of the lookup column.

**INDEX/MATCH** (flexible alternative):
```
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```

**Always wrap lookups in IFERROR** so missing matches read cleanly:
```
=IFERROR(XLOOKUP(A2, IDs, Names), "NOT IN LIST")
```

> **Audit use:** XLOOKUP each item in List A against List B. Anything returning "NOT IN
> LIST" is a difference to investigate — that's a reconciliation in one column.

---

### 6.1 Walkthrough: a two-list reconciliation

Goal: check the sales ledger agrees to cash receipts.

1. Put **Ledger** on Sheet1 (columns: Invoice no., Amount).
2. Put **Receipts** on Sheet2 (Invoice no., Amount received).
3. On the Ledger sheet, add a column:
   ```
   =IFERROR(XLOOKUP(A2, Receipts!A:A, Receipts!B:B), "NO RECEIPT")
   ```
4. Add a **Difference** column: `=B2 - C2` (0 = matched; non-zero = investigate).
5. Filter the Difference column for `<>0` and the "NO RECEIPT" rows.
6. Write a short note: list each difference and a likely reason (timing, error, missing).

That note is a real audit working paper.

---

## 7. PivotTables & charts (Week 4)

PivotTables summarise thousands of rows in seconds — essential for analytical review.

**Build one:**
1. Click in your data → Insert → PivotTable.
2. Drag fields: **Rows** (e.g. Account), **Columns** (e.g. Month), **Values** (e.g. Sum of Amount).
3. Right-click a value → *Summarize Values By* (Sum, Count, Average) or *Show Values As* (% of total, running total).
4. **Group** dates into months/quarters (right-click a date → Group).
5. Add a **Slicer** (PivotTable Analyze → Insert Slicer) for click-to-filter.
6. **Refresh** (`Alt+F5`) whenever source data changes — pivots don't auto-update.

**Charts:** select data → Insert → choose column (comparison), line (trend), or pie
(composition). Use a **PivotChart** to visualise a PivotTable.

> **Audit use:** pivot a year of transactions by month to spot unusual spikes; pivot by
> user/approver to test segregation of duties; pivot by account to build a leadsheet.

---

## 8. Audit file techniques: referencing & formula auditing (Week 5)

- **Linking sheets/files:** `=Sheet2!B5` or `='[Workbook.xlsx]Sheet1'!B5`. Lets a leadsheet pull from supporting schedules.
- **Trace Precedents / Dependents** (Formulas tab): visually see which cells feed a formula and which depend on it — great for understanding inherited files.
- **Show Formulas** (`Ctrl + ` `` ` ``): display all formulas at once to review logic.
- **Evaluate Formula** (Formulas tab): step through a complex formula to find an error.
- **Tick marks & cross-references:** use a consistent column for tick marks (e.g. "✓ agreed to invoice", "Ø recomputed") and reference supporting papers (e.g. "see B3.2"). This mirrors how audit software works.
- **Name ranges** (Formulas → Define Name) to make formulas readable: `=SUM(Sales)` instead of `=SUM(B2:B500)`.

---

### 8.1 Walkthrough: a leadsheet

A leadsheet summarises a balance and ties to the trial balance.
```
Account: Trade receivables          Ref: C1
Opening balance (PY)        120,000   [agreed to PY file]
+ Movements / additions      30,000   [per schedule C1.1]
− Receipts / write-offs    (25,000)   [per schedule C1.2]
= Closing balance           125,000   [agreed to TB ✓]
```
Each figure references a supporting schedule; the closing balance agrees to the trial
balance. That's the structure of nearly every audit working paper.

---

## 9. Analytical procedures & ratios in Excel (Week 6)

Build a reusable comparison template:

| Ratio | Formula in Excel |
|-------|------------------|
| Gross margin % | `=Gross_profit / Revenue` |
| Operating margin % | `=Operating_profit / Revenue` |
| ROCE | `=Operating_profit / Capital_employed` |
| Current ratio | `=Current_assets / Current_liabilities` |
| Quick ratio | `=(Current_assets - Inventory) / Current_liabilities` |
| Receivables days | `=Receivables / Revenue * 365` |
| Inventory days | `=Inventory / COS * 365` |
| Gearing | `=Debt / Equity` |
| YoY change % | `=(This_year - Last_year) / Last_year` |

Put **this year** and **last year** side by side, add a **% change** column, and apply
conditional formatting to flag big swings. Then write a sentence per significant movement
— that's an analytical review working paper.

---

## 10. Data cleaning toolkit (used across all weeks)

Real ledgers are messy. These fix common problems:
```
=TRIM(A2)             remove extra spaces
=CLEAN(A2)            remove non-printing characters
=UPPER/LOWER/PROPER   standardise case
=LEFT(A2,3) =RIGHT =MID    extract parts of text
=TEXT(A2,"DD/MM/YYYY")     format a date as text
=VALUE(A2)            convert text-number to a real number
=A2&" "&B2            join text (concatenate)
=TEXTSPLIT / Text to Columns   split one column into many
Remove Duplicates (Data tab)   dedupe a list
Data → Data Validation         restrict/standardise inputs
```

> **Tip:** text that won't sum is usually "numbers stored as text". Look for a green
> triangle in the cell corner; use `VALUE()` or Text-to-Columns to fix.

---

## 11. Common beginner mistakes (avoid these)

- Hard-coding numbers inside formulas → impossible to review or update.
- Forgetting `$` absolute references → totals break when copied.
- `VLOOKUP` with `TRUE`/approximate match by accident → wrong matches. Use `FALSE`.
- Not refreshing PivotTables after data changes.
- Overwriting the original client data — always keep an untouched copy.
- No header block → reviewer can't tell what the sheet is or where data came from.
- Merged cells everywhere → break sorting, filtering, and formulas. Avoid them.

---

## 12. Practice plan (do these to actually get good)

1. **Week 1–2:** rebuild a trial balance; total it with `SUM`; categorise with `SUMIFS`.
2. **Week 3:** do the two-list reconciliation in §6.1 from scratch, no notes.
3. **Week 4:** take a 1,000+ row dataset and build a 3-field PivotTable + chart.
4. **Week 5:** build the leadsheet in §8.1 with cross-references between sheets.
5. **Week 6:** build the ratio template in §9 from a set of accounts and write commentary.
6. **Week 7:** clean a messy file using §10 tools, then summarise it.

See `Resources/Practice-Exercises.md` for fuller drills, and
`Resources/Courses-and-Certifications.md` for the **MOS Excel certification** path.

---

## 13. Best free Excel learning resources

- **Microsoft Learn — Excel** (learn.microsoft.com) — official, free, includes MOS exam skills.
- **ExcelJet** (exceljet.net) — concise function references and shortcut cheat sheets.
- **Chandoo** (chandoo.org) — practical Excel for analysts and finance.
- **Leila Gharani / ExcelIsFun** (YouTube) — excellent free video tutorials.
- **Excel Exposure**, **GCFGlobal Excel** (edu.gcfglobal.org) — free structured courses.
- **Maven Analytics Data Playground** — free datasets to practise on.

---

*Next: `Other-Software-Tools.md` for audit software, Power Query/BI, Word, PowerPoint, and PDF tools.*
