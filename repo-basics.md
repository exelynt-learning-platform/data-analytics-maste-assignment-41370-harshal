$content = @'
# Git Repository Basics

## 1. What is Git?

Git is a version control system that tracks changes in project files. It helps developers manage project history and collaborate with others.

## 2. What is the .git folder?

The `.git` folder is created when we initialize a Git repository using `git init`.

It stores important repository information, including commit history, branches, configuration, and tracking information.

## 3. What is git status?

The `git status` command displays the current state of files in the Git repository. It tells us which files are untracked, modified, or staged.

## 4. Three Git File States

**Modified:** A tracked file has been changed, but the changes have not been added to the staging area.

**Staged:** Changes have been added to the staging area using the `git add` command. They are ready for the next commit.

**Committed:** Changes have been saved in the local Git repository history using the `git commit` command.

## 5. Git Status Output

```text
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.txt

nothing added to commit but untracked files present (use "git add" to track)