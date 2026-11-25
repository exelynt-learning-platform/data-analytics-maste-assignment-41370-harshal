# Create and Understand a Git Repository

## 1. Create and Initialize a Repository

A Git repository is a project where Git tracks changes to files over time.

To create a project folder and initialize Git, I can use the following commands:

```powershell
mkdir repo-basics-practice
cd repo-basics-practice
git init
```

- `mkdir` creates a new folder.
- `cd` moves into the project folder.
- `git init` initializes a new Git repository.

After initialization, Git creates a hidden `.git` folder that stores repository information and history.

To check the repository status:

```powershell
git status
```

## 2. Understand the `.git` Folder

The `.git` folder is the hidden folder created when I initialize a Git repository using `git init`.

It stores important information such as commit history, branches, configuration, and tracking information.

If I delete the `.git` folder, I will lose the Git history and tracking information for that repository, although my normal project files will remain.

## 3. Understand Git File States

Git files can be in four important states:

- **Untracked:** A new file that Git is not tracking yet.
- **Modified:** A tracked file that has been changed since the last commit.
- **Staged:** A file that has been selected for the next commit.
- **Committed:** A file whose changes have been saved in the Git history.

## 4. Understand the Git Workflow

Git has three main areas:

1. **Working Directory:** Where I create and edit files.
2. **Staging Area:** Where I prepare changes before committing.
3. **Repository:** Where Git permanently records committed snapshots.

The workflow is:

Working Directory → Staging Area → Repository

Commands used in this workflow:

```powershell
git status
git add index.txt
git status
git commit -m "Add index file"
git status
```

- `git status` shows the current state of my files.
- `git add index.txt` stages the file.
- `git commit -m "Add index file"` saves the staged changes in Git history.

## 5. Conclusion

Git helps me track changes, maintain project history, and restore earlier versions of my work. Understanding the working directory, staging area, repository, and different file states is essential for working with Git.
