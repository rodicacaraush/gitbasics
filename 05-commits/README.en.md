# Topic 05 — Saving Snapshots (git commit)

## The Analogy

`git add` = you chose who stands in the photo.
`git commit` = you press the button and save the photo forever, with a label describing the moment.

---

## What is a Commit?

A commit is a permanent snapshot of your staged files. Every commit records:
- The changes you saved
- Your name and email
- The date and time
- A message you write describing what changed

---

## The Command

```bash
git commit -m "your message here"
```

`-m` stands for "message". Always write a short, clear description.

### Good commit messages:
```
initial commit
add login page
fix typo in README
update homepage layout
```

### Bad commit messages:
```
stuff
asdfgh
changes
```

---

## After Committing

Run `git status` — you will see:
```
nothing to commit, working tree clean
```
This means everything is saved. Nothing has changed since your last snapshot.

---

## View Your Commits

```bash
git log
```

Shows the full history: commit ID, author, date, and message.

---

## Practice Tasks

1. Create a new file called `test.txt` with any text inside.
2. Stage it with `git add test.txt`.
3. Commit it with a meaningful message using `git commit -m "..."`.
4. Run `git log` — can you see both commits now?
