
# RStudio: git init + Rproject + remote sur github


## Création du répertoire 

Dans le terminal de Rstudio:  

* Aller dans le répertoire qui accueillera le projet: 
  * `cd path` 
* Créer un répertoire (si possible sans espace pour facilité l'édition des commandes) 
  * `mkdir nom_repertoire`


 ## Initialiser git dans le répertoire

 Toujours dans le terminal: 

 *  `git init`

 ## Créer les premiers fichiers

Utiliser la commande **`touch`** (normalement installé pour le terminal de RStudio)

* `touch nom_fichier.extension`

Exemple pour un projet type Quarto 

```
touch index.qmd
touch _quarto.yml
touch .gitignore
```

On peut déjà faire un premier commit sur la création des fichiers

``` 
git add .
git commit -m "Ajout des premiers fichiers"
```


Si la commande touch n'est pas installée (je crois que c'est le cas pour les invites de commandes windows):  **`npm install -g touch-for-windows`**

## Créer un projet R

On peut faire cette étape au début c'est au choix.  

* Dans la console R, on charge le package usethis [`install_packages("usethis")`]
  * `library(usethis)`  

* On génère le projet avec la fonction **`create_project()`**

Ici par exemple: 

```
create_project(path = "C:/Users/thevenin_m/Desktop/rstudio_projet", open = TRUE, rstudio = TRUE)
```

Output de la console:

```
✔ Setting active project to 'C:/Users/thevenin_m/Desktop/rstudio_projet'
✔ Creating 'R/'
✔ Writing 'rstudio_projet.Rproj'
✔ Adding '.Rproj.user' to '.gitignore'
✔ Opening 'C:/Users/thevenin_m/Desktop/rstudio_projet/' in new RStudio session
✔ Setting active project to '<no active project>'
```

* RStudio va se recharger sur le nouveau projet
* On a un répertoire R qui a été généré, on peut le supprimer. Dans le terminal:
  * `rmdir R`


## Création d'un répertoire distant su github

* Editer le fichier .gitignore si besoin. Le répertoire *.Rproject.user* a déjà été ajouté à ce fichier. 

* Dans la console R, ca création du répertoire distant sur Github se fait pas la commande **`use_github()`** du package `usethis` (il faut le recharger)

```
library(usethis)
use_github()
```

* Selectionner 2 (yup) pour pusher le contenu du répertoire local













