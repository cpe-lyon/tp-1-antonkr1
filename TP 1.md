# TP 1
## _Exercice 2 : Prise en main_
-Le manuel  
1- Le manuel s’ouvre avec l’option “man” devant la commande voulant être étudié, dans notre cas which : man which. Which permettant d'afficher le chemin d'accès à un executable donné  
2-  Pour chercher un terme précis il suffit de faire un /”terme” une fois entré dans le manuel.   
 3-  Pour quitter le manuel il suffit de faire q.  
4- En faisant man 6 intro (6 étant la section recherché), cette section correspond aux descriptions de fonctionnalités amusantes / jeux disponibles.  

-Navigation dans l'arborescence des fichers 

1- Pour acceder à un dossier il faut utiliser la commande cd suivi de l'arborescence du dossier cherché, exemple cd /var/log.  
2- Il suffit de faire cd ..  
3- Pour avoir accès au dossier personnel il suffit de faire cd
4- le complément ".." permet d'aller dans le dossier parent (cd ..), pour retourner dans le dossier précédent il suffit d'ajouter "-" en argument à la commande cd  
5- En essayant d'avoir accès au dossier /root ça me retourne "/root : Is a directory", je n'ai simplement pas les droits en tant que simple "user" pour y accéder.  
6- L'utilisation de la commande sudo permettant d'executer un executable en tant que super admin or en utilisant sudo pour avoir accès à un dossier : sudo cd /root, c'est la commande cd est une commande "builtin", elle n'apparait donc pas dans les commandes executables par sudo. Il faut donc être directement connecté en tant que superuser avec un -sudo par exemple pour y avoir accès.  
8/9- La commande rm "nom du fichier" permet de supprimer un fichier, il n'est néanmoins pas possible de supprimer un dossier avec cette même commander, il faut utiliser rmdir "nom du dossier".  
10/11- Il est impossible de supprimer un dossier qui n'est pas vide avec la commande rmdir mais en utilisant l'argument r à la commande rm (rm -r "nomdudossier").  


-Commandes importantes

1- La commande "Date" permet d'afficher le jour et l'heure, la commande "Time" permet d'afficher combien de temps prend une commande / utilisateur  
2- La commande "*ls*" permet d'afficher tout les fichiers / dossiers du répertoire dans lequel on se trouve, en faisant "*la*" ou "*ls -a*" on voit apparaitre des fichiers avec un . devant, des fichiers cachés.  
3- Le programme "*ls*" se trouve dans le dossier /bin avec les exécutables et binaires essentiels.  
4- "*ll*" permet d'afficher les différents droits affectés aux fichiers / dossiers du répertoire.  
5- "*ls /bin*" permet d'afficher le contenu du dossier /bin    
6- "*ls ..*" permet d'afficher qui est dans le dossier    
7- "*readlink -f (nom du dossier/fichier)*" permet d'afficher le chemin complet vers le dossier/ficher cherché.  
8- "*echo 'bip' > plop*" exécutée 2 fois créer un fichier text "plop" dans lequel on retrouve "bip" une seule fois  
9- "*echo 'bip' >> plop*" exécutée 2 fois créer un ficher text "plop" comme précédemment seulement, à chaque exécution de la commande un nouveau "bip" est ajouté au fichier texte ce qui n'était pas le cas avec la. commande précédente.  
10- "*sleep 10 | echo 'toto'*"permet afficher 'toto' pour ensuite mettre en pause l'invite de commande pendant 10 secondes avec sleep 10.  
11- "file" permet de déterminer le type de ficher d'un ficher  
12- Le "lien_phy" va avoir le même contenu que le fichier "original" même après modification et suppression du fichier.  
13- Le "lien_sym" va avoir le même contenu que le fichier "lien_phy" même après modification, sauf qu'après suppression de "lien_phy" "lin_sym" n'est plus accessible.  
14- ctrl s va mettre en pause le défilement de la commande jusqu'à l'utilisation de ctrl q pour relancer le défilement.  
15- head x "nom du fichier" permet d'afficher les x premieres lignes du contenu d'un fichier texte.    
- Pour les dernieres lignes d'un fichier c'est la même chose que head mais en utilisant tail    
16- mesg | less permet d'afficher "mesg" une page à la fois.  
17- Le fichier /etc/passwd contient tout les renseignements concernant les utilisateurs. Il faut faire man passwd pour afficher le manuel du fichier.    
18- Il faut utiliser "sort" pour trier les données d'un fichier texte, sort va par defaut trier dans l'ordre alphabétique et il faut ajouter l'argument -r pour inverser la commander et donc trier dans l'ordre alphabétique inverse.  
19- En utilisant wc -l /etc/passwd on affiche le nombre de lignes du fichier et donc le nombre d'utilisateur à savoir 34.    
20- En utilisant "man --k conversion | wc --l" j'ai trouvé 141 pages.  
21- La commande "find / -name 'passwd'" permet de trouver tout les fichiers s'appelant "passwd".  
22- J'ai utilisé "find / -name 'passwd' 2>&1 ~/list_passwd_files.txt", puis "find / -name 'passwd'2> /dev/null" pour rediriger les erreurs.  
23- J'ai utilisé "grep --r ls --alF *"* pour retrouver l'alias ll.  
24- J'ai pu trouvé ce fichier via "locate history.log".  
25- Il n'apparait pas étant donné que je me trouve déjà à l'endroit où il se trouve.    
## _Exercice 4 : Personnalisation du shell_  
1- J'ai créé une copie du .bashrc via grace à la commande cp : "cp ~/.bashrc .bashrc_bak"  
2- J'ai simplement supprimé le "#" devant "force_color_prompt=yes" pour le decommenter, j'ai ensuite enregistré la modification.  
3- Après l'execution de "source .bashrc" la couleur a changé.  








xargs permet de passer une commande en entrée standard en argument ex : cat fichier1 | xargs rm, cat permettant d'afficher les fichiers du dossier et rm les supprimer. 
