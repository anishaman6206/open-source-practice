# Common Errors & How to Fix Them

Run into a problem? Check here first!

---

## ❌ `git: command not found`

**What it means:** Git is not installed on your computer.

**Fix:** Download and install Git from [https://git-scm.com/downloads](https://git-scm.com/downloads), then restart your terminal.

---

## ❌ `Permission denied (publickey)`

**What it means:** GitHub doesn't recognize your computer.

**Fix:** You need to set up an SSH key, or use HTTPS instead. For HTTPS, clone using:

```bash
git clone https://github.com/YOUR-USERNAME/open-source-practice.git
```

When pushing, GitHub will ask for your username and a **Personal Access Token** (not your password). [Create one here](https://github.com/settings/tokens).

---

## ❌ `error: failed to push some refs`

**What it means:** Someone else made changes to the branch and your version is behind.

**Fix:** Pull the latest changes first, then push:

```bash
git pull origin your-branch-name
git push origin your-branch-name
```

---

## ❌ `You are not currently on a branch`

**What it means:** You're in a "detached HEAD" state — you checked out a specific commit instead of a branch.

**Fix:** Create a new branch from here:

```bash
git checkout -b your-new-branch-name
```

---

## ❌ Accidentally committed to `main`

**What it means:** You made commits directly on the `main` branch instead of a feature branch.

**Fix:**

```bash
# Create a new branch with your changes
git branch your-branch-name

# Reset main to where it was before
git reset --hard origin/main

# Switch to your new branch
git checkout your-branch-name
```

---

## ❌ `CONFLICT (content): Merge conflict in <filename>`

**What it means:** Two people edited the same part of the same file, and Git can't decide which version to keep.

**Fix:** Open the conflicting file. You'll see sections like:

```
<<<<<<< HEAD
Your version of the text
=======
Their version of the text
>>>>>>> upstream/main
```

Edit the file to keep the version you want (delete the markers), then:

```bash
git add <filename>
git commit -m "fix: resolve merge conflict"
```

---

## ❌ `I accidentally deleted a file!`

**Fix:** Restore it from the last commit:

```bash
git checkout HEAD -- path/to/file.md
```

---

## Still stuck?

Open a [Question Issue](../.github/ISSUE_TEMPLATE/question.md) — describe what happened, what you tried, and which step you're on. We'll help you out! 💬
