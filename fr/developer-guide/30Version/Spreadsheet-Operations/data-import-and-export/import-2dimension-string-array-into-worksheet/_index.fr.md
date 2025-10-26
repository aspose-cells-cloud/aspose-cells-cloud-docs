---
title: Importer un tableau de chaînes à 2 dimensions dans la feuille de calcul Excel
second_title: Documen
linktitle: Importer un tableau de chaînes à 2 dimensions
type: docs
url: /fr/import-a-2D-string-array-into-excel-worksheet/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/,/import/2dimension-string-array/ ]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données de tableaux de chaînes à deux dimensions dans des fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 20
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Importer un tableau de chaînes à 2 dimensions dans la feuille de calcul Excel
---
Cette feuille de travail REST API `import 2 dimension string array data` dans Excel.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient les données Import2DimensionStringArrayOption et la seconde contient un fichier de données.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Les paramètres importants sont décrits dans le tableau suivant :

**Import2DimensionStringArrayOption**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Première rangée| int||
| Première colonne| int||
| Données|Chaîne[,]||
|Feuille de travail de destination| chaîne| nom de la feuille de travail de destination.|
| EstInsérer| chaîne| vrai/faux.|
| ImporterDataType| chaîne|IntArray/DoubleArray/StringArray/DeuxDimensionIntArray/DeuxDimensionDoubleArray/DeuxDimensionStringArray/BatchData/CSVData.|
| Source| Source du fichier| Indique la position du fichier de données lorsque le paramètre BatchData est nul.|

**Exemple**

```json

{
    "Data": [
        ["1.0", "2.9"],
        ["2.0", "2.1"]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 1,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionStringArray"
}

```

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
