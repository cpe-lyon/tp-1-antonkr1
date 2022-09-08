# TP 1
## _Partie 2 : Prise en main_
-Le manuel
- Le manuel s’ouvre avec l’option “man” devant la commande voulant être étudié, dans notre cas which : man which. Which permettant d'afficher le chemin d'accès à un executable donné
-  Pour chercher un terme précis il suffit de faire un /”terme” une fois entré dans le manuel. 
 - Pour quitter le manuel il suffit de faire q.
- En faisant man 6 intro (6 étant la section recherché), cette section correspond aux descriptions de fonctionnalités amusantes / jeux disponibles

-Navigation dans l'arborescence des fichers 

- Pour acceder à un dossier il faut utiliser la commande cd suivi de l'arborescence du dossier cherché, exemple cd /var/log.
- Pour avoir accès au dossier personnel il suffit de faire cd
- le complément ".." permet d'aller dans le dossier parent (cd ..), pour retourner dans le dossier précédent il suffit d'ajouter "-" en argument à la commande cd
- En essayant d'avoir accès au dossier /root ça me retourne "/root : Is a directory", je n'ai simplement pas les droits en tant que simple "user" pour y accéder.
- L'utilisation de la commande sudo permettant d'executer un executable en tant que super admin or en utilisant sudo pour avoir accès à un dossier : sudo cd /root, c'est la commande cd est une commande "builtin", elle n'apparait donc pas dans les commandes executables par sudo. Il faut donc être directement connecté en tant que superuser avec un -sudo par exemple pour y avoir accès.
- La commande rm "nom du fichier" permet de supprimer un fichier, il n'est néanmoins pas possible de supprimer un dossier avec cette même commander, il faut utiliser rmdir "nom du dossier".
- Il est impossible de supprimer un dossier qui n'est pas vide avec la commande rmdir mais en utilisant l'argument r à la commande rm (rm -r "nomdudossier").


-Commandes importantes

- La commande "Date" permet d'afficher le jour et l'heure, la commande "Time" permet d'afficher combien de temps prend une commande / utilisateur 