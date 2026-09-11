LABORATOIRE 1 - GESTION DE VERSION ET COLLABORATION

Équipe :
Membre A : Rayane    (ALIR21030500)
Membre B : Allglory   (ADIA23010300)

URL: 
Partie 1
https://github.com/Ryan540gh/repo-gei311-lab1-Rayane.git
Partie 2 — Situation 1
https://github.com/Ryan540gh/repo-gei311-lab1-partie2-Rayane.git
Partie 2 — Situation 2
https://github.com/Ryan540gh/repo-get311-lab1-partie2-2-Rayane.git



1. RÉSUMÉ DE CE QUE NOUS AVONS APPRIS

Ce laboratoire nous a surtout permis de mieux comprendre comment Git fonctionne, parce qu'avant de commencer on connaissait pas vraiment Git et GitHub. On avait déja vu le principe de gestion de version, mais pas vraiment comment l'utiliser en pratique.

On a appris a faire un clone d'un repository, à travailler avec les fichiers, faire des add, des commit et ensuite envoyer les changements sur GitHub avec push. 
La partie sur les branches nous a aussi permis de comprendre pourquoi on utilise pas directement la branche principale pour tout faire. On a pu créer une branche pour travailler séparément, faire nos modifications dessus et ensuite la fusionner avec la branche main.

On s'est aussi rendu compte que les commits sont vraiment important. Au début on voyait surtout le commit comme une étape pour sauvegarder notre travail, mais avec les exercices on a compris que ça permet aussi de voir l'historique et de revenir à une ancienne version quand il y a un problème.

On a eu quelques problèmes pendant le laboratoire, surtout avec les permissions GitHub et la configuration de notre compte Git. Ça nous a permis de comprendre que même si le commit fonctionne sur notre ordinateur, ça veut pas forcément dire que le push va fonctionner sur GitHub.

Au final, on comprend mieux la logique générale de Git et surtout comment l'utiliser pour travailler à plusieurs sans modifier directement le travail de l'autre.

2.  GIT CHEAT-SHEET

 git init 
Commande :git init
Utilité :Initialise un nouveau repository Git dans le dossier actuel.

--- git clone ---
Commande  : git clone URL_DU_REPOSITORY
Utilité :Crée une copie locale d'un repository GitHub sur l'ordinateur.
Argument :URL_DU_REPOSITORY : adresse du repository GitHub à cloner.

git status 
Commande :git status
Utilité :Affiche l'état actuel du repository. 

git add 
Commande :git add .
Utilité :Ajoute tous les nouveaux fichiers et toutes les modifications à la zone de préparation du prochain commit.
Argument : représente les fichiers du dossier actuel et de ses sous-dossiers.

 git commit 
Utilité :Enregistre les modifications préparées dans l'historique local de Git.
Argument :-m : permet d'indiquer directement le message du commit.
Le message doit décrire clairement les modifications effectuées.

--- git push 
Commande utilisée :git push origin main
Utilité :Envoie les commits locaux vers le repository distant GitHub.
Arguments :origin : nom donné au repository distant.
main : branche sur laquelle les commits sont envoyés.

--- git pull 
Commande :git pull origin main
Utilité :Récupère les dernières modifications de la branche main du repository distant et les intègre dans le repository local.
Arguments :origin : repository distant. main : branche à récupérer.

--- git fetch 
Commande :git fetch
Utilité :Récupère les informations et les nouvelles références disponibles sur le repository distant sans 
les fusionner directement dans la branche actuelle.

--- git branch 
Commande :git branch
Utilité :Affiche les branches locales du repository. Le symbole * indique la branche actuellement utilisée.

--- git branch --show-current ---
Commande :git branch --show-current
Utilité :Affiche uniquement le nom de la branche actuellement utilisée.

--- git checkout -b ---

Utilité :Crée une nouvelle branche et se déplace immédiatement sur cette nouvelle branche.
Argument :-b : indique qu'une nouvelle branche doit être créée.

--- git checkout ---
Commande :git checkout main
Utilité :Permet de se déplacer sur une branche existante. 
Dans cet exemple, la commande permet de revenir sur la branche principale main.

--- git log ---
Commande :git log --oneline
Utilité :Affiche l'historique des commits sous une forme courte.
Argument :--oneline : affiche chaque commit sur une seule ligne avec son identifiant abrégé et son message.

--- git log avec graphique ---
Commande :git log --graph --oneline --all --decorate
Utilité :Affiche l'historique des commits sous forme graphique.
Arguments :
--graph : représente graphiquement les branches et leur historique.
--oneline : affiche chaque commit sur une seule ligne.
--all : affiche l'ensemble des branches.
--decorate : affiche les noms des branches et les références associées aux commits.

--- git revert 
Utilité :Permet d'annuler les modifications introduites par un ancien commit en créant un nouveau commit.
Argument :
48b540f : identifiant du commit dont les changements doivent être annulés.
Cette commande permet de conserver l'historique des changements.

--- git reset --hard 
Commande :git reset --hard ID_DU_COMMIT
Utilité :Replace la branche locale sur le commit indiqué et met les fichiers du répertoire de travail dans l'état correspondant à ce commit.
Arguments :
--hard : applique le changement à l'index et aux fichiers du répertoire de travail.
ID_DU_COMMIT : identifiant du commit vers lequel revenir.
Cette commande doit être utilisée avec prudence, car des modifications locales peuvent être perdues.

--- git remote add origin 
Commande :git remote add origin URL_DU_REPOSITORY
Utilité :Associe un repository Git local à un repository distant, par exemple un repository créé sur GitHub.
Arguments :origin : nom donné au repository distant.
URL_DU_REPOSITORY : adresse du repository GitHub.

--- git remote -v ---
Commande :git remote -v
Utilité :Affiche les repositories distants associés au repository local et leurs adresses.


git switch -c NOM_BRANCHE
Utilité: Permet de créer une nouvelle branche et de se placer directement dessus.

git merge NOM_BRANCHE
Utilité: Permet de fusionner une branche avec la branche sur laquelle je me trouve.

3. RETOUR D'EXPÉRIENCE SUR LES ISSUES

Pour nous, une Issue sert surtout à signaler  un problème pour que l'autre personne puisse comprendre ce qui se passe et savoir quoi chercher.

Après l'exercice, on trouve qu'un bon issue doit avoir un titre assez simple qui permet de comprendre directement le problème. 
Ensuite, il faut expliquer ce qui ne va pas, dans quel fichier ou quelle partie du projet, et si possible comment reproduire le problème.

Il faut aussi dire ce qu'on devrait normalement avoir à la place. Ça évite que la personne qui va corriger le problème doive deviner ce qui était attendu.

La structure qu'on trouve la plus logique est donc :
- le problème
- l'endroit où le problème se trouve
- les étapes pour le reproduire
- le résultat obtenu
- le résultat attendu

Une Issue mal décrite peut faire perdre du temps, parce que l'autre membre doit revenir poser plusieurs questions. 
Au contraire, une Issue claire permet de savoir plus rapidement quoi vérifier et quoi corriger.





