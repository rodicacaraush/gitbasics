# Notite Git — Referinta Rapida

> Foloseste acest fisier cand uiti ceva. Contine tot ce ai invatat + situatii practice.

---

## Termeni de Baza

| Termen | Intelesul simplu |
|--------|-----------------|
| Repository | Folderul proiectului pe care Git il urmareste |
| Commit | Un instantaneu salvat al proiectului |
| Branch | O copie separata a proiectului pentru lucru paralel |
| Merge | Combinarea a doua branch-uri |
| Staging | Zona de pregatire inainte de commit |
| Remote | Copia repo-ului stocata online (GitHub) |
| origin | Numele implicit al remote-ului tau |
| HEAD | Branch-ul/commit-ul la care esti in prezent |

---

## Fluxul de Lucru Zilnic

```
1. Verifica pe ce branch esti       git branch
2. Verifica ce s-a schimbat         git status
3. Vezi exact ce s-a modificat      git diff
4. Adauga fisierele dorite          git add fisier.txt  (sau git add .)
5. Salveaza instantaneul            git commit -m "mesaj clar"
6. Trimite pe GitHub                git push
```

---

## Toate Comenzile pe Categorii

### Configurare (o data per calculator)
```bash
git --version                                    # verifica versiunea
git config --global user.name "Numele Tau"       # seteaza numele
git config --global user.email "tu@email.com"    # seteaza email-ul
git config --list                                # verifica configuratia
```

### Creare Repository
```bash
git init                    # initializeaza repo in folderul curent
git clone URL               # descarca un repo de pe GitHub
```

### Verificare Status
```bash
git status                  # ce fisiere s-au schimbat
git log                     # istoricul complet al commit-urilor
git log --oneline           # istoricul scurt (o linie per commit)
git diff                    # ce s-a schimbat (inainte de git add)
git diff --staged           # ce s-a schimbat (dupa git add)
```

### Staging si Commit
```bash
git add fisier.txt          # adauga un fisier specific in staging
git add .                   # adauga TOATE fisierele modificate
git commit -m "mesaj"       # salveaza instantaneul cu un mesaj
```

### Branch-uri
```bash
git branch                  # lista tuturor branch-urilor (* = curent)
git branch nume             # creeaza un branch nou
git switch nume             # treci pe un branch
git switch -c nume          # creeaza SI treci pe el intr-un pas
git branch -d nume          # sterge un branch
```

### Merge
```bash
git switch main             # treci pe branch-ul de destinatie
git merge nume-branch       # aduce modificarile din alt branch
```

### Anulare Greseli
```bash
git restore fisier.txt              # anuleaza modificari (inainte de git add)
git restore --staged fisier.txt     # scoate din staging (pastreaza modificarile)
git revert HEAD                     # anuleaza ultimul commit (sigur, pastreaza istoricul)
```

### Remote (GitHub)
```bash
git remote add origin URL           # leaga repo-ul local de GitHub
git branch -M main                  # redenumeste branch-ul in main
git push -u origin main             # primul push (seteaza tracking-ul)
git push                            # trimite commit-urile noi pe GitHub
git pull                            # descarca modificarile de pe GitHub
```

---

## Situatii Frecvente in Practica

### "Am modificat un fisier din greseala si vreau sa il revin"
```bash
git restore fisier.txt
```

### "Am facut git add dar nu vreau sa commit acest fisier"
```bash
git restore --staged fisier.txt
```

### "Am facut un commit gresit"
```bash
git revert HEAD
# Se deschide Vim — tasteaza :wq si apasa Enter
```

### "Nu stiu pe ce branch sunt"
```bash
git branch        # * arata branch-ul curent
git status        # prima linie arata branch-ul
```

### "Vreau sa lucrez la o functie noua fara sa stric main"
```bash
git switch -c functie-noua     # creeaza branch si treci pe el
# ... lucreaza, fa commits ...
git switch main
git merge functie-noua
```

### "Colegul a modificat ceva pe GitHub si eu nu am ultima versiune"
```bash
git pull
```

### "Vreau sa vad ce s-a schimbat inainte sa commit"
```bash
git diff                  # modificari nestaged
git diff --staged         # modificari staged (dupa git add)
```

### "Am un conflict la merge"
```bash
# 1. Deschide fisierul cu conflict in VS Code
# 2. Cauta liniile cu <<<<<<, =======, >>>>>>>
# 3. Pastreaza ce vrei, sterge markerii
# 4. Salveaza fisierul
git add fisier.txt
git commit -m "resolve merge conflict"
```

### "Vreau sa vad istoricul scurt"
```bash
git log --oneline
```

### "Un fisier nu trebuie sa ajunga pe GitHub (parole, etc.)"
```bash
# Adauga numele fisierului in .gitignore
# ex: secret.txt sau *.env
# IMPORTANT: fara spatii inaintea regulilor
```

---

## Reguli de Aur

1. **Commit des** — instantanee mici si clare sunt mai utile decat unele mari
2. **Mesaje clare** — scrie CE ai facut, nu "modificari" sau "fix"
3. **Nu sterge .git** — este creierul repo-ului tau
4. **Verifica branch-ul** inainte sa incepi sa lucrezi (`git branch`)
5. **Foloseste git revert** in loc de comenzi distructive (`git reset --hard`)
6. **Nu pune secrete pe GitHub** — foloseste .gitignore pentru .env si parole
7. **git pull inainte de git push** — cand lucrezi in echipa

---

## Mesaje de Commit Bune vs. Proaste

| Bun | Prost |
|-----|-------|
| `add login page` | `stuff` |
| `fix typo in README` | `changes` |
| `update homepage layout` | `aaa` |
| `resolve merge conflict in header` | `done` |
| `add .gitignore for node_modules` | `git` |

---

## Vim — Cum Iesi (cand Git il deschide)

Git uneori deschide editorul Vim pentru mesaje de commit.
Daca esti blocat in Vim:

1. Apasa `Esc`
2. Tasteaza `:wq`
3. Apasa `Enter`

`:wq` = write (salveaza) + quit (iesi)

---

## Referinta Vizuala — Ciclul Git

```
[Fisiere modificate]
        |
     git add
        |
  [Staging Area]
        |
   git commit
        |
[Repo Local / istoric]
        |
    git push
        |
    [GitHub]
```
