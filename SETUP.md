# Git Setup and Understanding the Git Environment

## 1. Git Installation and Verification

Git is a distributed version control system that helps developers track changes in project files.

I am using Windows, so I installed Git for Windows and use Windows PowerShell to execute Git commands.

I verified the Git installation using:

```powershell
git --version
```

**Actual terminal output:**

```text
git version 2.56.1.windows.1
```

This confirms that Git is installed and working correctly on my computer.

## 2. Configure Global Username and Email

Git uses a username and email address to identify the author of commits.

I configured my global Git username and email using:

```powershell
git config --global user.name "Harshal Mahajan"
git config --global user.email "harshalmahajanji143@gmail.com"
```

I verified the global configuration using:

```powershell
git config --global --list
```

**Actual terminal output:**

```text
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=Harshal Mahajan
user.email = harshalmahajanji143@gmail.com
```

The output confirms that my Git username and email are configured globally.

## 3. Demonstrate Basic Terminal Commands

I used Windows PowerShell to practice basic terminal commands.

### Command 1: pwd

The `pwd` command displays the current working directory.

**Command:**

```powershell
pwd
```

**Actual terminal output:**

```text
Path
----
C:\Users\Genius Computer\OneDrive\git-assignment-course
```

### Command 2: dir

The `dir` command displays the files and folders in the current directory.

**Command:**

```powershell
dir
```

**Actual terminal output:**

```text
Directory: C:\Users\Genius Computer\OneDrive\git-assignment-course

Mode   LastWriteTime         Length Name
----   -------------         ------ ----
dar--l 25-11-2026     22:58           docs
-a---l 25-11-2026     18:39      602  .gitignore
-a---l 25-11-2026     18:40     6557  README.md
-a---l 25-11-2026     22:58     2291  repo-basics.md
-a---l 25-11-2026     22:58     1436  SETUP.md
```

### Command 3: cd

The `cd` command changes the current working directory.

I used `cd ..` to move to the parent directory.

**Command:**

```powershell
cd ..
pwd
```

**Actual terminal output:**

```text
Path
----
C:\Users\Genius Computer\OneDrive
```

Then I returned to my project directory.

**Command:**

```powershell
cd .\git-assignment-course
pwd
```

**Actual terminal output:**

```text
Path
----
C:\Users\Genius Computer\OneDrive\git-assignment-course
```

These commands helped me understand how to navigate directories and inspect files using PowerShell.

## 4. Conclusion

I successfully verified my Git installation, configured my global username and email, and practiced basic terminal commands.

I learned how to check the Git version, view global configuration, display files and folders, and navigate between directories.

These steps prepared my Windows computer for working with Git repositories and version control.