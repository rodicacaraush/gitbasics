# Tema 09 — Anularea Modificărilor

## Analogia

Ai scris ceva greșit în poveste. Ai trei opțiuni:
1. Ștergi înainte să salvezi (git restore)
2. Scoți din "gata de salvat" (git restore --staged)
3. Anulezi un commit dar păstrezi istoricul (git revert)

---

## Situația 1 — Ai modificat un fișier, NU ai făcut git add

```bash
git restore nume-fisier.txt
```
Anulează modificările din fișier. Revine la ultima versiune commitată.

---

## Situația 2 — Fișierul e staged (ai făcut git add), NU ai făcut commit

```bash
git restore --staged nume-fisier.txt
```
Scoate fișierul din staging. Modificările din fișier rămân.
Folosește apoi `git restore nume-fisier.txt` pentru a anula și modificările.

---

## Situația 3 — Ai făcut deja commit, vrei să îl anulezi

```bash
git revert HEAD
```
Creează un commit NOU care anulează ultimul commit.
Commit-ul original rămâne în istoric — nimic nu se șterge.

---

## Regula Cheie

`git revert` este SIGUR — nu șterge niciodată istoricul.
Preferă întotdeauna `git revert` față de comenzi distructive ca `git reset --hard`.

---

## Tabel Rezumat

| Situație | Comandă |
|----------|---------|
| Fișier modificat, nestaged | `git restore fisier.txt` |
| Fișier staged, necommitat | `git restore --staged fisier.txt` |
| Commit deja făcut | `git revert HEAD` |

---

## Sarcini Practice

1. Modifică un fișier, apoi folosește `git restore` pentru a anula.
2. Modifică un fișier, adaugă-l în staging, apoi folosește `git restore --staged`.
3. Fă un commit greșit, apoi folosește `git revert HEAD` pentru a-l anula.
4. Rulează `git log --oneline` — poți vedea commit-ul de revert în istoric?


Git a deschis editorul Vim pentru mesajul de commit al revert-ului. Ești "blocat" în Vim — nu poți scrie comenzi normale.

  Ieși din Vim și salvează cu acești pași:

  1. Apasă Esc (pentru siguranță)
  2. Tastează exact: :wq
  3. Apasă Enter

  :wq = write (salvează) + quit (ieși).