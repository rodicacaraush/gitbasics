# Tema 07 — Branch-uri (git branch & git switch)

## Analogia

Ești la capitolul 3 din povestea ta și vrei să încerci un final diferit
fără să strici originalul. Faci o copie — acea copie este un **branch**.

---

## Comenzi Cheie

```bash
# Vezi toate branch-urile (* marchează branch-ul curent)
git branch

# Creează un branch nou
git branch nume-branch

# Treci pe un branch
git switch nume-branch

# Creează ȘI treci pe el într-un singur pas
git switch -c nume-branch

# Șterge un branch
git branch -d nume-branch
```

---

## Ce Se Întâmplă de Fapt?

Branch-urile NU sunt foldere pe disc.
Ele trăiesc în interiorul folderului ascuns `.git`.

Când schimbi branch-ul, Git actualizează fișierele pe care le vezi în proiect
pentru a corespunde versiunii acelui branch. Fișierele din alte branch-uri sunt
ascunse în `.git` până când revii pe ele.

---

## Regulă Importantă

Știe întotdeauna pe ce branch ești înainte să faci modificări.
Verifică cu:
```bash
git branch
```
`*` arată branch-ul tău curent.

---

## Sarcini Practice

1. Rulează `git branch` — pe ce branch ești?
2. Creează un branch nou: `git switch -c branch-test`
3. Creează un fișier, fă commit pe branch-ul nou.
4. Treci înapoi pe master — dispare fișierul?
5. Treci înapoi pe branch-ul tău — reapare?
