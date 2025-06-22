---
title: Importer des données par lots dans la feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importer des données par lots
type: docs
url: /fr/import-batch-data-into-excel/
aliases: [/import-batch-data-into-worksheet/,/import-data/batch-data/,/import/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données par lots dans des fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 19
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Importer des données par lots dans une feuille de calcul Excel
---
Cette feuille de travail REST API `import batch data` dans Excel.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu multipart contient les données ImportBatchDataOption et la seconde contient un fichier de données.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Les paramètres importants sont décrits dans le tableau suivant :

**ImportBatchDataOption**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Données par lots|Liste<CellValue> | données par lots|
| Feuille de travail de destination| chaîne| nom de la feuille de travail de destination.|
| EstInsérer| chaîne| vrai/faux.|
| ImportDataType| chaîne|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Source| Source du fichier| Indique la position du fichier de données lorsque le paramètre BatchData est nul.|

**Valeur de la cellule**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| index de ligne| int||
|index de colonne| int||
| taper| chaîne| type de données|
| valeur| chaîne||
| style| Style(objet)||

**Source du fichier**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Type de source de fichier| chaîne| Fichiers en mémoire/Système de fichiers cloud/Fichiers de requête|
| Chemin du fichier| chaîne| position du fichier|

**Exemple**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
