---
title: Importer des données dans les fichiers Excel et exporter des données à partir des fichiers Excel
second_title: Documen
linktitle: Importer et exporter des données
type: docs
url: /fr/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Générer de nouveaux documents ou rapports pouvant inclure des graphiques, des tableaux et d'autres éléments de visualisation de données
weight: 25
kwords: Excel Importation de données vs. Accès direct à la base de données ; Importation de données par lots vs. Écriture de données ligne par ligne ; Exportation de données automatisée vs. Extraction manuelle de données.
---
Aspose.Cells Cloud API prend en charge l'importation de données à partir de diverses sources de données et peut exporter des données à partir de Excel, de graphiques et de graphiques vers différents formats, notamment Excel, CSV, PDF, HTML, PNG, etc. Cela rend la gestion et le partage des données simples et efficaces.

## Comment importer des données à partir de diverses sources de données

L'importation de données dans un fichier Excel est un processus complexe. De nombreux facteurs contribuent à cette complexité et doivent donc être pris en compte lors de l'exportation. La possibilité d'importer des formats et types de données variés avec une qualité professionnelle est l'une des principales fonctionnalités de Aspose.Cells Cloud.

### Informations sur les API d'importation de données

Les API suivantes pour importer des données dans un fichier Excel ou plusieurs fichiers Excel sont fournies :

