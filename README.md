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
- `git commit -m "description"`

### --amend

- avant d'avoir envoyé un commit sur GitHub, il est possible de modifier le message qu'on lui a attaché 
- la commande `git commit --amend` va ouvrir un éditeur de texte dans lequel on va pouvoir modifier le message. 
  
---

## git log

- donne un aperçu du dépôt complet en listant les commits enregistrés et en donnant pour chacun des infos: 
  - le signataire du commit (pseudo github et son adresse mail)
  - la date du commit
  - le message du commit
  - le SHA-1 (identifiant) du commit

## git config 

- on utilise cette commande pour configurer le comportement du git
- on peut le faire au niveau du système avec l'option --global
- ou au niveau du dépôt dans lequel on se trouve (sans option)
- en fin de S1, on a configuré le user.name et le user.email afin de signer nos commits
- on peut également définir des alias pour les commandes un peu longue ou pénibles à taper 
  - `git config --global alias.tree 'log --greaph --online --all'`

---

