# Other Software Tools for Auditors

> Excel is your hammer, but auditors use a whole toolbox. This covers the audit-specific
> software, the data tools that make you stand out, and the everyday Office apps you'll
> use to communicate. Learn the *concepts* here; learn the *exact buttons* on whatever
> version HLB Tashkent uses.

---

## 1. Audit engagement software (the system you'll live in)

Modern firms manage each audit inside dedicated software rather than loose Excel files.
The most common in firms like HLB:

### CaseWare (Working Papers / IDEA / Cloud)
The market-leading audit & assurance platform. It holds the whole engagement file:
- **Working Papers** — the electronic audit file: trial balance import, automatic
  leadsheets, working-paper referencing, sign-off, and review notes.
- **CaseWare IDEA** — data-analytics tool for interrogating large datasets (extract,
  sample, find duplicates/gaps, Benford's Law tests).
- Newer AI-assisted workflows (e.g. CaseWare's Verity platform) are being adopted across
  the industry to automate risk assessment and testing.

**What an intern actually does in it:** open the engagement file, import/agree the trial
balance, complete assigned working papers, attach evidence, cross-reference, and clear
review points raised by seniors.

> *Content rephrased from public CaseWare announcements for licensing compliance.*
> Source: [CaseWare press releases](https://www.caseware.com).

### Other platforms you may meet
- **AICPA Dynamic Assurance Solution (DAS)** — connected, data-driven audit workflow.
- **TeamMate+** (Wolters Kluwer) — common for internal audit.
- **MyWorkpapers**, **Inflo**, **AuditBoard**, **Pentana** — engagement/analytics tools.
- **CCH / ProSystem fx**, **Karbon**, **Onvio** — practice management and workflow.

> **Action:** in Week 1, ask your senior *"Which engagement software do we use, and is
> there a training environment or e-learning I can practise in?"* Most vendors have free
> learning portals (e.g. CaseWare's learning site) and most firms have internal training.

---

## 2. Data analytics tools (these make you stand out)

Audit is becoming data-driven. Even basic skills here impress seniors.

### Power Query (built into Excel — learn this first, it's free)
The best entry point to "real" data work. It **imports, cleans, and combines** data
without manual copy-paste, and **remembers the steps** so you can refresh in one click.

Core skills:
- **Get Data** from Excel, CSV, folder, or database.
- **Remove/keep columns and rows**, filter, sort.
- **Remove duplicates**, split columns, change data types.
- **Unpivot** messy "wide" data into a clean table.
- **Merge** queries (like a JOIN — combine two tables on a key).
- **Append** queries (stack multiple files, e.g. 12 monthly files into one).
- **Refresh** to re-run everything when source data updates.

> **Audit use:** combine a year of monthly transaction exports into one clean table for
> testing; reconcile two systems; standardise a messy client extract.

### Power BI (impressive, optional for an intern)
Microsoft's dashboarding tool. Loads data (often via Power Query), builds relationships,
and creates interactive visual reports. Useful for analytical review and presenting trends
to a manager. Free **Power BI Desktop** download to practise.

### CaseWare IDEA / ACL (Galvanize / Diligent)
Specialist audit data-analytics tools. They test entire populations (not just samples):
duplicate payments, gaps in invoice sequences, weekend/round-sum transactions, and
**Benford's Law** anomaly detection. You'll likely use these once trained.

### SQL (a strong bonus skill)
Basic `SELECT … FROM … WHERE … GROUP BY` lets you query databases directly. Not essential
day one, but increasingly valued. Free practice at SQLBolt, Mode SQL tutorial, or W3Schools.

---

## 3. Microsoft Word (audit reports, letters, documentation)

You'll prepare and edit formal documents: engagement letters, management letters, the
audit report, and file memos. Skills that matter:
- **Styles & headings** for consistent, navigable documents.
- **Track Changes & Comments** — essential for review cycles with seniors.
- **Templates** — firms have standard report/letter templates; learn to use, not break, them.
- **Tables, cross-references, table of contents, headers/footers, page numbering.**
- **Mail merge** for confirmation letters (e.g. receivables circularisation).

> **Certification:** Word has its own MOS exam (MO-110 Associate) — see the certifications file.

---

## 4. Microsoft PowerPoint (presenting findings)

Used for audit closing meetings, summaries to management, and internal updates.
- Clean **slide layouts** and master slides for consistency.
- Turn Excel charts/tables into clear visuals (paste linked so they update).
- Keep it simple: one message per slide, minimal text, readable numbers.
- **Certification:** MOS PowerPoint exam (MO-310 Associate).

---

## 5. Microsoft Outlook & professional email

Underrated but vital as an intern:
- Clear, concise, professional emails (subject line, ask, deadline).
- **Calendar** management for engagement scheduling.
- Folders/rules to organise client correspondence (which becomes audit evidence).
- Always be mindful of **confidentiality** — client data must not leave secure channels.

---

## 6. PDF tools (Adobe Acrobat / alternatives)

Much audit evidence arrives as PDF (invoices, contracts, bank statements):
- Search, annotate, and bookmark PDFs.
- Combine/split documents; extract pages for the audit file.
- Use **OCR** to make scanned documents searchable.
- Convert PDF tables to Excel (Acrobat export, or Excel's *Data → From PDF*).

---

## 7. Accounting systems you'll encounter at clients

You'll extract data from clients' bookkeeping systems. Useful to recognise:
- **1C** (very common in Uzbekistan / CIS region), **SAP**, **Oracle NetSuite**,
  **Microsoft Dynamics**, **QuickBooks**, **Xero**, **Sage**.
- You don't need to operate them, but learn to **export a trial balance and a transaction
  listing** (usually to Excel/CSV) — that's the raw material for your testing.

---

## 8. Collaboration & file management

- **SharePoint / OneDrive / Teams** — shared files, co-authoring, version history.
- **Folder discipline & file naming** — follow the firm's convention exactly; a tidy file
  is reviewable and audit-trail friendly.
- **Document retention & security** — audit files have legal retention requirements; never
  store client data on personal devices or send it outside approved systems.

---

## 9. AI tools in audit (use carefully)

The profession is adopting AI for risk assessment, document review, and analytics
(e.g. CaseWare Verity, Thomson Reuters tools). As an intern:
- Great for explaining a concept, drafting a first version of a memo, or summarising a standard.
- **Never** paste confidential client data into public AI tools — it breaches confidentiality.
- **Always** verify AI output against the source — it can be confidently wrong.
- Follow the firm's AI policy; ask before using any tool on real engagement data.

---

## 10. Priority order for an intern

| Priority | Tool | Why |
|----------|------|-----|
| 1 | **Excel** | Daily, everything. (see `Excel-for-Auditors.md`) |
| 2 | **Firm's audit software** (CaseWare etc.) | You work inside it. |
| 3 | **Word / Outlook** | Reports, letters, communication. |
| 4 | **Power Query** | Easy win, big productivity gain. |
| 5 | **PowerPoint** | Presenting findings. |
| 6 | **Power BI / IDEA / SQL** | Stand-out analytics skills, learn over time. |

---

## 11. Free learning resources

- **Microsoft Learn** (learn.microsoft.com) — free official training for Excel, Word, PowerPoint, Power BI, Power Query.
- **CaseWare learning portal** + your firm's internal training — for the engagement software.
- **YouTube:** Leila Gharani, Kevin Stratvert (Office apps), Guy in a Cube (Power BI).
- **SQLBolt / Mode SQL tutorial** — free interactive SQL.
- **GCFGlobal** (edu.gcfglobal.org) — free beginner courses for all Office apps.

---

*Next: `Resources/Courses-and-Certifications.md` — where to get officially certified with real exams.*
