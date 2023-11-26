---
title: Importer des données Json dans Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importer Jso
type: docs
url: /fr/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API prend en charge l'importation de données de tableaux de chaînes dans des fichiers Excel. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 40
---
Ce REST API `import json data` dans la feuille de travail Excel.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Les paramètres importants sont décrits dans le tableau suivant :


**OptionImportStringArray**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| nom| chaîne| Le nom du classeur|
| importJsonRequest| classe| Importez la requête json.|
| mot de passe| chaîne| Le mot de passe du classeur.|
| dossier| chaîne| Dossier de classeur d'origine.|
| Nom de stockage| chaîne| Nom de stockage.|
| chemin de sortie| chaîne| Chemin du fichier de sortie.|
| nomdestockageout| chaîne| Nom de stockage du fichier de sortie.|
| checkExcelRestriction| chaîne| Vérifiez la restriction Excel.|


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

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :





