# Tema 11 — Ignorarea Fișierelor (.gitignore)

## Analogia

Ai un sertar cu documente private — parole, notițe personale.
Când faci o poză biroului tău pentru GitHub, vrei ca sertarul
să fie complet invizibil pentru Git.

`.gitignore` este un fișier în care îi spui lui Git: "Nu urmări niciodată aceste fișiere."

---

## Crearea .gitignore

Creează un fișier numit `.gitignore` (începe cu punct, fără extensie)
în folderul principal al proiectului. Scrie o regulă pe linie.

---

## Sintaxa

```
# Ignoră un fișier specific
secret.txt

# Ignoră toate fișierele cu extensia .log
*.log

# Ignoră un folder întreg
node_modules/

# Ignoră toate fișierele dintr-un folder
logs/*
```

**Important:** Fără spații înaintea regulilor — Git le citește literal.

---

## Ce să Ignori de Obicei

| Fișier/Folder | De ce |
|---------------|-------|
| `.env` | Conține parole și chei secrete |
| `node_modules/` | Generat automat, foarte mare |
| `*.log` | Fișiere temporare de log |
| `Thumbs.db` | Fișier de sistem Windows |
| `.DS_Store` | Fișier de sistem Mac |

---

## Cum Verifici că Funcționează

După salvarea `.gitignore`, rulează:
```bash
git status
```
Fișierele ignorate NU trebuie să apară în listă.

---

## Sarcini Practice

1. Adaugă `*.tmp` în `.gitignore`.
2. Creează un fișier numit `test.tmp` cu orice conținut.
3. Rulează `git status` — apare `test.tmp`?
