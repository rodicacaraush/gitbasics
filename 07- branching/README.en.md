# Topic 07 — Branching (git branch & git switch)

## The Analogy

You are at chapter 3 of your story and want to try a different ending
without ruining the original. You make a copy — that copy is a **branch**.

---

## Key Commands

```bash
# See all branches (* marks the current one)
git branch

# Create a new branch
git branch branch-name

# Switch to a branch
git switch branch-name

# Create AND switch in one step
git switch -c branch-name

# Delete a branch
git branch -d branch-name
```

---

## What Actually Happens?

Branches are NOT folders on your disk.
They live inside the hidden `.git` folder.

When you switch branches, Git updates the files you see in your project
to match that branch's version. Files from other branches are hidden
inside `.git` until you switch back.

---

## Important Rule

Always know which branch you are on before making changes.
Check with:
```bash
git branch
```
The `*` shows your current branch.

---

## Practice Tasks

1. Run `git branch` — which branch are you on?
2. Create a new branch: `git switch -c my-test-branch`
3. Create a file, commit it on the new branch.
4. Switch back to master — does the file disappear?
5. Switch back to your branch — does it reappear?
