
## Assignment 1: Git Configuration & Customization (Windows)

### Objective
Set up Git with your user details and custom aliases on Windows.

### Steps
1. Open **Command Prompt** or **Git Bash**.
2. Configure your global Git username and email:
   ```cmd
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

3. Create a Git alias to simplify commands (e.g., `git status` as `git s`):
   ```cmd
   git config --global alias.s "status"
   ```
4. Verify your configuration:
   ```cmd
   git config --list
   ```
5. Test the alias by running:
   ```cmd
   git s
   ```
6. Unset the alias:
   ```cmd
   git config --global --unset alias.s
   ```

✅ **Task Completion Check:** Run `git config --list` and ensure configurations are set.

---

## Assignment 2: Git Basics - Initialize, Clone & Commit (Windows)

### Objective
Learn to create a repository, track changes, and commit files on Windows.

### Steps
1. Open **Command Prompt** or **Git Bash**.
2. Navigate to a folder where you want to create a new repository:
   ```cmd
   cd C:\Users\YourUser\Documents
   mkdir Azure-DevOps && cd Azure-DevOps
   ```
3. Initialize a new Git repository:
   ```cmd
   git init
   ```
4. Create a file and add some content:
   ```cmd
   echo This is my first git project > hello.txt 
   ```
5. Stage the file:
   ```cmd
   git add hello.txt
   ```
6. Commit the changes:
   ```cmd
   git commit -m "Added hello.txt"
   ```
7. View commit history:
   ```cmd
   git log --oneline
   ```

✅ **Task Completion Check:** Run `git log --oneline` to confirm the commit is recorded.

---

## Assignment 3: Branching & Merging (Windows)

### Objective
Create, switch, and merge branches in Git on Windows.

### Steps
1. Open **Command Prompt** or **Git Bash**.
2. Navigate to your repository and create a new file:
   ```cmd
   cd C:\Users\YourUser\Documents\Azure-DevOps
   echo Main branch content > file.txt
   git add file.txt or git add .
   git commit -m "Initial commit on main branch"
   ```
3. Create a new branch and switch to it:
   ```cmd
   git branch feature-branch
   git checkout feature-branch  # or `git switch feature-branch`
   ```
4. Modify the file and commit:
   ```cmd
   echo Feature branch update >> file.txt
   git add file.txt
   git commit -m "Updated file.txt in feature branch"
   ```
5. Switch back to `main`:
   ```cmd
   git checkout main
   ```
6. Merge `feature-branch` into `main`:
   ```cmd
   git merge feature-branch
   ```
7. Delete the feature branch:
   ```cmd
   git branch -d feature-branch
   ```

✅ **Task Completion Check:** Run `git log --oneline` and `type file.txt` to verify the merge.

---

## Assignment 4: Pushing & Pulling from Remote Repository (Windows)

### Objective
Learn how to connect a local Git repository with a remote repository on Windows.

### Steps
1. Create a **new repository on GitHub** (do not initialize with README).
2. Open **Command Prompt** or **Git Bash**, and navigate to a directory where you want to clone the repo:
   ```cmd
   cd C:\Users\YourUser\Documents
   git clone <repo_url>
   cd <repo_name>
   ```
3. Create a new file and commit it:
   ```cmd
   echo This is a test from remote repo > remote.txt
   git add remote.txt or git add .
   git commit -am "Added remote.txt"
   ```
4. Push the changes to GitHub:
   ```cmd
   git push or git push origin main 
   ```
5. Fetch the latest changes (if any):
   ```cmd
   git fetch origin
   ```
6. Pull changes (if needed):
   ```cmd
   git pull origin main
   ```
7. List and verify remote repositories:
   ```cmd
   git remote -v
   ```

✅ **Task Completion Check:** Verify changes on GitHub after pushing.

---

## Assignment 5: Stashing & Cherry-Picking (Windows)

### Objective
Temporarily save changes and apply specific commits selectively on Windows.

### Steps
1. Open **Command Prompt** or **Git Bash**, and navigate to your working directory:
   ```cmd
   cd C:\Users\YourUser\Documents
   git init stash-demo && cd stash-demo
   echo Initial version > stash-file.txt
   git add stash-file.txt
   git commit -am "Initial commit"
   ```
2. Modify the file but **do not commit**:
   ```cmd
   echo Uncommitted changes >> stash-file.txt
   ```
3. Stash the changes:
   ```cmd
   git stash
   ```
4. View stashed changes:
   ```cmd
   git stash list
   ```
5. Apply and remove the stash:
   ```cmd
   git stash pop
   ```
6. Create a new branch and commit multiple changes:
   ```cmd
   git branch cherry-pick-demo
   git checkout cherry-pick-demo
   echo Cherry-pick Commit 1 > file1.txt && git add file1.txt && git commit -m "Commit 1"
   echo Cherry-pick Commit 2 > file2.txt && git add file2.txt && git commit -m "Commit 2"
   ```
7. Switch to `main` and cherry-pick only **Commit 1**:
   ```cmd
   git checkout main
   git cherry-pick <commit-hash-of-commit-1>
   ```

✅ **Task Completion Check:** Run `git log --oneline` to confirm only Commit 1 is added.

---
**Well done! You've made great progress in mastering Git. Keep practicing, keep exploring, and keep it up!🔥**
