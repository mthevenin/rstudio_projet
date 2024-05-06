
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


Si la commande touch n'est pas installée (je crois que c'est le cas pour les invites de commandes windows):  **`npm install -g touch-for-windows`**






