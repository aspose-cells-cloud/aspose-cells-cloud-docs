---
title: SQLScriptSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/sqlscriptsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : SqlScriptSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, SqlScriptSaveOptions
weight: 50
---
## **sqlScriptSaveOptions**

 Représente les options d'enregistrement du fichier .sql.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| CheckIfTableExists| Booléen| Vrai| FAUX|| Vérifiez si le nom de la table existe avant de créer|
| ColumnTypeMap| Chaîne| Vrai| FAUX|| Obtient et définit la carte du type de colonne pour différentes bases de données.|
| CheckAllDataForColumnType| Booléen| Vrai| FAUX|| Vérifiez toutes les données pour trouver le type de données des colonnes.|
| Ajouter une ligne blanche entre les lignes| Booléen| Vrai| FAUX|| Insérez une ligne vide entre chaque donnée.|
| Séparateur| Chaîne| Vrai| FAUX|| Obtient et définit le séparateur de caractères du script SQL.|
| Type d'opérateur| Chaîne| Vrai| FAUX|| Obtient et définit le type d'opérateur de SQL.|
| Clé primaire| Entier| Vrai| FAUX|| Représente quelle colonne est la clé primaire de la table de données.|
| CréerTable| Booléen| Vrai| FAUX|| Indique si vous exportez SQL ou créez une table.|
| NomIdentifiant| Chaîne| Vrai| FAUX||Obtient et définit le nom de la colonne id.|
| ID de démarrage| Entier| Vrai| FAUX|| Obtient et définit l'identifiant de démarrage.|
| Nom de la table| Chaîne| Vrai| FAUX|| Obtient et définit le nom de la table.|
| Exporter en tant que chaîne| Booléen| Vrai| FAUX|| Indique si toutes les données sont exportées sous forme de valeur de chaîne.|
| Zone d'exportation| Classe :CellArea| Vrai| FAUX|| Obtient ou définit la plage d’exportation.|
| HasHeaderRow| Booléen| Vrai| FAUX|| Indique si la plage contient une ligne d'en-tête.|
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
| Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : [Options d'enregistrement](/specification/model/saveoptions)

