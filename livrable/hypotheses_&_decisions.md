# Règles métier à définir

## comment calculer le chiffre d'affaires net (prix, quantité, devise, annulation partielle ou totale, retour) ;

## quelle clé identifie de manière unique une ligne de commande, et comment traiter les doublons ;
une ligne de commande possede un clé composer de commande_id et ligne_id 

## que faire des lignes invalides ou incomplètes 
il faut faire un pretraitement avec les regle definie dans fichier quality_rule

## que faire d'une annulation orpheline ;
mettre la ligne dans un fichier annulation orpheline qui sera traité humainement le jour suivant pour le traitement prochain

## à quelle journée rattacher une annulation (celle de la commande ou celle de l'annulation) ;
la journée doit etre celle de l'annulation vu que l'annulation fait reference a la commande qui posses sa propre date

## comment classer les événements tardifs ;
ils seront pris en compte pour le prochain traitement

## que faire si un flux est absent ou incomplet au moment du traitement ;
continuer le traitement, envoyer une alerte et attendre l'envoie d'un flux à n'importe qu'elle moment de la journée et faire le traitement dès que possible. 

## comment départager les produits à égalité dans le top 5 ;
comparer les egalité par rapport au nombre de commande 

## quelles données peuvent apparaître dans les sorties.

1. le chiffre d'affaires net par catégorie :

| categorie | CA net |
|-----------|--------| 

2. le nombre de commandes par catégorie ; 

| categorie | nbr commande | 
|-----------|--------------|

3. les cinq produits les plus consultés par catégorie ;

| produit | catégorie | nbr consultation | placement | 
|---------|-----------|------------------|-----------|


4. une liste des anomalies de données à examiner.

 | nom fichier | clé ligne | colonne concernée | message explicité |
 |-------------|-----------|-------------------|-------------------|