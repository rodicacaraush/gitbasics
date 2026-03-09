# Tema 10 — Repository-uri Remote (GitHub)

## Analogia

Repo-ul tău local este un caiet acasă.
GitHub este un dulap în cloud — o copie a caietului accesibilă de oriunde.

---

## Termeni Cheie

| Termen | Înțeles |
|--------|---------|
| Remote | O copie a repo-ului tău stocată online |
| origin | Numele implicit pe care Git îl dă remote-ului tău (GitHub) |
| push | Trimite commit-urile locale pe GitHub |
| pull | Descarcă modificările de pe GitHub pe calculatorul tău |
| clone | Descarcă un repo de pe GitHub pentru prima dată |

---

## Conectează un Repo Local la GitHub

```bash
# 1. Leagă repo-ul local de GitHub
git remote add origin https://github.com/username/nume-repo.git

# 2. Redenumește master în main (standardul GitHub)
git branch -M main

# 3. Trimite toate commit-urile pe GitHub (-u setează tracking-ul implicit)
git push -u origin main
```

---

## După Primul Push

```bash
# Trimite commit-uri noi pe GitHub
git push

# Descarcă modificări de pe GitHub
git pull
```

---

## Clonează un Repo (descarcă de pe GitHub)

```bash
git clone https://github.com/username/nume-repo.git
```

Creează o copie locală a oricărui repository de pe GitHub.

---

## Sarcini Practice

1. Mergi pe repo-ul tău GitHub în browser — poți vedea toate fișierele?
2. Editează un fișier direct pe GitHub (click pe iconița creion), fă commit acolo.
3. Rulează `git pull` în terminal — apare modificarea local?
