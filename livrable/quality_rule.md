# Commandes
| Probleme                                                             | Résolution                                                                                                                                                                                                              |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| + d'une ligne nom colonne                                            | Supprimer les lignes en surplus                                                                                                                                                                                         |
| ligne du csv en double                                               | Supprimer les lignes en double                                                                                                                                                                                          |
| ligne avec une colonne null/vide ou ne respectant pas le format des  | 1. retrouver dans le ficher correction de la journée la ligne a corriger <br> 2. retrouver dans les cas en dessous une resolution <br> 3. mettre la ligne dans le ficher "lignes corrompues" avec le probleme si trouvé |

### Commandes_id
| Probleme     | Résolution |
|--------------|------------|
| valeur null  | pass       |
### Client_id

| Probleme            | Résolution                                                                                                                                                        |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valeur parfois null | la ligne qui provient d'une commande qui possede d'autre ligne avec le client_id, possibilité de compléter |

### produit_id
| Probleme      | Résolution |
|---------------|------------|
| valeur null   | pass       |

### categorie
| Probleme                                                                        | Résolution                                 |
|---------------------------------------------------------------------------------|--------------------------------------------|
| valeur null                                                                     | retrouver la catégorié via l'id du produit |
| espace avant la valeur                                                          | enlever cette espace                       |
| valeur sous differente forme ex :<br> -" blabla" <br> -"Blabla" <br> -"blabla"  | Mettre les donnée en format snake_case     | 

### quantite
| Probleme             | Résolution                            |
|----------------------|---------------------------------------|
| valeur null          | retrouver le nombre via le produit_id |
| valeur négatif       | retrouver le nombre via le produit_id |
| valeur non numérique | retrouver le nombre via le produit_id |

### prix_unitaire
| Probleme          | Résolution                                                                                                                                                       |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valeur négatif    | 1. retrouver dans le ficher correction de la journée <br> 2. retrouver la valeur via l'id du produit <br> 3. mettre dans un fichier avec explication valeur null |
| valeur null       | retrouver la valeur via l'id du produit                                                                                                                          |
| valeur sans point | vérifier que la valeur dans la colonne devise est un nombre remplacer la prochaine virgule par un point                                                          | 

### devise
| Probleme             | Résolution                                                                                                   |
|----------------------|--------------------------------------------------------------------------------------------------------------|
| valeur null          | si. retrouver la valeur via l'id du produit <br> sinon.  mettre dans un fichier avec explication valeur null |
| valeur diff de "EUR" | convertir prix unitaire vers EURO                                                                            |

### statut
| Probleme          | Résolution |
|-------------------|------------|
| valeur null       | pass       |

### horodatage_commande
| Probleme                                      | Résolution |
|-----------------------------------------------|------------|
| valeur non sous la forme :aaaa-MM-jjThh:mm:ss | pass       |

# annulations
| Probleme                     | Résolution                                                                                                                                                                                                              |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| + d'une ligne nom colonne    | Supprimer les lignes en surplus                                                                                                                                                                                         |
| ligne du csv en double       | Supprimer les lignes en double                                                                                                                                                                                          |
| ligne dans avec un null/vide | 1. retrouver dans le ficher correction de la journée la ligne a corriger <br> 2. retrouver dans les cas en dessous une resolution <br> 3. mettre la ligne dans le ficher "lignes corrompues" avec le probleme si trouvé |

### annulation_id
| Probleme          | Résolution |
|-------------------|------------|

### commande_id
| Probleme          | Résolution |
|-------------------|------------|
| valeur null       | pass       |

### ligne_id
| Probleme          | Résolution |
|-------------------|------------|
| valeur null       | pass       |

### type
| Probleme          | Résolution |
|-------------------|------------|

### motif
| Probleme                                                                        | Résolution                             |
|---------------------------------------------------------------------------------|----------------------------------------|
| valeur sous differente forme ex :<br> -" blabla" <br> -"Blabla" <br> -"blabla"  | Mettre les donnée en format snake_case |

### quantite

### montant_rembourse
| Probleme          | Résolution                                                                                                                                                       |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valeur négatif    | 1. retrouver dans le ficher correction de la journée <br> 2. retrouver la valeur via l'id du produit <br> 3. mettre dans un fichier avec explication valeur null |
| valeur null       | retrouver la valeur via l'id du produit                                                                                                                          |
| valeur sans point | vérifier que la valeur dans la colonne devise est un nombre remplacer la prochaine virgule par un point                                                          | 

### horodatage_annulation

# consultation
### session_id
### client_id
### produit_id
### categorie
### url
### horodatage_vue
### horodatage_commande
| Probleme                                      | Résolution |
|-----------------------------------------------|------------|
| valeur non sous la forme :aaaa-MM-jjThh:mm:ss | pass       |


