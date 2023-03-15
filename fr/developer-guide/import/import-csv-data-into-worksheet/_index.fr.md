---
title: Importer des données CSV dans la feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importer des données csv
type: docs
url: /fr/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données csv dans des fichiers Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 19
---
Ce REST API `import csv data` dans la feuille de travail Excel.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient les données ImportCSVDataOption et la seconde contient un fichier de données.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Les paramètres importants sont décrits dans le tableau suivant :


**ImportCSVDataOptionImportCSVDataOption**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| SéparateurChaîne| chaîne||
| ConvertNumericData| chaîne|vrai faux.|
| Première rangée| entier||
| PremièreColonne| entier||
| Fichier source| chaîne||
| Analyseurs personnalisés|Liste<CustomParserConfig> ||


**CustomParserConfigCustomParserConfig**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Index de colonne| entier||
| ParseMethod| chaîne||
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

## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
