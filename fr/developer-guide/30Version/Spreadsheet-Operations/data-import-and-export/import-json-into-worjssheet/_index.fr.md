---
title: Importer des données Json dans Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importer Jso
type: docs
url: /fr/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API prend en charge l'importation de données de tableaux de chaînes dans des fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 40
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Importer des données Json dans Excel
---
Cette feuille de travail REST API `import json data` dans Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Les paramètres importants sont décrits dans le tableau suivant :

**ImportStringArrayOption**

|Nom du paramètre| Chemin/Chaîne de requête/Corps HTTP|Taper|Description|
|:- |:- |:- |:- |
| nom| Chemin| chaîne| Le nom du classeur|
| importJsonRequest| Corps HTTP| classe| Importer une requête json.|
| mot de passe| Chaîne de requête| chaîne| Le mot de passe du classeur.|
| dossier| Chaîne de requête| chaîne| Classeur original.|
| nom de stockage| Chaîne de requête| chaîne| Nom de stockage.|
| chemin de sortie| Chaîne de requête| chaîne| Chemin du fichier de sortie.|
| outStorageName| Chaîne de requête| chaîne| Nom de stockage pour le fichier de sortie.|
| checkExcelRestriction| Chaîne de requête| chaîne| Vérifiez la restriction Excel.|

**Exemple**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
