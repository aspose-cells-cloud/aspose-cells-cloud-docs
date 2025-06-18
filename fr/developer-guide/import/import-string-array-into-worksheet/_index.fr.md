---
title: Importer un tableau de chaînes dans la feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importer un tableau de chaînes
type: docs
url: /fr/import/string-array/
aliases: [/import-string-array-into-excel-worksheet/,/import-string-array-into-worksheet/,/import-data/string-array/]
keywords: Import string array data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données de tableau de chaînes dans des fichiers Excel. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 40
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, importer un tableau de chaînes dans une feuille de calcul Excel
---
Ce REST API `import string array data` dans la feuille de travail Excel.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient les données ImportStringArrayOption et la seconde contient un fichier de données.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Les paramètres importants sont décrits dans le tableau suivant :


**OptionImportStringArray**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Première rangée| int||
| PremièreColonne| int||
| EstVertical| chaîne| vrai faux.|
| Données|Chaîne[]||
| Feuille de travail de destination| chaîne| nom de la feuille de travail de destination.|
| EstInsérer| chaîne| vrai faux.|
| ImportDataType| chaîne|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Source| FichierSource| Indique la position du fichier de données lorsque le paramètre BatchData est nul.|


**Exemple**

```xml

<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>

```

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




