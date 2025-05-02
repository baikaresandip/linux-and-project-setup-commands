# Git 
## 📘 Git Commands Reference

### 📁 Repository Management

```bash
git init
```

> Initialize a new Git repository in the current directory.

```bash
git clone <repo-url>
```

> Clone an existing Git repository to your local machine.

---

### 📄 Staging & Committing

```bash
git status
```

> Show the current state of the working directory and staging area.

```bash
git add <file>
```

> Add a file to the staging area.

```bash
git add .
```

> Add **all changes** (new, modified, deleted files) to the staging area.

```bash
git commit -m "Your commit message"
```

> Commit staged changes with a message.

---

### 📜 Branching

```bash
git branch
```

> List all local branches.

```bash
git branch <branch-name>
```

> Create a new branch.

```bash
git checkout <branch-name>
```

> Switch to a different branch.

```bash
git checkout -b <new-branch>
```

> Create and switch to a new branch.

```bash
git merge <branch>
```

> Merge the specified branch into the current one.

---

### 🌐 Remote Repositories

```bash
git remote add origin <repo-url>
```

> Add a remote repository named `origin`.

```bash
git remote -v
```

> Show URLs of the remote repositories.

```bash
git push origin <branch-name>
```

> Push local branch to the remote repository.

```bash
git pull
```

> Fetch and merge changes from the remote repository.

---

### 🧹 Undo & Reset

```bash
git reset <file>
```

> Unstage a file (but keep the changes in working directory).

```bash
git reset --hard
```

> Discard all local changes and reset to the last commit.

```bash
git checkout -- <file>
```

> Discard changes in a specific file.

---

### 🔍 Viewing History

```bash
git log
```

> View commit history.

```bash
git log --oneline
```

> Get the all files changes in the last commit
```bash 
git diff --name-only HEAD HEAD~1
```

> View a simplified commit history.

```bash
git diff
```

> Show differences between working directory and index.

```bash
git show <commit>
```

> Show details of a specific commit.

---

### 🧪 Tags

```bash
git tag
```

> List all tags.

```bash
git tag <tagname>
```

> Create a new tag.

```bash
git push origin <tagname>
```

> Push a specific tag to the remote repository.

---

### 🗑️ Deleting

```bash
git branch -d <branch>
```

> Delete a local branch.

```bash
git rm <file>
```

> Remove a file from the working directory and stage the deletion.

---

### 🧠 Tips

* Use `.gitignore` to exclude files from tracking.
* Always commit with meaningful messages.
* Use `git stash` to temporarily save uncommitted changes.
