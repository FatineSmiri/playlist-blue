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

## git remote

- avec add, on donne une adresse distante où envoyer notre dépôt local

    - `git remote add origin (nom par défaut) git@github.com:xxx (adresse ssh du dépôt)`

- avec -v, on liste les adresses distantes enregistrées

    - `git remote -v`

---

## git push

- lors du 1er envoi, il faut lier la branche locale courante à une branche du dépôt distant

    - `git push --set-upstream (ou -u) origin (dépôt distant) master (branche distante)`

- lors des envois de mise à jour, git saura comment lier cette branche à une branche distante

    - `git push`

- On peut également pusher sur d'autres branches que la branche principale en indiquant le nom complet de la branche distante
  - `git push origin <nom_branche>`

---

## git branch

- depuis la branche courante, on peut créer une nouvelle branche ET rester dans la branche courante

- si on est sur la branche master, `git branch henriette` va créer la branche henriette mais on restera sur la branche master

    - `git branch <nom_branche>`
    - `git checkout <nom_branche>`

- Astuce : on peut créer une nouvelle branche et se positionner dessus directement

    `git checkout -b <nom_branche>`

- on peut supprimer une branche en local

    - avec un warning si la branche n'a pas été pushée sur la branche distante

        - `git branch -d <nom_branche>`

    - sans warning ni vérification

        - `git branch -D <nom_branche>`

---

## git checkout

- permet de se placer sur un commit avec son id ou sur une branche avec son nom

    - `git checkout f1529e320bb68d15aed5bb87ac625732c886709f` se place sur le commit indiqué (marche aussi avec la version courte de l'id)

    - `git checkout <nom_branche>` se place sur la branche indiquée

- permet aussi de remettre un fichier local dans le même état que sur la branche distante

    - `git checkout <nom_fichier>`

---

