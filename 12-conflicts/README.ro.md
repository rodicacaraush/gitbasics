# Tema 12 — Conflicte la Merge

## Analogia

Tu și un coleg editați aceeași linie din același fișier pe branch-uri diferite.
Când faceți merge, Git nu știe ce versiune să păstreze — și îți cere să decizi tu.

---

## Când Apare un Conflict?

Când două branch-uri modifică **aceeași linie** din **același fișier**.
Git poate gestiona majoritatea merge-urilor automat — conflictele apar doar în acest caz specific.

---

## Cum Arată un Conflict

Când rulezi `git merge` și există un conflict, Git marchează fișierul astfel:

```
<<<<<<< HEAD
Versiunea ta (branch-ul curent)
=======
Versiunea lor (branch-ul care se face merge)
>>>>>>> nume-branch
```

| Marker | Înțeles |
|--------|---------|
| `<<<<<<< HEAD` | Începutul versiunii tale |
| `=======` | Separator între cele două versiuni |
| `>>>>>>> nume-branch` | Sfârșitul versiunii primite |

---

## Cum Rezolvi

1. Deschide fișierul cu conflict în editor
2. Decide ce păstrezi — versiunea ta, a lor, sau o combinație
3. Șterge TOȚI markerii de conflict (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Salvează fișierul
5. Adaugă în staging și fă commit:

```bash
git add nume-fisier.txt
git commit -m "resolve merge conflict"
```

---

## Sfaturi

- VS Code evidențiază conflictele cu culori și butoane (Accept Current / Accept Incoming)
- Comunică întotdeauna cu echipa înainte de merge pentru a evita conflictele
- Conflictele sunt normale — orice developer le întâlnește

---

## Sarcini Practice

1. Creează două branch-uri care modifică aceeași linie dintr-un fișier.
2. Fă merge și observă markerii de conflict.
3. Rezolvă manual păstrând o versiune.
4. Rulează `git log --oneline` — poți vedea commit-ul de merge?
