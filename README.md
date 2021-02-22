# Commandes GIT

## git init

- initialise le répertoire courant comme dépôt git 
- création du dossier .git contenant les infos nécessaires à la gestion de l'historique 
  
---

## git status

- donne l'état du dépôt à un moment donné 
- on a des infos sur la branche courante, sur l'état des fichiers du projet et souvent une indication de la prochaine commande à réaliser

--- 

## git add

- ajout d'un ou plusieurs fichiers dans la zone de surveillance
  - `git add README.md` ajoute le fichier README.MD
  - `git add README.md .gitignore` ajoute les fichiers listés
  - `git add .` ajoute tous les fichiers en attente à chaque modification; on doit ajouter la nouvelle version du fichier dans la zone de surveillance

---

## git rm --cached

- retire un ou plusieurs fichiers de la zone de surveillance 
  - `git rm --cached .gitignore`

## git commit 

- enregistre dans l'histoire une version de l'application
- on va effectuer le commit pur marquer une étape du développement

---
