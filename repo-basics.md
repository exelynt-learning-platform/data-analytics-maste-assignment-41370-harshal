# Create and Understand a Git Repository

## 1. Create and Initialize a Repository

A Git repository is a project where Git tracks and stores changes to files over time.

The following commands are used to create a project folder and initialize Git:

```powershell
mkdir repo-basics-practice
cd repo-basics-practice
git init
```

I initialized my existing assignment repository using:

```powershell
git init
```

**Actual terminal output:**

```text
Reinitialized existing Git repository in C:/Users/Genius Computer/OneDrive/git-assignment-course/.git/
```

This confirms that Git recognized and reinitialized the existing repository.

## 2. Identify and Understand the .git Folder

The `.git` folder is a hidden folder automatically created when Git initializes a repository.

It stores important repository information, including commit history, branches, configuration, and tracking information.

I used the following PowerShell command to identify hidden files and folders:

```powershell
Get-ChildItem -Force | Select-Object Mode, Name
```

**Actual terminal output:**

```text
Mode   Name
darh-l .git
dar--l docs
-a---l .gitignore
-a---l commits.md
-a---l git
-a---l github-setup.md
-a---l index.txt
-a---l learning-notes.md
-a---l push-practice.md
-a---l README.md
-a---l repo-basics.md
-a---l Tracking
-a---l untracked-demo.txt
```

The output confirms that the `.git` folder exists in my project.

Deleting the `.git` folder removes Git's tracking information and repository history, but does not normally delete my other project files.

## 3. Understand the Three Git File States

Git has three important states in its file workflow:

**1. Modified**

A tracked file becomes modified when I change its contents after the previous commit.

**2. Staged**

A modified file becomes staged when I use `git add`. It is prepared for the next commit.

**3. Committed**

A staged file becomes committed when I use `git commit`. The changes are recorded in the Git repository history.

**Note about untracked files:**

An untracked file is a newly created file that Git has not started tracking. It is separate from the three main states of the tracked-file workflow.

## 4. Demonstrate Git File States Using git status

I created a new file and added content to demonstrate the different Git file states.

```powershell
Set-Content index.txt "This file demonstrates Git file states."
Set-Content untracked-demo.txt "This is a new file not yet tracked by Git."
git status
```

**Actual terminal output showing modified and untracked files:**

```text
On branch git-repository-basics-week1-20
Your branch is up to date with 'origin/git-repository-basics-week1-20'.

Changes not staged for commit:
        modified:   index.txt

Untracked files:
        untracked-demo.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

The output shows that `index.txt` is modified and `untracked-demo.txt` is untracked.

### Stage the files

I used `git add` to prepare both files for committing.

```powershell
git add index.txt untracked-demo.txt
git status
```

**Actual terminal output showing staged files:**

```text
On branch git-repository-basics-week1-20
Your branch is up to date with 'origin/git-repository-basics-week1-20'.

Changes to be committed:
        modified:   index.txt
        new file:   untracked-demo.txt
```

Both files are now in the staging area.

### Commit the files

I used the following command to save the staged changes:

```powershell
git commit -m "Add Git file state examples"
```

**Actual terminal output:**

```text
[git-repository-basics-week1-20 2fd9ca2] Add Git file state examples
 2 files changed, 2 insertions(+)
 create mode 100644 untracked-demo.txt
```

The commit was successful, and Git recorded the changes in repository history.

### Check the final repository status

```powershell
git status
```

**Actual terminal output:**

```text
On branch git-repository-basics-week1-20
Your branch is ahead of 'origin/git-repository-basics-week1-20' by 1 commit.

nothing to commit, working tree clean
```

This confirms that there are no remaining uncommitted changes.

## 5. Understand the Git Workflow

Git has three main areas:

1. Working Directory – Where I create and modify files.
2. Staging Area – Where I prepare changes for the next commit.
3. Repository – Where committed changes are stored in Git history.

The Git workflow is:

Working Directory → Staging Area → Repository

Important commands:

- `git status` – Checks the current status of files.
- `git add` – Moves changes to the staging area.
- `git commit` – Saves staged changes in repository history.
- `git log` – Displays previous commits.
- `git init` – Initializes a Git repository.

## 6. Conclusion

Through this practical exercise, I learned how to initialize a Git repository, identify the hidden `.git` folder, understand Git file states, and use `git status`, `git add`, and `git commit`.

Git helps developers track project changes, maintain version history, and manage their work efficiently.
