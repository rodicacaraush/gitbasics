# Topic 06 — Viewing History (git log & git diff)

## git log — What was saved and when?

```bash
git log
```

Shows every commit with:
- Commit ID (a long unique code like `a3f9c2d...`)
- Author name and email
- Date and time
- Commit message

### Shorter view (one line per commit):
```bash
git log --oneline
```

---

## git diff — What exactly changed?

```bash
git diff
```

Run this BEFORE staging (`git add`) to see changes not yet staged.

### Reading the output:
```diff
- old line that was removed     (shown in red with -)
+ new line that was added       (shown in green with +)
  line that did not change      (no symbol)
```

### See changes already staged:
```bash
git diff --staged
```

---

## Practice Tasks

1. Run `git log --oneline` — how many commits do you have?
2. Edit any file, then run `git diff` — read what changed.
3. Stage the file with `git add`, then run `git diff --staged`.
   What is the difference between the two?
