# Tema 06 — Vizualizarea Istoricului (git log & git diff)

## git log — Ce a fost salvat și când?

```bash
git log
```

Afișează fiecare commit cu:
- ID-ul commit-ului (un cod unic lung ca `a3f9c2d...`)
- Numele și email-ul autorului
- Data și ora
- Mesajul commit-ului

### Vizualizare scurtă (o linie per commit):
```bash
git log --oneline
```

---

## git diff — Ce s-a schimbat exact?

```bash
git diff
```

Rulează ÎNAINTE de staging (`git add`) pentru a vedea modificările care nu sunt încă staged.

### Citirea rezultatului:
```diff
- linie veche care a fost ștearsă     (roșu cu -)
+ linie nouă care a fost adăugată     (verde cu +)
  linie care nu s-a schimbat          (fără simbol)
```

### Vezi modificările deja staged:
```bash
git diff --staged
```

---

## Sarcini Practice

1. Rulează `git log --oneline` — câte commit-uri ai?
2. Editează orice fișier, apoi rulează `git diff` — citește ce s-a schimbat.
3. Adaugă fișierul cu `git add`, apoi rulează `git diff --staged`.
   Care este diferența dintre cele două?
