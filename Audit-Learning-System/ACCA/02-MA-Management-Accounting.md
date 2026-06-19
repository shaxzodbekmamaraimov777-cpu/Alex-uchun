# MA — Management Accounting (ACCA Applied Knowledge)

> While FA looks *outward* (statements for investors, banks, tax), MA looks *inward* —
> how managers use numbers to plan, control, and make decisions.

**ACCA level:** Applied Knowledge · **Exam:** on-demand, computer-based, 2 hours, 50% to pass.

---

## Why this matters for your audit job

You'll audit companies that use management-accounting systems to set prices, build
budgets, and value inventory. Understanding costing helps you assess whether
**inventory valuation, cost of sales, and management estimates** are reasonable — all
common audit risk areas.

---

## 1. Cost classification

You must be able to slice costs several ways:

**By behaviour (how cost changes with activity):**
- **Fixed** — stays the same regardless of output (rent, salaries). Per-unit fixed cost *falls* as output rises.
- **Variable** — changes in proportion to output (raw materials). Per-unit stays constant.
- **Semi-variable** — has both a fixed and a variable element (a phone bill: line rental + usage).
- **Stepped fixed** — fixed within a range, then jumps (one supervisor per 10 workers).

**By function:** production, administration, selling & distribution.

**By traceability:**
- **Direct** — directly attributable to a product (direct materials, direct labour).
- **Indirect (overheads)** — can't be traced directly (factory rent, supervisor salary).

**The High-Low method** (splitting semi-variable costs):
```
Variable cost per unit = (Cost at high activity − Cost at low activity)
                         ÷ (High activity − Low activity)
Fixed cost = Total cost − (Variable cost per unit × activity)
```

---

## 2. Absorption vs marginal costing

This is one of the most-tested MA topics.

| | Marginal costing | Absorption costing |
|---|------------------|-------------------|
| Product cost includes | Only **variable** production costs | Variable **+ fixed** production overhead |
| Fixed production cost treated as | Period cost (expensed in full) | Absorbed into units, released as units are sold |
| Inventory valued at | Variable cost only | Full production cost |

**Why profit differs between the two:**
- If **inventory increases** (produce more than you sell), absorption profit > marginal profit (fixed costs are "stored" in inventory).
- If **inventory decreases**, marginal profit > absorption profit.

> Audit link: IFRS requires **absorption costing** for inventory in published accounts.
> If a client values inventory at marginal cost only, it's misstated.

**Overhead absorption rate (OAR):**
```
OAR = Budgeted overheads ÷ Budgeted activity level
(activity = labour hours, machine hours, units, etc.)
```
Over/under-absorption occurs when actual ≠ budget.

---

## 3. Marginal costing & decision-making

**Contribution** is the key concept:
```
Contribution = Sales − Variable costs
Contribution per unit = Selling price − Variable cost per unit
Profit = Total contribution − Fixed costs
```

**Break-even point** (where profit = 0):
```
Break-even (units) = Fixed costs ÷ Contribution per unit
Break-even (revenue) = Fixed costs ÷ Contribution-to-sales ratio
```

**Margin of safety** = how far sales can fall before a loss:
```
Margin of safety = Budgeted sales − Break-even sales
```

**Target profit:**
```
Units needed = (Fixed costs + Target profit) ÷ Contribution per unit
```

**Limiting factor analysis:** when a resource is scarce (e.g. machine hours), rank
products by **contribution per unit of the scarce resource** and make the most profitable first.

---

## 4. Costing techniques

- **Job costing** — cost per individual job/order (e.g. a bespoke audit engagement).
- **Batch costing** — cost per batch, then per unit within the batch.
- **Process costing** — for continuous production; handle work-in-progress with **equivalent units**, plus normal vs abnormal losses.
- **Activity-Based Costing (ABC)** — assign overheads using **cost drivers** rather than a single blanket rate. More accurate when overheads are large and varied.

---

## 5. Budgeting

- **Purpose:** plan, coordinate, communicate, motivate, control, evaluate.
- **Types:** fixed budget (one activity level) vs **flexible budget** (flexed to actual activity for fair comparison).
- **Cash budget** — forecast of cash receipts and payments; flags when financing is needed. *Very relevant to going-concern assessment in audit.*
- **Functional budgets:** sales → production → materials/labour → overheads → master budget.

---

## 6. Standard costing & basic variances

A **standard cost** is a pre-set expected cost per unit. **Variances** compare actual vs standard.

- **Favourable (F):** actual better than standard (lower cost / higher revenue).
- **Adverse (A):** actual worse than standard.

Core variances (covered in more depth in PM):
```
Material price variance = (Standard price − Actual price) × Actual quantity
Material usage variance = (Standard qty for actual output − Actual qty) × Standard price
Labour rate variance    = (Standard rate − Actual rate) × Actual hours
Labour efficiency var.   = (Standard hrs for actual output − Actual hrs) × Standard rate
```

---

## 7. Other MA topics

- **Forecasting** — high-low, linear regression, time series, moving averages.
- **Time value of money basics** — simple/compound interest, discounting (deeper in FM).
- **Performance measurement** — basic ratios and KPIs (deeper in PM).
- **Spreadsheets in MA** — the syllabus explicitly expects you to use Excel for budgets, variances, and forecasts. *This ties directly to your Excel learning.*

---

## 8. How auditors use MA

| MA concept | On the audit |
|------------|--------------|
| Absorption costing | Check inventory is valued correctly under IAS 2. |
| Cash budgets | Evidence for going-concern review. |
| Standard costs/variances | Understand and challenge management's cost data. |
| Break-even / contribution | Assess commercial viability of a struggling client. |
| Overhead absorption | Test whether overheads in inventory are reasonable. |

---

## 9. Self-test questions

1. A product sells for 50, has variable cost of 30, and the company has 100,000 fixed costs. What is the break-even point in units?
2. Why does absorption costing usually give a higher profit than marginal costing when inventory is rising?
3. Split this semi-variable cost with high-low: at 1,000 units cost is 8,000; at 2,000 units cost is 12,000.
4. What is "contribution" and why is it more useful than profit for short-term decisions?

<details>
<summary>Answers</summary>

1. Contribution per unit = 50 − 30 = 20. Break-even = 100,000 ÷ 20 = **5,000 units**.
2. Because some fixed production overhead is carried forward in the value of closing inventory instead of being expensed this period.
3. Variable cost/unit = (12,000 − 8,000) ÷ (2,000 − 1,000) = **4/unit**. Fixed = 8,000 − (4 × 1,000) = **4,000**.
4. Contribution = Sales − Variable costs. It's more useful short-term because fixed costs don't change with the decision, so maximising contribution maximises profit.
</details>

---

## 10. Best free resources for MA

- **OpenTuition** — full free MA lectures and notes.
- **ACCA Global** — MA syllabus, specimen exam, examiner reports.
- **ACCA-X (edX)** — free intro to management accounting.

---

*Next: `03-PM-Performance-Management.md` builds directly on this paper.*
