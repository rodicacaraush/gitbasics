# Topic 09 — Undoing Changes

## The Analogy

You wrote something wrong in your story. You have three options:
1. Erase before saving (git restore)
2. Remove from the "ready to save" pile (git restore --staged)
3. Undo a commit but keep the history (git revert)

---

## Situation 1 — Modified a file, NOT staged yet

```bash
git restore filename.txt
```
Discards changes in the file. Reverts to the last committed version.

---

## Situation 2 — File is staged (git add done), NOT committed yet

```bash
git restore --staged filename.txt
```
Removes the file from staging. The changes in the file are kept.
Then use `git restore filename.txt` to also discard the file changes.

---

## Situation 3 — Already committed, want to undo

```bash
git revert HEAD
```
Creates a NEW commit that undoes the last commit.
The original commit stays in history — nothing is deleted.

---

## Key Rule

`git revert` is SAFE — it never deletes history.
Always prefer `git revert` over destructive commands like `git reset --hard`.

---

## Summary Table

| Situation | Command |
|-----------|---------|
| Changed file, not staged | `git restore file.txt` |
| File staged, not committed | `git restore --staged file.txt` |
| Commit already made | `git revert HEAD` |

---

## Practice Tasks

1. Modify a file, then use `git restore` to undo it.
2. Modify a file, stage it, then use `git restore --staged` to unstage it.
3. Make a bad commit, then use `git revert HEAD` to undo it.
4. Run `git log --oneline` — can you see the revert commit in the history?


Git a deschis editorul Vim pentru mesajul de commit al revert-ului. Ești "blocat" în Vim — nu poți scrie comenzi normale.

  Ieși din Vim și salvează cu acești pași:

  1. Apasă Esc (pentru siguranță)
  2. Tastează exact: :wq
  3. Apasă Enter

  :wq = write (salvează) + quit (ieși).