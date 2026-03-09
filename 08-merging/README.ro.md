# Tema 08 — Merge (git merge)

## Analogia

Ai terminat de scris finalul alternativ pe copia ta.
Ți-a plăcut — acum vrei să îl atașezi la povestea originală.
Aceasta este un **merge**.

---

## Ce este un Merge?

Merge-ul preia modificările dintr-un branch și le aduce în altul.
De obicei faci merge dintr-un branch de lucru înapoi în `master`.

---

## Pașii

```bash
# 1. Treci pe branch-ul în care vrei să aduci modificările (de obicei master)
git switch master

# 2. Fă merge cu celălalt branch
git merge nume-branch
```

---

## Fast-Forward Merge

Cel mai simplu tip. Se întâmplă când `master` nu are commit-uri noi de când a fost creat branch-ul.
Git pur și simplu avansează `master` pentru a corespunde branch-ului — fără conflict, fără commit extra.

```
Înainte:  master → A → B
                        └── feature → C → D

După:     master → A → B → C → D
```

Output arată astfel:
```
Fast-forward
 fisier.txt | 8 ++++++++
```

---

## După un Merge

Rulează `git log --oneline` — vei vedea ambele branch-uri arătând spre același commit:
```
d200ed4 (HEAD -> master, topic-07-practice) mesajul commit-ului tău
```
Asta înseamnă că ambele branch-uri sunt acum sincronizate.

---

## Sarcini Practice

1. Creează un branch nou: `git switch -c test-merge`
2. Creează un fișier și fă commit pe acel branch.
3. Întoarce-te pe master: `git switch master`
4. Fă merge: `git merge test-merge`
5. Rulează `git log --oneline` — ce observi?
