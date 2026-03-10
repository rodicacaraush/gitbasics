# Topic 11 — Ignoring Files (.gitignore)

## The Analogy

You have a drawer with private documents — passwords, personal notes.
When you take a photo of your desk for GitHub, you want that drawer
to be completely invisible to Git.

`.gitignore` is a file where you tell Git: "Never track these files."

---

## Creating .gitignore

Create a file named `.gitignore` (starts with a dot, no extension)
in the root of your project. Write one rule per line.

---

## Syntax

```
# Ignore a specific file
secret.txt

# Ignore all files with .log extension
*.log

# Ignore an entire folder
node_modules/

# Ignore all files inside a folder
logs/*
```

**Important:** No spaces before the rules — Git reads them literally.

---

## Common Things to Ignore

| File/Folder | Why |
|-------------|-----|
| `.env` | Contains passwords and secret keys |
| `node_modules/` | Auto-generated, very large |
| `*.log` | Temporary log files |
| `Thumbs.db` | Windows system file |
| `.DS_Store` | Mac system file |

---

## How to Verify It Works

After saving `.gitignore`, run:
```bash
git status
```
The ignored files should NOT appear in the list.

---

## Practice Tasks

1. Add `*.tmp` to your `.gitignore`.
2. Create a file called `test.tmp` with any content.
3. Run `git status` — does `test.tmp` appear?
