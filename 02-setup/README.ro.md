# Tema 02 — Configurarea Git (git config)

## Analogia

Înainte ca Git să îți înregistreze munca, trebuie să știe cine face modificările.
Gândește-te ca și cum îți semnezi numele pe fiecare lucrare pe care o depui.

---

## Comenzi

### Verifică dacă Git este instalat
```bash
git --version
```

### Setează numele și email-ul (o singură dată per calculator)
```bash
git config --global user.name "Numele Tău"
git config --global user.email "tu@exemplu.com"
```

### Verifică configurația
```bash
git config --list
```
Caută `user.name` și `user.email` la sfârșitul listei.

---

## Ce înseamnă `--global`?

Înseamnă că această setare se aplică TUTUROR proiectelor tale Git de pe acest calculator.

---

## Sarcini Practice

1. Rulează `git --version` și confirmă că Git este instalat.
2. Setează numele și email-ul folosind `git config --global`.
3. Rulează `git config --list` și găsește numele și email-ul tău în rezultat.
