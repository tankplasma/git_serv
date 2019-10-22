CONFIGURATION DE GIT


# s'enregistre dans .gitconfig de votre compte user
$gitconfig --global user.name Tony
$gitconfig --global user.email tony@tony.fr
# Définir un éditeur pour écrire le texte du commit# Normalement lors de l'installation automatique de Git# sous Window ou Mac un éditeur est déjà défini
$gitconfig --global core.editor vim
# pour un dépôt en particulier, dans le fichier config du dossier .git 
$gitconfig --local user.name Alan
$gitconfig --local user.email alan@alan.fr


GIT INIT


# pour initialiser le projet
git init
# Pour voir si tout fonctionne bien vous vous placerez dans le dossier versionné ettaperez la commande suivante
git status
# ajouter le fichier dans la zone d'index
git add
# commande pour desindexer le dossier
git rm --cached
# commande de Git qui permet de voir ce qu’il y a dansl’historique:linux
find .git/objects -type f
# cree des commit
# version courte
gitcommit -m "[motif]"
# équivalent, dans ce cas vous avez un éditeur qui s'ouvre ce dernier vous permet d'expliquer plus pécisémment ce que vous venez de faire
gitcommit
# visualiser les logs, voire les clefs de hachages et commit
git log
git log --oneline
git shortlog
# commande pour voir l'état de votre dépôt 
git status
# Ajoutez un ensemble de fichiers/dossiers ou modifs 
git add .
# ou de manière équivalent 
git add -A
# pour avoire toutes les commandes 
$ git help
 # voir alias dans la configuration
$ git log --oneline
# voir les différences entre deux branches
$ git log master..origin/master 
# 5 derniers commits
$ git log -5 
# log avec différence pour chaque commit sur les 5 derniers
$ git log -p -5 
# stat sur les modifs par commits
$ git log --stat # stat sur les modifs par commits
# depuis deux semaines, --until existe également
$ git log --since=2.weeks 
# Blame qui a fait la modif !
# rechercher qui a fait les modifs par ligne -L
$ git blame -L 40,60 readme.md 
# depuis 3 semaines avec auteurs des modifications
$ git blame --since=3.weeks -- readme.md
# recherche avec expression régulière
$ git blame -L "/^### /" readme.md 
# voir tout les fichiers suivis
git ls-files


RENOMER UN FICHIER


git mv mon_ancien_fichier mon_nouveau_fichier git status


