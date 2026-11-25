# Git Branching and Merging

## 1. Introduction

Git branching allows developers to work on different features independently without affecting the main branch.

A branch is a separate line of development. It helps developers make changes, test new features, and merge completed work into the main branch.

## 2. Create and Switch Between Branches

First, I created a local main branch connected to the remote main branch.

```powershell
git switch --track -c main origin/main
```

Then I created a feature branch and switched to it:

```powershell
git switch -c feature-branch-demo
```

**Terminal output:**

```text
Switched to a new branch 'feature-branch-demo'
```

I checked the available branches using:

```powershell
git branch
```

The output showed that `feature-branch-demo` was my active branch.

## 3. Make Changes and Commit in a Separate Branch

I created a new file named `feature-demo.txt` inside the feature branch.

```powershell
Set-Content feature-demo.txt "This change was created in the feature branch."
```

I checked the file status:

```powershell
git status
```

**Terminal output:**

```text
On branch feature-branch-demo
Untracked files:
        feature-demo.txt

nothing added to commit but untracked files present
```

Then I staged and committed the new file:

```powershell
git add feature-demo.txt
git commit -m "Add feature branch demonstration"
```

**Actual commit output:**

```text
[feature-branch-demo 4629625] Add feature branch demonstration
1 file changed, 1 insertion(+)
create mode 100644 feature-demo.txt
```

This confirms that my changes were committed in the feature branch.

## 4. Merge the Feature Branch into Main

I switched back to the main branch:

```powershell
git switch main
```

I verified the active branch:

```powershell
git branch --show-current
```

**Output:**

```text
main
```

Then I merged the feature branch into main:

```powershell
git merge feature-branch-demo
```

**Actual terminal output:**

```text
Updating 59a978a..4629625
Fast-forward
 feature-demo.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature-demo.txt
```

This was a fast-forward merge because the main branch did not have separate new commits that needed to be combined with the feature branch.

I verified that the file was available after merging:

```powershell
Get-Content feature-demo.txt
```

**Output:**

```text
This change was created in the feature branch.
```

After that, I switched back to my assignment branch and merged the local main branch into it:

```powershell
git switch branching-merging-week1-20
git merge main
```

**Actual merge output:**

```text
Updating 59a978a..4629625
Fast-forward
 feature-demo.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature-demo.txt
```

This brought the completed branching exercise into my assignment branch.

## 5. Understand Merge Conflicts

A merge conflict occurs when Git cannot automatically combine changes from different branches.

For example, suppose two developers work on separate branches and modify the same line of a file differently.

Main branch:

```text
Total Sales = 1000
```

Feature branch:

```text
Total Sales = 2000
```

Git cannot automatically decide which value is correct. Therefore, it reports a merge conflict.

Git displays conflict markers in the affected file:

```text
<<<<<<< HEAD
Total Sales = 1000
=======
Total Sales = 2000
>>>>>>> feature-branch
```

To resolve a merge conflict:

1. Open the file containing the conflict.
2. Decide which changes should be kept.
3. Edit the file with the correct content.
4. Remove the conflict markers.
5. Save the file.
6. Run `git add` on the resolved file.
7. Complete the merge commit if Git requests it.

**Note:** My practical merge in this assignment was successful using a fast-forward merge. I did not encounter an actual merge conflict in this exercise. The example above explains how conflicts can occur.

## 6. Git Commit History

I used the following command to visualize branches and commit history:

```powershell
git log --oneline --graph --decorate --all
```

**Actual terminal output captured after merging:**

```text
*   ede809e (origin/main, origin/HEAD) Merge pull request #12 from exelynt-learning-platform/git-installation-setup-week1-20
|\
| * 99fb06f (origin/git-installation-setup-week1-20, git-installation-setup-week1-20) Complete Git installation and setup assignment
| * bfcfd02 Complete the assignment
|/
| * 4629625 (HEAD -> branching-merging-week1-20, main, feature-branch-demo) Add feature branch demonstration
|/
*   59a978a (origin/branching-merging-week1-20) Merge pull request #11 from exelynt-learning-platform/git-repository-basics-week1-20
```

The graph shows that my local main branch, feature branch, and assignment branch point to commit `4629625`.

## 7. Important Git Commands Learned

| Command | Purpose |
|---|---|
| `git branch` | Lists branches |
| `git switch branch-name` | Switches to an existing branch |
| `git switch -c branch-name` | Creates and switches to a new branch |
| `git add` | Stages changes |
| `git commit` | Records changes |
| `git merge` | Merges another branch |
| `git log --oneline --graph` | Displays commit history as a graph |

## 8. Conclusion

Through this practical assignment, I learned how to create branches, switch between branches, make independent changes, commit those changes, and merge a feature branch into main.

I also learned that merge conflicts occur when Git cannot automatically combine different changes, and that developers must resolve them before completing a merge.

Branching and merging help developers collaborate, manage features independently, and maintain an organized project history.