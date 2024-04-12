---
title: Importation
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données dans des fichiers Excel. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 31
---
L'importation de données dans un fichier Excel est un processus complexe. De nombreux facteurs contribuent à cette complexité et doivent donc être pris en compte lors du processus d’exportation. La possibilité d'importer des types de formats et des types de données dans le fichier avec une qualité professionnelle précise est l'une des principales fonctionnalités de Aspose.Cells Cloud.

## API RSET

Les API suivantes pour importer des données dans un fichier Excel ou plusieurs fichiers Excel sont fournies :

|API|Description|
|:- |:- |
|[POST /cellules/importation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importez des données dans des fichiers Excel sans utiliser de stockage.|
|[POST /cells/{nom}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importez les données dans le fichier Excel en utilisant le stockage.|

## Paramètres de la demande
 
### Sans utiliser de stockage

| Le nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| déposer| déposer| Données de formulaire| Fichier à télécharger|
| Option d'importation| Options d'importation|Corps HTTP| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Avec l'utilisation du stockage

| Le nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| dossier| chaîne| requête||
| Nom de stockage| chaîne| requête| nom de stockage.|
| importer des données|| corps||


### Paramètre d'option d'importation de données

**Les paramètres importants sont décrits dans le tableau suivant**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Données par lots</td><td>Liste<CellValue></td> <td>données par lots</td> </tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>Chaîne</td> <td>vrai faux.</td> </tr>
    <tr> <td>Première rangée</td><td>int</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>Chaîne de séparation</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>Analyseurs personnalisés</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>Données CSV</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Chaîne[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>Image</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Entier[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>TableauIntDeuxDimensions</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Double[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>TableauDoubleDeuxDimensions</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne[,]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>Tableau de chaînes à deux dimensions</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Entier[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>TableauEntier</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
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
    <tr> <td>PremièreColonne</td><td>int</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Double[]</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>DoubleArray</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>Ligne supérieure gauche</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonne supérieure gauche</td><td>int</td><td></td></tr>
    <tr> <td>Ligne inférieure droite</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonne inférieure droite</td><td>int</td><td></td></tr>
    <tr><td>Nom de fichier</td><td>Chaîne</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de travail de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsérer</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>ImportDataType</td><td> Chaîne</td><td>Tableau de chaînes</td></tr>
    <tr> <td>Source</td><td> FichierSource</td><td>Indique la position du fichier de données lorsque le paramètre BatchData est nul.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>indexligne</td><td>int</td> <td></td> </tr>
    <tr><td>Indice de colonne</td><td>int</td><td></td></tr>
    <tr><td>taper</td><td>Chaîne</td><td>Type de données</td></tr>
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
    <tr><td>TypeFichierSource</td><td>Chaîne</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Chemin du fichier</td><td>Chaîne</td><td> emplacement du fichier</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Comment appeler les API RSET

Les articles suivants expliquent chaque API comment appeler en détail et contiennent des exemples de cURL et de SDK pour chaque API :

- [Comment importer des données dans des fichiers Excel sans utiliser de stockage.](/cells/fr/import/without-using-storage)
- [Comment importer des données dans des fichiers Excel en utilisant le stockage.](/cells/fr/import/with-using-storage)
- [Comment importer des données par lots dans la feuille de calcul Excel](/cells/fr/import/batch-data/)
- [Comment importer des données CSV dans la feuille de calcul Excel](/cells/fr/import/csv-data/)
- [Comment importer une image dans la feuille de calcul Excel](/cells/fr/import/picture/)
- [Comment importer un tableau d'entiers dans la feuille de calcul Excel](/cells/fr/import/integer-array/)
- [Comment importer un double tableau dans la feuille de calcul Excel](/cells/fr/import/double-array/)
- [Comment importer un tableau de chaînes dans la feuille de calcul Excel](/cells/fr/import/string-array/)
- [Comment importer un tableau d'entiers à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import/2dimension-integer-array/)
- [Comment importer un tableau double à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import/2dimension-double-array/)
- [Comment iImporter un tableau de chaînes à 2 dimensions dans une feuille de calcul Excel](/cells/fr/import/2dimension-string-array/)
