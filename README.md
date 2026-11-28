# Collaborating on GitHub and Following Best Practices

## 1. Project Overview

This repository is part of my Git and GitHub learning assignment. It documents the essential concepts of version control, repository management, remote collaboration, and Git best practices.

The main purpose of this project is to understand how developers manage project files, track changes, collaborate with others, and maintain a clean and organized repository.

## 2. Learning Objectives

Through this project, I am learning how to:

- Understand Git and version control.
- Create and manage local and remote repositories.
- Stage, commit, and push changes.
- Work with branches.
- Understand GitHub Issues and Pull Requests.
- Follow best practices for data analytics projects.
- Organize project files and documentation.

## 3. Repository Structure

The repository is organized to keep documentation easy to find.

## Repository Structure

git-assignment-course/
│
├── .gitignore
├── README.md
├── SETUP.md
├── repo-basics.md
│
├── docs/
│   ├── commits.md
│   ├── github-setup.md
│   ├── learning-notes.md
│   ├── push-practice.md
│   ├── remote-workflow.md
│   └── tracking-changes.md
│
└── git-data-analysis-project/
    ├── .gitignore
    ├── README.md
    ├── data/
    │   └── sales.csv
    └── notes/
        └── analysis-notes.md

### File descriptions

- `README.md`: Project overview, setup instructions, GitHub collaboration concepts, and best practices.
- `.gitignore`: Lists files and folders that should not be tracked by Git.
- `docs/commits.md`: Notes about staging, commits, and common Git mistakes.
- `docs/github-setup.md`: Notes about connecting local and remote repositories.
- `docs/learning-notes.md`: General Git and GitHub learning notes.
- `docs/push-practice.md`: Notes about pushing changes to GitHub.

## 4. Requirements and Setup

### Requirements

- Git installed on the computer.
- A GitHub account.
- A code editor such as Visual Studio Code.
- Basic knowledge of command-line commands.

### Clone the repository

```bash
git clone <repository-url>
```

Move into the project folder:

```bash
cd git-assignment-course
```

Check the repository status:

```bash
git status
```

Check the configured remote repository:

```bash
git remote -v
```

## 5. How to Use This Repository

This is a documentation and practice repository. Read the Markdown files in the `docs/` folder to understand the concepts and commands.

Practice Git commands in the terminal and check the results using:

```bash
git status
git log --oneline
git branch
```

## 6. Understanding GitHub Issues

GitHub Issues are used to report problems, suggest improvements, ask questions, and track tasks in a repository.

For example, an issue in this project could be:

**Issue title:** Improve GitHub documentation

**Description:**
The repository documentation needs improvement. The README should explain the project, GitHub Issues, Pull Requests, and Git best practices.

### How to create an Issue

1. Open the repository on GitHub.
2. Select the **Issues** tab.
3. Click **New issue**.
4. Add a meaningful title and description.
5. Submit the issue.

Issues help developers organize work and track tasks until they are completed.

## 7. Understanding Pull Requests

A Pull Request (PR) is used to propose changes from one branch to another branch.

It allows team members to review changes, discuss improvements, and approve code before merging it into the target branch.

### Typical Pull Request workflow

1. Create a feature branch.
2. Make changes to project files.
3. Stage and commit the changes.
4. Push the feature branch to GitHub.
5. Open a Pull Request.
6. Review the changes.
7. Merge the Pull Request into the target branch.

### Example commands

```bash
git switch -c feature/update-documentation

git add README.md

git commit -m "docs: improve project documentation"

git push -u origin feature/update-documentation
```

After pushing, open GitHub, select **Pull Requests**, and create a Pull Request from the feature branch into the target branch.

## 8. Git Best Practices for Data Analytics Projects

Following good Git practices keeps a project safe, organized, and easy to maintain.

1. **Use feature branches:** Create a separate branch for each new feature, task, or improvement instead of making every change directly on the main branch.

2. **Make small and meaningful commits:** Commit related changes with clear messages so that the project history is easy to understand.

3. **Never commit passwords or secrets:** Keep API keys, passwords, database credentials, and private tokens out of the repository. Store sensitive values in environment variables or `.env` files, and ignore those files using `.gitignore`.

4. **Avoid uploading large datasets:** Do not commit huge raw datasets or unnecessary files. Use appropriate storage for large data and keep generated or raw files out of Git when they are not required.

5. **Clear notebook outputs:** Remove unnecessary outputs from Jupyter notebooks before committing them to keep files clean and reduce repository size.

6. **Use a `.gitignore` file:** Exclude temporary files, virtual environments, checkpoints, secrets, and large data files.

7. **Review changes before committing:** Use `git status` and `git diff` to check which files have changed.

8. **Write clear commit messages:** Use messages that explain the purpose of the change, such as `docs: add GitHub workflow explanation`.

9. **Review Pull Requests:** Check the changes before merging them into the target branch.

10. **Keep documentation updated:** Update the README and relevant notes whenever the repository structure or workflow changes.

## 9. Common Git Commands

| Command | Purpose |
|---|---|
| `git status` | Check the working tree status |
| `git add .` | Stage changes |
| `git commit -m "message"` | Save changes in Git history |
| `git push` | Upload commits to a remote repository |
| `git pull` | Download and integrate remote changes |
| `git branch` | List local branches |
| `git switch -c branch-name` | Create and switch to a new branch |
| `git log --oneline` | View a short commit history |
| `git remote -v` | View remote repository URLs |

## 10. Conclusion

This project helps me understand how Git and GitHub are used in real development workflows. I have learned about version control, commits, remote repositories, and repository management.

I am also learning how Issues and Pull Requests support collaboration and how Git best practices help maintain clean, secure, and organized data analytics projects.


## 11. Using the Sales Data Analysis Project

The repository includes a practical Sales Data Analysis project in the `git-data-analysis-project/` folder.

### Project Files

- `data/sales.csv` – Sample sales dataset.
- `notes/analysis-notes.md` – Sales analysis notes and findings.
- `README.md` – Project overview and setup information.
- `.gitignore` – Files and folders excluded from Git tracking.

### How to Use the Project

1. Open the `git-data-analysis-project/` folder.
2. Open `data/sales.csv` using Excel, Python, or another data analysis tool.
3. Read `notes/analysis-notes.md` to understand the initial analysis.
4. Practise calculating sales, profit, and other business KPIs.
5. Create visualizations and dashboards using Power BI or Python.

### Project Repository

Personal GitHub repository:

https://github.com/Harshal-78/git-data-analysis-project

## 12. Git Commit History

The following graph shows the actual commit history, including the feature branch and merge.

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
