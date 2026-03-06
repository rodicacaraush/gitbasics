# Tema 05 — Salvarea Instantaneelor (git commit)

## Analogia

`git add` = ai ales cine stă în poză.
`git commit` = apeși pe buton și salvezi fotografia pentru totdeauna, cu o etichetă care descrie momentul.

---

## Ce este un Commit?

Un commit este un instantaneu permanent al fișierelor tale staged. Fiecare commit înregistrează:
- Modificările pe care le-ai salvat
- Numele și email-ul tău
- Data și ora
- Un mesaj scris de tine care descrie ce s-a schimbat

---

## Comanda

```bash
git commit -m "mesajul tău aici"
```

`-m` înseamnă "mesaj". Scrie întotdeauna o descriere scurtă și clară.

### Mesaje bune de commit:
```
commit initial
adaugă pagina de login
corectează greșeala din README
actualizează layout-ul paginii principale
```

### Mesaje proaste de commit:
```
chestii
asdfgh
modificări
```

---

## După Commit

Rulează `git status` — vei vedea:
```
nothing to commit, working tree clean
```
Asta înseamnă că totul este salvat. Nimic nu s-a schimbat de la ultimul tău instantaneu.

---

## Vezi Commit-urile Tale

```bash
git log
```

Afișează istoricul complet: ID commit, autor, dată și mesaj.

---

## Sarcini Practice

1. Creează un fișier nou numit `test.txt` cu orice text înăuntru.
2. Adaugă-l cu `git add test.txt`.
3. Fă commit cu un mesaj semnificativ folosind `git commit -m "..."`.
4. Rulează `git log` — poți vedea ambele commit-uri acum?
