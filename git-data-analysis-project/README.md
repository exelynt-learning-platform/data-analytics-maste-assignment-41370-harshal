# Sales Data Analysis Project

## 1. Project Overview

This project demonstrates a basic sales data analysis workflow using Git and GitHub.

It contains a sample sales dataset and analysis notes for practising business analysis.

## 2. Project Objectives

- Analyze total sales and profit.
- Compare product categories.
- Identify regional sales performance.
- Understand sales and quantity trends.
- Practise Git and GitHub workflows.

## 3. Repository Structure

```text
git-data-analysis-project/
├── .gitignore
├── README.md
├── data/
│   └── sales.csv
└── notes/
    └── analysis-notes.md
```

## 4. Dataset Information

The sample dataset contains 10 records and 9 columns.

Columns:
- OrderID
- OrderDate
- Region
- Category
- Product
- Quantity
- UnitPrice
- Sales
- Profit

Dataset location: `data/sales.csv`

## 5. Setup Instructions

### Requirements
- Git
- Microsoft Excel or Power BI (optional)
- GitHub account

### Clone the Personal Repository

```powershell
git clone https://github.com/Harshal-78/git-data-analysis-project.git
cd git-data-analysis-project
```

Open `data/sales.csv` using Excel or Power BI.

Read `notes/analysis-notes.md` to understand the initial analysis.

No Python packages are required to open CSV and Markdown files.

## 6. Tools Used

- Git
- GitHub
- PowerShell
- CSV
- Excel / Power BI

## 7. Branching and Merging

Feature branch: `feature/monthly-sales-analysis`

Main branch: `main`

Feature branch commit: `3137a0a`

Main branch commit: `f87495e`

Merge commit: `18ca8c4`

The feature branch was merged into main.

## 8. Merge Conflict Explanation

A genuine content conflict occurred in `notes/analysis-notes.md` because both branches modified the same file.

The main branch contained:
- Total Sales: 224700
- Total Profit: 36300

The feature branch changed the dataset formatting and did not contain these figures.

The final merged version retained the feature branch formatting. The original sales figures were not retained.

### Actual Conflict Evidence

Command executed:

```powershell
git -C "$env:USERPROFILE\git-data-analysis-project-source" show --remerge-diff 18ca8c4 -- notes/analysis-notes.md
```

Actual terminal output:

```text
remerge CONFLICT (content): Merge conflict in notes/analysis-notes.md
```

The merge conflict was resolved and recorded in commit `18ca8c4`.

## 9. Git Commit History

Total commits: 9

```text
* b738d39 (HEAD -> main, origin/main, origin/HEAD) docs: improve sales analysis project README
* f8c4671 docs: document merge conflict and git history
*   18ca8c4 merge: resolve conflict in sales analysis notes
|\
| * 3137a0a (origin/feature/monthly-sales-analysis, feature/monthly-sales-analysis) feat: add monthly sales analysis notes
* | f87495e docs: update analysis goals on main branch
|/
* 21dc932 docs: add project overview and setup instructions
* d9221f3 chore: add gitignore for unnecessary files
* 548c501 docs: add initial sales analysis notes
* eac987d data: add sample sales dataset
```