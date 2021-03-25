# Géocodage de la table des émissions du Registre des émissions polluantes

Le registre national des Émissions Polluantes est une base de donnée maintenue par
la Direction Générale de la Prévention des Risques du Ministère de l’Ecologie, 
du Développement Durable, et de l’Energie, qui recense les principaux rejets et 
transferts de polluants déclarés par :

- les principales installations industrielles,
- les stations d'épuration urbaines de plus de 100 000 équivalents habitants,
- certains élevages

Elle est disponible sur le site [Géorisques](https://www.georisques.gouv.fr/donnees/bases-de-donnees/installations-industrielles-rejetant-des-polluants), sous 
[Licence Ouverte](https://www.etalab.gouv.fr/wp-content/uploads/2014/05/Licence_Ouverte.pdf)

Ce projet s'interesse en particulier à la table des émissions de cette base de données.
Cette table contient des informations géographiques sur les établissements émetteurs,
mais ces informations sont difficiles à exploiter et peu fiables. 

Nous essayons donc de les améliorer, en particulier pour un usage cartographique en testant plusieurs méthodes, grâce à :

- l'[API de la Base Adresse Nationale](https://api.gouv.fr/les-api/base-adresse-nationale), 
sous [Licence Ouverte version 2.0](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf),
- la [Base SIRÈNE](https://www.data.gouv.fr/fr/datasets/base-sirene-des-entreprises-et-de-leurs-etablissements-siren-siret/) sous [Licence Ouverte version 2.0](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf)
- la [Base officielle des codes postaux](https://www.data.gouv.fr/fr/datasets/base-officielle-des-codes-postaux/) sous licence [ODbL](http://opendatacommons.org/licenses/odbl/summary/).

Ces données sont mises à jour au moment de générer le fichier corrigé `emissions_geo.csv`.

Les données contenues dans les colonnes ajoutées par le géocodage sont sous licence 
[ODbL](http://opendatacommons.org/licenses/odbl/summary/).

À noter que dans ce fichier, les colonnes `Coordonnees_X` et `Coordonnees_Y`
correspondent aux données originales, et les colonnes `latitude` et `longitude` aux valeurs corrigées.

