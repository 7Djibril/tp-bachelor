﻿# tp-bachelor
 ## Objectif
Créer un projet Git local et distant tout en se familiarisant avec les commandes principales de Git : clone, remote, pull, add, commit, push, résolution de conflits, etc.

## Étapes Réalisées
1. **Cloner le dépôt initial**
Commande utilisée :
git clone https://github.com/cecilev-axe/tp-bachelor.git
**Résultat :** Le dépôt a été cloné localement.
Vérification avec :
ls
### 2. **Changer l’origine du dépôt**
Commande utilisée :
git remote set-url origin https://github.com/7Djibril/tp-bachelor.git
Vérification avec :
git remote -v**Résultat attendu :**

origin  https://github.com/7Djibril/tp-bachelor.git (fetch)
origin  https://github.com/7Djibril/tp-bachelor.git (push)
### 3. **Ajout d'une fonctionnalité : une quatrième image**
Modifications effectuées :
- Ajout d'une quatrième image dans le fichier HTML.
- Mise à jour du fichier CSS pour le dot correspondant.

Commande pour vérifier l'état des modifications :
git status

Commande pour ajouter les modifications :
git add .

Commande pour enregistrer les modifications :
git commit -m "Ajout d'une quatrième image et d'un dot"
### 4. **Pousser les modifications vers le dépôt distant**
Commande utilisée :
git push origin main
**Résultat attendu :** Les modifications sont visibles sur GitHub.
### 5. **Gestion d’un conflit**
#### Situation :
- Le fichier `css/style.css` a été modifié sur GitHub (dots passés à 20px).
- En local, les dots ont été modifiés pour passer à 25px.
#### Étapes :
1. Récupération des modifications distantes :
   git pull origin main
   **Conflit détecté :**
   CONFLICT (content): Merge conflict in css/style.css
2. Résolution du conflit :
   - Ouvrir le fichier `css/style.css`.
   - Résoudre le conflit en choisissant la version locale ou en combinant les deux modifications.
**Exemple après résolution :**
   .dot {
       width: 25px;
       height: 25px;
       border-radius: 50%;
       background-color: #000;
   }

3. Marquer le conflit comme résolu :
   git add css/style.css
4. Committer la résolution :
bash   git commit -m "Résolution du conflit sur la taille des dots"
5. Pousser les modifications résolues :

   git push origin main
### 6. **Documentation des actions**
Création de ce fichier `README.md` pour détailler toutes les étapes, commandes utilisées et résultats obtenus.

Commande pour ajouter et commit le fichier :
git add README.md
git commit -m "Ajout du fichier README.md avec documentation"
Commande pour le pousser sur GitHub :
git push origin main

## Résultats de `git log`
Exemple d'historique des commits :
fa5a319 Résolution du conflit sur la taille des dots
490e452 Ajout d'une quatrième image et d'un dot
5cf1cdf Initial commit depuis le dépôt cloné
## Résultats de `git status` (à chaque étape clé)
### Après ajout de la quatrième image :
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html
        modified:   css/style.css

## Difficulté rencontré 
Mauvais modification de l'url donc pas push dans mon github
Conflit pas trouvé des le depart car pas bien modifier dans le css
Gestion du temps
Problème lors de l'entré du token




