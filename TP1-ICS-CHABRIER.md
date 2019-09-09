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
