# Topic 08 — Merging (git merge)

## The Analogy

You finished writing the alternative ending on your copy.
You liked it — now you want to attach it to the original story.
That is a **merge**.

---

## What is a Merge?

Merging takes the changes from one branch and brings them into another.
You are usually merging a feature branch back into `master`.

---

## The Steps

```bash
# 1. Switch to the branch you want to merge INTO (usually master)
git switch master

# 2. Merge the other branch into it
git merge branch-name
```

---

## Fast-Forward Merge

The simplest type. Happens when `master` has no new commits since the branch was created.
Git simply moves `master` forward to match the branch — no conflict, no extra commit.

```
Before:  master → A → B
                       └── feature → C → D

After:   master → A → B → C → D
```

Output looks like:
```
Fast-forward
 file.txt | 8 ++++++++
```

---

## After a Merge

Run `git log --oneline` — you will see both branch names pointing to the same commit:
```
d200ed4 (HEAD -> master, topic-07-practice) your commit message
```
This means both branches are now in sync.

---

## Practice Tasks

1. Create a new branch: `git switch -c test-merge`
2. Create a file and commit it on that branch.
3. Switch back to master: `git switch master`
4. Merge: `git merge test-merge`
5. Run `git log --oneline` — what do you see?
