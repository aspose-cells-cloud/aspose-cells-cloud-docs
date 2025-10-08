---
title: Importer des données CSV dans la feuille de calcul Excel
second_title: Documen
linktitle: Importer des données CSV
type: docs
url: /fr/import-csv-data-into-excel/
aliases: [/import-csv-data-into-worksheet/,/import-data/csv-data/,/import/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données CSV dans des fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 19
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Importer des données CSV dans une feuille de calcul Excel
---
Cette feuille de travail REST API `import csv data` dans Excel.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient les données ImportCSVDataOption et la seconde contient un fichier de données.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Les paramètres importants sont décrits dans le tableau suivant :

**Importer une option de données CSV**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Chaîne de séparation| chaîne||
| Convertir des données numériques| chaîne|vrai/faux.|
| Première rangée| int||
| Première colonne| int||
| Fichier source| chaîne||
| Analyseurs personnalisés|Liste<CustomParserConfig> ||

**Configuration de l'analyseur personnalisé**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Index de colonne| int||
| Méthode d'analyse| chaîne||
| Style personnalisé| chaîne||

**Exemple**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
