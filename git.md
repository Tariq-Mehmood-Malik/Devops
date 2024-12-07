## 1. Setup and Configuration Commands

### `git config`

When setting up Git for the first time or changing user details.

**Example**:
```bash
git config --global user.name "John Doe"
git config --global user.email "john@example.com"
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
git clone https://github.com/example/repo.git
```
## 3. Working with Files
### `git add`

When you’ve made changes to files and want to stage them for commit.

**Example**:
```bash
git add file1.txt
git add .
```
### `git commit`

To save staged changes to the repository.

**Example**:
```bash
git commit -m "Added feature X"
git commit --amend -m "Fixed typo in commit message"
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
git branch feature-branch
git branch -d old-branch
git branch
```
### `git switch` (preferred over `git checkout` for branches)

To move to another branch.

**Example**:
```bash
git switch feature-branch
```
### `git merge`

To combine changes from another branch into the current one.

**Example**:
```bash
git merge feature-branch
```
## 5. Viewing and Inspecting History

### `git log`

To view the commit history.

**Example**:
```bash
git log
git log --oneline # In one line
```
### `git show`

To view the details of a specific commit.

**Example**:
```bash
git show 123abc
```
### `git diff`

To compare changes.

**Example**:
```bash
git diff
git diff feature-branch main
```
## 6. Undoing Changes

### `git revert`

To undo changes made in a specific commit by creating a new commit.

**Example**:
```bash
git revert 123abc
```
## 7. Remote Repository Commands

### `git remote`

To add or manage remote repositories.

**Example**:
```bash
git remote add origin https://github.com/example/repo.git
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
git push origin feature-branch
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
git blame file1.txt
```
### `git cherry-pick`

**Trigger**: To apply specific commits from another branch.

**Example**:
```bash
git cherry-pick 123abc
```
