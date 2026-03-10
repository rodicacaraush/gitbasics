# Topic 12 — Merge Conflicts

## The Analogy

You and a colleague both edit the same line in the same file on different branches.
When you merge, Git does not know which version to keep — so it asks you to decide.

---

## When Does a Conflict Happen?

When two branches modify the **same line** in the **same file**.
Git can handle most merges automatically — conflicts only happen in this specific case.

---

## What a Conflict Looks Like

When you run `git merge` and there is a conflict, Git marks the file like this:

```
<<<<<<< HEAD
Your version (current branch)
=======
Their version (branch being merged)
>>>>>>> branch-name
```

| Marker | Meaning |
|--------|---------|
| `<<<<<<< HEAD` | Start of your version |
| `=======` | Divider between the two versions |
| `>>>>>>> branch-name` | End of the incoming version |

---

## How to Resolve

1. Open the conflicted file in your editor
2. Decide what to keep — your version, their version, or a combination
3. Delete ALL the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Save the file
5. Stage and commit:

```bash
git add filename.txt
git commit -m "resolve merge conflict"
```

---

## Tips

- VS Code highlights conflicts with colors and buttons (Accept Current / Accept Incoming)
- Always communicate with your team before merging to avoid conflicts
- Conflicts are normal — every developer encounters them

---

## Practice Tasks

1. Create two branches that modify the same line in a file.
2. Merge them and observe the conflict markers.
3. Resolve manually by keeping one version.
4. Run `git log --oneline` — can you see the merge commit?
