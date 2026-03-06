# Tema 03 — Crearea unui Repository (git init)

## Analogia

Deschizi un folder nou și îi spui lui Git:
"Urmărește tot ce se întâmplă aici de acum înainte."
Acel folder devine un **repository** — un proiect pe care Git îl urmărește.

---

## Comanda

```bash
git init
```

Rulează această comandă o singură dată în orice folder. Git creează un folder ascuns
numit `.git` în interior — acolo Git stochează toată istoria și datele sale.
Nu șterge niciodată folderul `.git`.

---

## Pas cu Pas

```bash
# Intră în folderul proiectului tău
cd proiectul-meu

# Inițializează repository-ul
git init
```

Rezultat:
```
Initialized empty Git repository in .../proiectul-meu/.git/
```

---

## Verifică Statusul

```bash
git status
```

Imediat după `git init` vei vedea:
```
On branch master
No commits yet
nothing to commit
```

Aceasta este normal — Git este pregătit dar nu ai salvat nimic încă.

---

## Ce înseamnă "Untracked files"

Dacă ai deja fișiere în folder, Git le va lista ca "untracked".
Asta înseamnă că Git le vede dar NU înregistrează modificările lor încă.
Rezolvi asta cu `git add` — acesta este subiectul următor.

---

## Sarcini Practice

1. Creează un folder nou gol numit `test-repo` oriunde pe calculatorul tău.
2. Rulează `git init` în interior.
3. Rulează `git status` — ce vezi?
