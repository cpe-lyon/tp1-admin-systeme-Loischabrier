Loïs CHABRIER

# _TP 1 - Installation d’Ubuntu Server et prise en main du shell_

## Exercice 2

### _Manuel_
<br>
<span style='color:red'>1.</span> A l’aide du manuel, identifiez le rôle de la commande which </span>

La commande `which` sert à localiser une commande.

<span style='color:red'>2.</span> Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option? 

Lorsqu'on est sur la page `which`, il faut appuyer sur "`/`" puis taper `option`. Cela redirige automatiquement sur le mot `option`.

<span style='color:red'>3.</span> Comment quitte-t-on le manuel? 

Il suffit simplement d'appuyer sur la lettre `q`

<span style='color:red'>4.</span> Chaque section du manuel a une première page, qui présente le contenu de la section. 
Aﬀicher la première page de la section 6; 
De quoi parle cette section?

Cette section parle de `tout les programmes et jeux amusants qui existent sur le système`

<br>

### _Navigation dans l’arborescence des fichiers_
<br>

<span style='color:red'>1.</span> Allez dans le dossier /var/log

Entrer `cd /var/log/`

<span style='color:red'>2.</span> Remontez dans le dossier parent (/var) en utilisant un chemin relatif

Entrer `cd ..`

<span style='color:red'>3.</span> Retournez dans le dossier personnel

Entrer simplement `cd`

<span style='color:red'>4.</span> Revenez au dossier précédent (/var)

Entrer `cd /var/`

<span style='color:red'>5.</span> Essayez d’accéder au dossier /root; que se passe-t-il?

Le système nous refuse l'accès avec un `Permission denied`

<span style='color:red'>6.</span> Essayez la commande sudo cd /root; que se passe-t-il? Expliquez

Le système renvoie un `Command not found`. La commande `cd` fait partie intégrante du Bash, donc la commande `sudo` ne peut pas l'utiliser.

<span style='color:red'>7.</span> A partir de votre dossier personnel, créez l’arborescence suivante :

Entrer tout d'abord `cd` pour être sûr de retourner dans le dossier personnel.
Entrer `mkdir dossier1` puis `cd dossier1` puis `touch fichier1`

Entrer ensuite `cd ..` puis `mkdir dossier2` puis `cd dossier2` puis `mkdir dossier2.1 && mkdir dossier2.2` puis `cd dossier2.2` et enfin `touch fichier2 && touch fichier3`

<span style='color:red'>8.</span> Revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1; que se passe-t-il?

Le système nous renvoie `No such file or directory` puisque nous sommes pas dans le bon dossier pour supprimer le fichier1. Il nous faudrait spécifier le chemin absolu pour pouvoir le supprimer.

<span style='color:red'>9.</span> Quelle commande permet de supprimer un dossier?

Il faut utiliser `rmdir <nom dossier>`

<span style='color:red'>10.</span> Que se passe-t-il quand on applique cette commande à Dossier2?

Le système spécifie qu'il existe des choses dans le dossier2.

<span style='color:red'>11.</span> Comment supprimer en une seule commande Dossier2 et son contenu?

Il suffit d'utiliser `rm -r dossier2`

<br>

### _Commandes importantes_
<br>

<span style='color:red'>1.</span> Quelle commande permet d’aﬀicher l’heure? A quoi sert la commande time?

C'est la commande `date` qui permet d'afficher l'heure.
La commande `time` permet de déterminer le temps d'éxecution d'une commande.

<span style='color:red'>2.</span> Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point?

Les dossiers commençant par des points sont `des dossiers cachés`

<span style='color:red'>3.</span> Où se situe le programme ls?

Il est situé dans `/usr/bin/`

<span style='color:red'>4.</span> Que fait la commande ll? (indice : la commande alias peut vous aider) 

Elle liste les fichiers avec les droits qui leur sont associés.

<span style='color:red'>5.</span> Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier /bin? 

Si on est dans le dossier "bin", il suffit de faire un `ls`. Si on n'y est pas, il faut spécifier le chemin après le ls : `ls /usr/bin/`

<span style='color:red'>6.</span>  Que fait la commande ls ..? 

Elle permet de lister les fichiers et dossiers d'un répertoire.

<span style='color:red'>7.</span> Quelle commande donne le chemin complet du dossier courant?

La commande est `pwd`

<span style='color:red'>8.</span> Que fait la commande echo 'yo' > plop exécutée 2 fois?

La première fois elle écrit 'yo' dans le fichier 'plop' et la deuxième fois elle remplace le premier 'yo' par le deuxième.
Si on éxecute 10 fois cette commande, on n'aura qu'un seul 'yo' d'écrit dans 'plop'.

<span style='color:red'>9.</span> Que fait la commande echo 'yo' >> plop exécutée 2 fois?

Contrairement à la question du dessus, en utilisant 2 ">", au lieu de remplacer le 'yo' par un autre, cela en rajoute un. Si on éxecute 10 fois cette commande, on aura 'yo' écrit 10 fois dans 'plop'.

<span style='color:red'>10.</span> A quoi sert la commande file? Essayez la sur des fichiers de types différents

Elle permet de déterminer le type d'un fichier.

<span style='color:red'>11.</span> Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. 
Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?

