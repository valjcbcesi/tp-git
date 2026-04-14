# TP Git et GitHub

## Présentation du projet DevOps
Ce repository a été créé dans le cadre d'un TP d'initiation à Git et GitHub.

### Installation de Git
Sur Windows :
Télécharger et installer https://gitforwindows.org/

### Liens utiles
Voici les pages de documentation officielle utilisées pour ce TP :
Documentation officielle de Git https://git-scm.com/docs
Générer une clé SSH pour GitHub https://docs.github.com/fr/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

### Commandes réalisées
Voici un tableau récapitulatif des commandes Git utilisées tout au long de ce TP :

| Commande | Description |
|---|---|
| `git init` | Initialise un nouveau dépôt Git en local. |
| `git branch -M main` | Renomme la branche par défaut en `main`. |
| `git checkout -b develop` | Crée une nouvelle branche nommée `develop` et bascule dessus. |
| `git add .` | Ajouter le contenu du fichier à l'index. |
| `git commit -m "Message"` | Crée un commit avec les fichiers préparés et un message descriptif. |
| `git push -u origin <branche>`| Envoie la branche locale vers le dépôt distant GitHub. |
| `git checkout main` | Permet de basculer sur la branche `main`. |
| `git merge develop` | Fusionne les modifications de la branche `develop` vers la branche actuelle. |
| `git rm <fichier>` | Supprime un fichier et prépare cette suppression pour le prochain commit. |

---
Diagramme du flow de commit
---

gitGraph
    commit id: "Initialisation"
    branch develop
    checkout develop
    commit id: "Création file1, file2, file3"
    checkout main
    merge develop id: "Premier merge sur main"
    checkout develop
    commit id: "Renommage file1, suppression file3"
    commit id: "Ajout du README"
    checkout main
    merge develop id: "Merge final sur main"