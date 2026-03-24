# Contributing Guide

Welcome, and thank you for wanting to contribute! 🎉

This guide will walk you through **every single step** needed to make your first contribution. Read it fully before starting.

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [Step 1 — Fork the Repository](#step-1--fork-the-repository)
- [Step 2 — Clone Your Fork](#step-2--clone-your-fork)
- [Step 3 — Create a Branch](#step-3--create-a-branch)
- [Step 4 — Make Your Change](#step-4--make-your-change)
- [Step 5 — Commit Your Change](#step-5--commit-your-change)
- [Step 6 — Push to GitHub](#step-6--push-to-github)
- [Step 7 — Open a Pull Request](#step-7--open-a-pull-request)
- [Step 8 — Respond to Reviews](#step-8--respond-to-reviews)
- [Writing Good Commit Messages](#writing-good-commit-messages)
- [Branch Naming Convention](#branch-naming-convention)
- [Code of Conduct](#code-of-conduct)

---

## Prerequisites

Before you start, make sure you have:

- [ ] A **GitHub account** — [Sign up here](https://github.com/signup) (it's free)
- [ ] **Git installed** on your computer — [Download Git](https://git-scm.com/downloads)
- [ ] A **text editor** — [VS Code](https://code.visualstudio.com/) is recommended

**Verify Git is installed** by running this in your terminal:

```bash
git --version
```

You should see something like `git version 2.x.x`. If you get an error, Git is not installed.

---

## Step 1 — Fork the Repository

**What is a fork?** A fork is your own personal copy of this repo on GitHub. You make changes in your fork, not the original.

1. Click the **Fork** button at the top-right of this page
2. GitHub will create a copy at `https://github.com/YOUR-USERNAME/open-source-practice`
3. You now own this copy — do anything you like with it!

---

## Step 2 — Clone Your Fork

**What is cloning?** Cloning downloads your fork from GitHub to your local computer so you can edit files.

```bash
git clone https://github.com/YOUR-USERNAME/open-source-practice.git
```

Replace `YOUR-USERNAME` with your actual GitHub username.

Then move into the project folder:

```bash
cd open-source-practice
```

**Connect to the original repo** (called "upstream") so you can get future updates:

```bash
git remote add upstream https://github.com/anishaman6206/open-source-practice.git
```

Verify your remotes are set up:

```bash
git remote -v
```

You should see both `origin` (your fork) and `upstream` (the original).

---

## Step 3 — Create a Branch

**What is a branch?** A branch is an isolated workspace. Changes on your branch don't affect `main` until you merge.

⚠️ **Never commit directly to `main`.** Always create a new branch for every contribution.

First, make sure your local `main` is up to date:

```bash
git checkout main
git pull upstream main
```

Now create your branch:

```bash
git checkout -b your-branch-name
```

**Example:**

```bash
git checkout -b feat/add-ada-lovelace-contributor
```

See [Branch Naming Convention](#branch-naming-convention) for naming rules.

---

## Step 4 — Make Your Change

Open the file you want to edit in your text editor and make your change.

For example, to add your name to the Contributors table in `README.md`:

```markdown
| Your Name | @your-github-handle | Added my name to the list |
```

Save the file when done.

---

## Step 5 — Commit Your Change

**What is a commit?** A commit is a snapshot of your changes with a message describing what you did.

First, check what files you changed:

```bash
git status
```

Stage your changes (tell Git which files to include in the commit):

```bash
git add README.md
```

Or stage all changed files at once:

```bash
git add .
```

Now commit with a clear message:

```bash
git commit -m "feat: add Ada Lovelace to contributors"
```

See [Writing Good Commit Messages](#writing-good-commit-messages) for the format.

---

## Step 6 — Push to GitHub

**What is pushing?** Pushing sends your local commits up to GitHub.

```bash
git push origin your-branch-name
```

Example:

```bash
git push origin feat/add-ada-lovelace-contributor
```

---

## Step 7 — Open a Pull Request

**What is a PR?** A Pull Request asks the repo owner to review and merge your changes into the main repo.

1. Go to your fork on GitHub: `https://github.com/YOUR-USERNAME/open-source-practice`
2. You'll see a banner: **"Compare & pull request"** — click it
3. Fill in the PR form:
   - **Title:** Follow the format in [Branch Naming Convention](#branch-naming-convention)
   - **Description:** Fill in the PR template (it will appear automatically)
4. Click **"Create Pull Request"**

A maintainer will review your PR and either:
- ✅ **Approve and merge it** — congratulations, you've contributed!
- 💬 **Request changes** — they'll leave comments asking you to adjust something

---

## Step 8 — Respond to Reviews

If a reviewer requests changes:

1. Read their comments carefully
2. Make the changes on your **same branch** (don't create a new one)
3. Commit and push again — the PR updates automatically

```bash
# Make your changes, then:
git add .
git commit -m "fix: address review comments"
git push origin your-branch-name
```

Reply to the review comments on GitHub to let the reviewer know you've made the changes.

---

## Writing Good Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>: <short description>
```

| Type | When to use |
|------|-------------|
| `feat` | Adding something new |
| `fix` | Fixing a bug or error |
| `docs` | Updating documentation |
| `chore` | Maintenance tasks |
| `style` | Formatting, no logic change |

**Good examples:**
```
feat: add John Doe to contributors list
fix: correct typo in about.md
docs: add fun fact about elephants
```

**Bad examples:**
```
update stuff
changes
asdfgh
```

---

## Branch Naming Convention

```
<type>/<short-description-with-hyphens>
```

**Good examples:**
```
feat/add-john-doe-contributor
fix/typo-in-about-md
docs/add-fun-fact-penguins
```

---

## Code of Conduct

By contributing, you agree to follow our [Code of Conduct](CODE_OF_CONDUCT.md).

The short version: **be kind, be respectful, be patient.** Everyone here is learning.

---

*Still confused? Open a [Question Issue](.github/ISSUE_TEMPLATE/question.md) — we're happy to help!* 💬
