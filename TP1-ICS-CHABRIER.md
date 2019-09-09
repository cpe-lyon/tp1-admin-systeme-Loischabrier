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