|API|Description|
|:- |:- |
|[POST /cellules/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importez des données dans des fichiers Excel sans utiliser de stockage.|
|[POST /cellules/{nom}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importez des données dans le fichier Excel en utilisant le stockage.|

### Paramètres de la demande

#### Sans utiliser de stockage

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| déposer| déposer| données de formulaire| Fichier à télécharger|
| Option d'importation| Options d'importation| Corps HTTP| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

#### Avec l'utilisation du stockage

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| dossier| chaîne| requête||
| nom de stockage| chaîne| requête| nom de stockage.|
| importer des données|| corps||

#### Paramètre d'option d'importation de données

**Les paramètres importants sont décrits dans le tableau suivant**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Données par lots</td><td>Liste<CellValue></td> <td>données de lot</td> </tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Tableau de données par lots de chaînes à deux dimensions</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Convertir des données numériques</td><td>Chaîne</td> <td>vrai/faux.</td> </tr>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>Chaîne de séparation</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>Analyseurs personnalisés</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Données CSV</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>Données</td><td> Chaîne[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Image</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Entier[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Tableau d'entiers à deux dimensions</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Double[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Tableau double à deux dimensions</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Tableau de chaînes à deux dimensions</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>Données</td><td> Entier[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>tableau d'entiers</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>Première colonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>Données</td><td> Double[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>DoubleArray</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Rangée supérieure gauche</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonne supérieure gauche</td><td>int</td><td></td></tr>
    <tr> <td>Ligne inférieure droite</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonne inférieure droite</td><td>int</td><td></td></tr>
    <tr><td>Nom de fichier</td><td>Chaîne</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai/faux.</td></tr>
    <tr><td>ImporterDataType</td><td> Chaîne</td><td>Tableau de chaînes</td></tr>
    <tr> <td>Source</td><td> Source du fichier</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>index de ligne</td><td>int</td> <td></td> </tr>
    <tr><td>index de colonne</td><td>int</td><td></td></tr>
    <tr><td>taper</td><td>Chaîne</td><td>type de données</td></tr>
    <tr><td>valeur</td><td> Chaîne</td> <td></td></tr>
    <tr><td>style</td><td> Style(objet)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>Type de source de fichier</td><td>Chaîne</td> <td>Fichiers en mémoire/Système de fichiers cloud/Fichiers de requête</td> </tr>
    <tr><td>Chemin du fichier</td><td>Chaîne</td><td> position du fichier</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Comment exporter des objets Excel vers différents formats de fichiers

Si vous avez créé à l'origine un fichier Excel dans un certain format, comme[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , et[CSV](https://docs.fileformat.com/spreadsheet/csv/)Il peut parfois être utile de convertir un fichier Excel vers un autre format afin de bénéficier de ses fonctionnalités spécifiques. Par exemple, vous pouvez exporter un fichier Excel vers[PDF](https://docs.fileformat.com/pdf/) pour protéger votre contenu de toute modification non autorisée et le rendre facile à lire et à partager simultanément.

L'exportation d'objets Excel est un processus complexe. De nombreux facteurs contribuent à cette complexité et doivent donc être pris en compte lors du processus d'exportation. La possibilité d'exporter des objets Excel vers un fichier au format unique avec une qualité professionnelle est l'une des fonctionnalités phares de Aspose.Cells Cloud.

 Il fonctionne parfaitement pour les classeurs, graphiques, formes et images exportés depuis un fichier Excel. Vous pouvez exporter les formats suivants :[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [SAO](https://docs.fileformat.com/spreadsheet/ods/), [SMS](https://docs.fileformat.com/word-processing/txt/) . Les formats d'exportation uniquement :[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NOMBRES](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient le fichier de données et la seconde contient les options de sauvegarde.

Le classeur REST API `export` et les objets internes dans un fichier de format différent.

### Exportation API Informations

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| déposer| déposer| données de formulaire| Fichier à télécharger|
| type d'objet| chaîne| requête| type d'objet (classeur/feuille de calcul/graphique/forme/image/objet de liste/objet ole)|
| format| chaîne| requête|[Format de fichier](/cells/fr/supported-file-formats/)  |

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Comment appeler les API d'importation et d'exportation

Les articles suivants expliquent en détail comment appeler chaque API et contiennent des exemples de cURL et de SDK de chaque API :

- [Comment importer des données dans des fichiers Excel sans utiliser de stockage.](/cells/fr/import/without-using-storage)
- [Comment importer des données dans des fichiers Excel à l'aide du stockage.](/cells/fr/import/with-using-storage)
- [Comment importer des données par lots dans la feuille de calcul Excel](/cells/fr/import-batch-data-into-excel-worksheet/)
- [Comment importer des données CSV dans la feuille de calcul Excel](/cells/fr/import-csv-data-into-excel-worksheet/)
- [Comment importer une image dans la feuille de calcul Excel](/cells/fr/import-picture-into-excel-worksheet/)
- [Comment importer un tableau d'entiers dans la feuille de calcul Excel](/cells/fr/import-integer-array-into-excel-worksheet/)
- [Comment importer un tableau double dans la feuille de calcul Excel](/cells/fr/import-double-array-into-excel-worksheet/)
- [Comment importer un tableau de chaînes dans la feuille de calcul Excel](/cells/fr/import-string-array-into-excel-worksheet/)
- [Comment importer un tableau d'entiers à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import-a-2D-integer-array-into-excel-worksheet/)
- [Comment importer un tableau double à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import-a-2D-double-array-into-excel-worksheet/)
- [Comment importer un tableau de chaînes à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import-a-2D-string-array-into-excel-worksheet/)
- [Exporter le graphique Excel vers un format de fichier différent](/cells/fr/export-excel-chart-to-different-formats/)
- [Exporter la liste d'objets Excel vers un format de fichier différent](/cells/fr/export-excel-listobject-to-different-formats/)
- [Exporter l'objet ole Excel vers un format de fichier différent](/cells/fr/export-excel-ole-object/)
- [Exporter l'image Excel vers un format de fichier différent](/cells/fr/export-excel-picture-to-different-formats/)
- [Exporter la forme Excel vers un format de fichier différent](/cells/fr/export-excel-shape-to-different-formats/)
- [Exporter le classeur Excel vers un format de fichier différent](/cells/fr/export-excel-to-different-formats/)
- [Exporter la feuille de calcul Excel vers un format de fichier différent](/cells/fr/export-excel-worksheet-to-different-formats//)
