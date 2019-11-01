CONSULTER L'HISTORIQUE ET LES MODIFS 
# consulter les commits d’un auteur en particulier :
git log --author " "
# consulter l’historique :
git log --since=1.day 
git log --before="2019-09-01"
# consulter l’historique d’un fichier uniquement :
git log [fichier]
# visualiser les modifications au sein d’un fichier ou de l’ensemble/d’un ensemble des fichier(s) : 
git log -p [fichier]
# Dans l'ensemble des commits 
git log -p
# Ou pour les 2 derniers commits 
git log -2 -p
# visualiser les changements ligne par ligne :
git log -p --word-diff [fichier]
# visualiser les statistiques des modifications des fichiers :
git log --stat [fichier]
# visualisation du graphe du dépôt :
git log --pretty=format:"%h %s" --graph
# permet de rechercher des logs: E expression pour recherche les/l’occurence(s) et i pour insensible à la casse (majuscule/minuscule) :
git log -E -i --grep='Pizza'
# savoir qui a fait la modification
git blame calzone.tx
# visualiser les modifications : 
git diff
# La commande git diff affiche les modifications avant l’indexation. l’option –cached permet de visualiser les modifications de votre fichier avec le dernier commit :
git diff --cached
# voir les modifications un commit en arrière : HEADˆ1 pour reculé d’un commit en arrière
git diff HEAD~1
# Récupérez les haches des deux derniers commits 
git log --oneline
# Et étudier les différences entre deux commits 
git log 
# faire des stat sur les différences opérées dans les fichiers:
git diff --stat # [fichier] | 2 +-
# Changements dans le répertoire de travail qui ne sont pas encore dans l’index.
git diff --cached
# Changements dans l’index et le fichier dans l’espace de travail.
git HEAD
# rremettre le dépôt dans l’état dans lequel il se trouvait juste avant la modification :
git restore [fichier]
# si on refait la modification et que l’on ajoute le fichier dans l’index : 
git restore --staged
# Permet de fusionner les derniers changements au dernier commit :
git commit --amend --no-edit
# Annule le dernier commit et met tout dans le WD sans perte (revient au commit précédent -1 
git reset HEAD~1
# Annule le dernier commit et met tout dans la staging area sans perte 
git reset --soft HEAD~1
# Annule le dernier commit et supprime les modifications...(danger)
$ git reset --hard HEAD~1 git 
# Permet de revenir avant la refonte
$ git checkout [9b85968] [fichier]