Il faut tout d'abord exécuter la commande `echo 'Hello Toto !' > toto`. Ensuite, exécuter `ln toto titi` puis exécuter `echo 'Hello Toto2 !' > toto` pour changer le contenu du fichier "toto". Ensuite, en affichant le contenu du fichier "titi", on se rend compte qu'il est lié au fichier "toto" et que lorsqu'on modifie ce dernier, le fichier "titi" est modifié également.
Lorsqu'on supprime le fichier "toto", cela ne supprime pas le fichier "titi".


<span style='color:red'>12.</span> Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?

Lorsque l'on modifie le contenu de "titi", le contenu de "tutu" change également. En revanche, lorsque l'on supprime "titi", "tutu" est également supprimé.
Cela signifie qu'en rajoutant le `-s` pour créer le lien symbolique entre les 2 fichiers, ces derniers sont liés également pour la suppression.

<span style='color:red'>13.</span> Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?

Pour afficher le fichier /var/log/syslog/, il suffit d'exécuter la commande `cat /var/log/syslog`.
Pour naviguer librement dans le fichier, il faut rajouter "less" comme ceci : `cat /var/log/syslog | less`

<span style='color:red'>14.</span> Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.

 - 5 premières : `head -5 /var/log/syslog`
 - 15 dernières : `tail -15 /var/log/syslog`
 - Lignes 10 à 20 : `perl -ne'10..20 and print' /var/log/syslog`

<span style='color:red'>15.</span> Que fait la commande dmesg | less ?

La commande `dmesg` permet de voir l'historique des messages du noyaux. La commande `less` permet quant à elle de naviguer dans le fichier librement.

<span style='color:red'>16.</span> Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?

Le fichier `/etc/passwd` contient toutes les informations relatives aux utilisateurs (login, mots de passe, etc).
La commande permettant l'affichage de la page de manuel de ce fichier est `man passwd` pour afficher la première page du manuel et `man <numéro page> passwd` pour afficher une page en particulier.

<span style='color:red'>17.</span> Affichez seulement la première colonne triée par ordre alphabétique inverse

Pour se faire, il faut exécuter la commande `sort -r +0 /etc/passwd` où `sort` permet de trier les colonnes, `-r` permet de trier dans l'ordre alphabétique inverse et ou `+0` signifie que l'on veut seulement garder la première colonne.

<span style='color:red'>18.</span>  Quelle commande nous donne le nombre d’utilisateurs ?

1 utilisateur = 1 ligne, donc on compte le nombre de lignes avec `wc -l /etc/passwd` ce qui nous donne 31 lignes donc 31 utilisateurs.

<span style='color:red'>19.</span> Combien de pages de manuel comportent le mot-clé conversion dans leur description ?


<span style='color:red'>20.</span> A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine

Pour rechercher tous les fichiers se nommant "passwd" dans le système, il suffit d'entrer la commande `find -name 'passwd'`.

<span style='color:red'>21.</span> Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null

Pour stocker le retour de la commande find dans "~/list_passwd_files.txt" et que les erreurs soient envoyés sur "/dev/null", il faut utiliser la commande `find / -name 'passwd' > ~/list_passwd_files.txt 2>/dev/null`.
Le "2" devant ">" permet de préciser que ce sont les erreurs qyu doivent être envoyées dans "/dev/null".

<span style='color:red'>22.</span> Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment



<span style='color:red'>23.</span> Utilisez la commande locate pour trouver le fichier history.log.

Pour se faire, exécuter la commande `locate history.log`.
Le système nous retourne la localisation : "/var/log/apt/history.log"

<span style='color:red'>24.</span> Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?

Pour créer le fichier : `touch fichier` puis `locate fichier` pour le localiser.
Effectivement, rien n'apparaît quand on tente de le localiser. Cela vient du fait que la commande "locate" utilise une base de données pour retrouver l'emplacement. Cette base de données se rafraîchissant seulement toutes les 24h, le fichier créé à l'instant n'est pas connu. Il faut utiliser `updatedb` pour mettre à jour la base de données et pour voir que la commande `locate fichier` est désormais fonctionnelle.

## Exercice 3. Découverte de l’éditeur de texte nano

<span style='color:red'>1.</span> Copiez le fichier /var/log/syslog dans votre dossier personnel sous le nom log.txt, puis ouvrez-le avec nano

Pour copier le fichier : `sudo cp /var/log/syslog ~/log.txt`
Pour l'ouvrir avec nano : `nano ~/log.txt`
Pour tout faire en une seule commande : `sudo cp /var/log/syslog ~/log.txt && nano ~/log.txt`

<span style='color:red'>2.</span> Remplacez toutes les occurrences du mot kernel par le mot noyau

Pour remplacer avec nano : Entrer `CTRL + W` puis `CTRL + R`,taper ensuite le mot à remplacer (donc ici kernek), et pour finir taper le mot qui remplacera l'ancien (donc ici noyau)

<span style='color:red'>3.</span> Déplacer les 10 premières lignes à la fin du fichier

- Pour sélectionner les 10 lignes : `CTRL + ^` et se déplacer avec les flèches pour surligner les 10 lignes
- Faire un `CTRL + K` pour couper et descendre à la fin du fichier pour faire un `CTRL + U` pour coller.

<span style='color:red'>4.</span> Annulez cette action

Pour annuler, il suffit tout simplement de faire un `ALT + U`

<span style='color:red'>5.</span> Enregistrez le fichier avant de quitter nano

- Pour enregistrer le fichier : `CTRL + S`
- Pour quitter nano : `CTRL + X`
