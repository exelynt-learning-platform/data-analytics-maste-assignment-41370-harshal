# Sales Data Analysis Project

## Project Overview
This project demonstrates a basic sales data analysis workflow using Git and GitHub.

It contains a sample sales dataset and analysis notes to understand sales performance, product performance, and regional performance.

## Project Objectives
- Analyze total sales and profit.
- Identify the highest-performing region.
- Compare product categories.
- Understand sales performance.

## Project Structure
```text
git-data-analysis-project/
├── data/
│   └── sales.csv
├── notes/
│   └── analysis-notes.md
├── .gitignore
└── README.md
```

## Dataset Information
The dataset contains 10 sales records and 9 columns.

Important columns:
- OrderID
- OrderDate
- Region
- Category
- Product
- Quantity
- UnitPrice
- Sales
- Profit

## Setup Instructions
1. Clone this repository from GitHub.
2. Open the project folder.
3. Access sales.csv inside the data folder.
4. Read analysis-notes.md inside the notes folder.

## Tools Used
- Git
- GitHub
- PowerShell
- CSV

## Author
Data Analytics Learner

## Branching and Merging

Created a feature branch named feature/monthly-sales-analysis.

Added monthly sales analysis on the feature branch.

Modified the same analysis heading on the main branch to demonstrate a merge conflict.

## Merge Conflict Explanation

A merge conflict occurred because both main and feature branches modified the same heading in notes/analysis-notes.md.

Git identified the conflicting changes using conflict markers.

I resolved the conflict by combining the required information from both branches and removing all conflict markers.

After resolving the conflict, I staged the file and successfully committed the merge.

## Git Commit History

```text
*   18ca8c4 (HEAD -> main) merge: resolve conflict in sales analysis notes
|\  
| * 3137a0a (feature/monthly-sales-analysis) feat: add monthly sales analysis
* | f87495e docs: update analysis goals on main branch
|/  
* 21dc932 docs: add project overview and setup instructions
* d9221f3 chore: add gitignore for unnecessary files
* 548c501 docs: add initial sales analysis notes
* eac987d data: add sample sales dataset