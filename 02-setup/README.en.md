# Topic 02 — Git Setup (git config)

## The Analogy

Before Git records your work, it needs to know who is making the changes.
Think of it like signing your name on every piece of work you submit.

---

## Commands

### Check if Git is installed
```bash
git --version
```

### Set your name and email (do this once per computer)
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Verify your configuration
```bash
git config --list
```
Look for `user.name` and `user.email` at the bottom of the list.

---

## What does `--global` mean?

It means this setting applies to ALL your Git projects on this computer.

---

## Practice Tasks

1. Run `git --version` and confirm Git is installed.
2. Set your name and email using `git config --global`.
3. Run `git config --list` and find your name and email in the output.
