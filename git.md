## 1. Setup and Configuration Commands

### `git config`

When setting up Git for the first time or changing user details.

**Example**:
```bash
git config --global user.name "----------"
git config --global user.email "--------@-------.com"
```
## 2. Basic Repository Commands

### `git init`

To start version control for a project OR Creates a new Git repository in the current folder.

**Example**:
```bash
git init
```
### `git clone`
To copy an existing repository to your local machine.

**Example**:
```bash
git clone https://github.com/user-name/repo-name.git
```
## 3. Working with Files
### `git add`

When you’ve made changes to files and want to stage them for commit.

**Example**:
```bash
git add file-name   # to add single file
git add .           # to add all files
```
### `git commit`

To save staged changes to the repository.

**Example**:
```bash
git commit -m "Add your comment"
git commit --amend -m "Change previous comment"
```
### `git status`
To see the state of the working directory and staging area.

**Example**:
```bash
git status
```
## 4. Branching and Merging

### `git branch`

To create, delete, or list branches.

**Example**:
```bash
git branch new-branch-name
git branch -d branch-name   # to delete old branch
git branch                  # list all branches
```
### `git switch` (preferred over `git checkout` for branches)

To move to another branch.

**Example**:
```bash
git switch branch-name
```
### `git merge`

To combine changes from another branch into the current one.

**Example**:
```bash
git merge branch-name         # merge current branch with branch-name
```
## 5. Viewing and Inspecting History

### `git log`

To view the commit history.

**Example**:
```bash
git log
git log --oneline   # show each commit in one line
```
### `git show`

To view the details of a specific commit.

**Example**:
```bash
git show commit-number
```
### `git diff`

To compare changes.

**Example**:
```bash
git diff
git diff branch-name main    # show difference b/w main and branch-name
```
## 6. Undoing Changes

### `git revert`

To undo changes made in a specific commit by creating a new commit.

**Example**:
```bash
git revert commit-number
```
## 7. Remote Repository Commands

### `git remote`

To add or manage remote repositories.

**Example**:
```bash
git remote add origin https://github.com/user-name/repo-name.git
git remote -v
```
### `git fetch`

To download updates from a remote repository without merging.

**Example**:
```bash
git fetch origin
```
### `git pull`

To fetch and merge updates from a remote repository.

**Example**:
```bash
git pull origin main
```
### `git push`

To upload commits to a remote repository.

**Example**:
```bash
git push origin branch-name
```
## 8. Miscellaneous Commands

### `git clean`

**Trigger**: To remove untracked files or directories.

**Example**:
```bash
git clean -f
git clean -fd
```
### `git blame`

**Trigger**: To identify who made changes to each line of a file.

**Example**:
```bash
git blame file-name
```
### `git cherry-pick`

**Trigger**: To apply specific commits from another branch.

**Example**:
```bash
git cherry-pick commit-number
```
