Lien vers ressources git en françcais : 

https://www.christopheducamp.com/2013/12/15/github-pour-nuls-partie-1/

https://www.christopheducamp.com/2013/12/16/github-pour-nuls-partie-2/


/*/////////////////////////////////////////////
	    Etape à suivre dans le terminal
////////////////////////////////////////////*/


mkdir ~/GitProject  : 

mkdir est le raccourci de “make directory”. Ce n’est en réalité pas une ligne de commande Git, mais une commande générale de navigation provenant du temps avant les interfaces ordinateurs visuelles. Le ~/ veille à vous assurer de construire le repository au niveau supérieur de la structure de fichiers de notre ordinateur, au lieu d’un répertoire coincé dans quelque autre répertoire qui serait plus difficile à retrouver. En fait, si vous saisissez ~/ dans la fenêtre de votre navigateur, cela vous ramènera vers le répertoire local le plus haut de votre ordinateur. 

cd ~/GitProject  : 

cd signifie change directory, et c’est aussi une commande de navigation. Nous venons de produire un répertoire, et nous voulons maintenant passer à ce répertoire et aller dedans. Une fois que nous avons tapé cettte commande, nous sommes transportés à l’intérieur de MonProjet.
Maintenant, nous allons pour finir utiliser une commande Git. Saisissez :

git init :  

Vous savez que vous utilisez une commande Git car elle démarre toujours par git. Init signifie “initialiser”. Les deux précédentes commandes que nous avons saisies étaient des termes généraux de ligne de commande. Quand nous tapons ce code à l’intérieur, cela dit à l’ordinateur de reconnaître ce répertoire comme un dépôt local Git. Si vous ouvrez le répertoire, il ne s’affichera pas différemment, parce que ce nouveau répertoire Git est un fichier caché à l’intérieur du dépôt dédié.
Cependant, votre ordinateur sait maintenant que ce répertoire est prêt-pour-git, et vous pouvez commencer à entrer des commandes Git. Maintenant, vous avez à la fois un dépôt local et un repo en ligne pour votre projet.

touch Readme.md  : 

Permet de créer un fichier Readme.md dans le dossier GitProject.

git status  :  

La ligne de commande, généralement passive jusqu’à ce stade, vous renvoie quelques lignes de texte.
On est sur la branche master. Le fichier est répertorié comme untracked, ce qui signifie que Git l’ignore pour l’instant. Il faut l’ajouter. 

git add Readme.md  :

Remarquez comment la ligne de commande vous glisse un truc ici ? Très bien, nous avons ajouté notre premier fichier, aussi est-il temps à ce stade de prendre un “instantané” du projet, ou de le “consigner” :



git commit -m "Ajout Readme.md »  : ajouter un titre au commit


git remote add origin https://github.com/Virginie3377/GitProject.git  : 

Connecter Votre Dépôt Local À Votre Dépôt GitHub
La première partie est connue ; nous avons déjà utilisé git add avec les fichiers. Nous avons ajouté après le mot origin pour indiquer un nouvel endroit à partir duquel viendront les fichiers. remote est un descripteur de origin, pour indiquer que l’original n’est pas sur l’ordinateur, mais quelque part en ligne.
Git sait désormais qu’il existe un dépôt distant et que c’est là où vous voulez envoyer vos modifications du dépôt local. Pour confirmer, saisissez cela pour déposer :

$ git remote -v

Maintenant, nous voulons téléverser, ou “push“er, nos modifications vers le dépôt distant Github. C’est facile. Tapez simplement :


$ git push
# GitProject
