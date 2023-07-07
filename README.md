Git & Github Documentation - Manthan Mishra

Introduction:

- Git is version control System
- Used to track the code changes

Basic:

Firstly, we need to initialize git on a particular directory.

# (1) git init

# --> It creates a hidden folder named ".git".

eg:

PS D:\git-tut> git init
Initialized empty Git repository in D:/git-tut/.git/
========================================================

# (2) git status

# ---> It tells us about the tracked and untracked files

eg:

On branch master

No commits yet

Untracked files:
(use "git add <file>..." to include in what will be committed)
README.md
index.html

# nothing added to commit but untracked files present (use "git add" to track)

# (3) git add

# ----> To move files to staging environment

eg:

# git add index.html

# (3.1) git add --all

# ---->To add more than one files

eg:

# git add --all

--->Now again check with git status

==================================================
eg:

On branch master

No commits yet

Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file: README.md
new file: index.css
new file: index.html
==================================================

# (4) git commit -m "<message>"

--> It is a save point
-->We can go back to this stage of app or product and fix the bug
================================================
eg:

git commit -m "first release in paktolus"
[master (root-commit) ecfe956] first release in paktolus
3 files changed, 42 insertions(+)
create mode 100644 README.md
create mode 100644 index.css
create mode 100644 index.html

================================================

# (4.1) git commit -a -m "<message>"

----> It is used to commit without staging
----> But it is not recommended

# -----> Now lets use git status again

eg:

git status
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index.html

# no changes added to commit (use "git add" and/or "git commit -a")

---> Now lets commit without going to staging level/phase

====================================================
eg:

git commit -a -m "git commit without staging"
[master a449971] git commit without staging
1 file changed, 1 insertion(+)
====================================================

# (5) git log

---> Used to view the history of commits for a repo

====================================================
eg:

git log
commit a449971fd3adcabd1f3631b062b421ebe023e152 (HEAD -> master)
Author: manthan-paktolus <mmishra@paktolus.com>
Date: Thu Jul 6 14:40:07 2023 +0530

    git commit without staging

commit ecfe9564ff3a4b27b100f985cd696702dc833281
Author: manthan-paktolus <mmishra@paktolus.com>
Date: Thu Jul 6 14:31:21 2023 +0530

    first release in paktolus

====================================================

# (6) git <command> -help

---> to see the available options for specific command

======================================================
eg:

git status -help
usage: git status [<options>] [--] [<pathspec>...]

    -v, --verbose         be verbose
    -s, --short           show status concisely
    -b, --branch          show branch information
    --show-stash          show stash information
    --ahead-behind        compute full ahead/behind values
    --porcelain[=<version>]
                          machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --ignored[=<mode>]    show ignored files, optional modes: traditional, matching, no. (Default: traditional)
    --ignore-submodules[=<when>]
                          ignore changes to submodules, optional when: all, dirty, untracked. (Default: all)
    --column[=<style>]    list untracked files in columns
    --no-renames          do not detect renames
    -M, --find-renames[=<n>]
                          detect renames, optionally set similarity index

======================================================

# (6.1) git help --all

---> to see all possible commands

=======================================================
eg:

git help --all
See 'git help <command>' to read about a specific subcommand

Main Porcelain Commands
add Add file contents to the index
am Apply a series of patches from a mailbox
archive Create an archive of files from a named tree
bisect Use binary search to find the commit that introduced a bug
branch List, create, or delete branches
bundle Move objects and refs by archive
checkout Switch branches or restore working tree files
cherry-pick Apply the changes introduced by some existing commits
citool Graphical alternative to git-commit
clean Remove untracked files from the working tree
clone Clone a repository into a new directory
commit Record changes to the repository
describe Give an object a human readable name based on an available ref
diff Show changes between commits, commit and working tree, etc
fetch Download objects and refs from another repository
format-patch Prepare patches for e-mail submission
gc Cleanup unnecessary files and optimize the local repository
gitk The Git repository browser
grep Print lines matching a pattern
gui A portable graphical interface to Git
init Create an empty Git repository or reinitialize an existing one
log Show commit logs
maintenance Run tasks to optimize Git repository data
merge Join two or more development histories together
mv Move or rename a file, a directory, or a symlink
notes Add or inspect object notes
pull Fetch from and integrate with another repository or a local branch
push Update remote refs along with associated objects
range-diff Compare two commit ranges (e.g. two versions of a branch)
=======================================================

# (7) git branch <branch-name>

# ---> to create a new branch

eg:

git branch add-new-content
PS D:\git-tut> git branch
add-new-content

- # master

# (8) git checkout <branchName>

# ---> to move from one branch to another

eg:

git checkout add-new-content
Switched to branch 'add-new-content'
PS D:\git-tut> git branch

- add-new-content
  master
  ========================================================

# (8.1) git checkout -b <branchName>

# ---> directly branch will changed and also new branch will be created

eg:

git checkout -b emergeny-fix
Switched to a new branch 'emergeny-fix'
======================================================

# (9) git merge <branchName>

---> to merge two branches

====================================================
eg:

git merge emergeny-fix
Updating 7f86a76..73fae70
Fast-forward
index.html | 2 +-
1 file changed, 1 insertion(+), 1 deletion(-)
====================================================
