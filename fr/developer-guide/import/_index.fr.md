---
title: Importer
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API prend en charge l'importation de données dans des fichiers Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 31
---
L'importation de données dans un fichier Excel est un processus complexe. De nombreux facteurs contribuent à la complexité et doivent donc être pris en compte lors du processus d'exportation. La possibilité d'importer des types de formats et des types de données dans le fichier avec une qualité professionnelle précise est une caractéristique majeure de Aspose.Cells Cloud.

## API RSET

Les API suivantes pour importer des données dans un fichier Excel ou plusieurs fichiers Excel sont fournies :

|API|Description|
|:- |:- |
|[POST /cellules/importation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importez des données dans des fichiers Excel sans utiliser de stockage.|
|[POST /cells/{nom}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importez des données dans le fichier Excel en utilisant le stockage.|

## Paramètres de requête
 
### Sans utiliser de stockage

| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| déposer| déposer| Données de formulaire| Fichier à uploader|
| Option d'importation| Options d'importation| Corps HTTP| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Image|

### Avec utilisation du stockage

| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| dossier| chaîne| mettre en doute||
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
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
    <tr> <td>Données de lot</td><td>Liste<CellValue></td> <td>données de lot</td> </tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>TwoDimensionStringBatchDataArray</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>SéparateurChaîne</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>Analyseurs personnalisés</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>Données CSV</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Chaîne[]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>Image</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>Données</td><td> Entier[,]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>TwoDimensionIntArray</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>Données</td><td> Double[,]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>TwoDimensionDoubleArray</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne[,]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>TwoDimensionStringArray</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Entier[]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>TableauEntiers</td></tr>
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
    <tr> <td>Première rangée</td><td>entier</td> <td></td> </tr>
    <tr> <td>PremièreColonne</td><td>entier</td><td></td></tr>
    <tr><td>EstVertical</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Données</td><td> Double[]</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>DoubleTableau</td></tr>
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
    <tr> <td>UpperLeftRow</td><td>entier</td> <td></td> </tr>
    <tr> <td>Colonne supérieure gauche</td><td>entier</td><td></td></tr>
    <tr> <td>ligne inférieure droite</td><td>entier</td> <td></td> </tr>
    <tr> <td>Colonne inférieure droite</td><td>entier</td><td></td></tr>
    <tr><td>Nom de fichier</td><td>Chaîne</td><td></td></tr>
    <tr><td>Données</td><td> Chaîne</td> <td></td></tr>
    <tr> <td>Feuille de calcul de destination</td><td> Chaîne</td><td> Nom de la feuille de travail de destination.</td></tr>
    <tr><td>EstInsère</td><td>Chaîne</td><td>vrai faux.</td></tr>
    <tr><td>Type de données d'importation</td><td> Chaîne</td><td>ChaîneTableau</td></tr>
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
    <tr><td>index de ligne</td><td>entier</td> <td></td> </tr>
    <tr><td>index de colonne</td><td>entier</td><td></td></tr>
    <tr><td>taper</td><td>Chaîne</td><td>Type de données</td></tr>
    <tr><td>valeur</td><td> Chaîne</td> <td></td></tr>
    <tr><td>style</td><td> Style (objet)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Paramètre</th><th scope="col">Taper</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>Chaîne</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Chemin du fichier</td><td>Chaîne</td><td> emplacement du fichier</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Comment appeler les API RSET

Les articles suivants expliquent chaque API comment appeler en détail et contiennent des exemples cURL et SDK de chaque API :

- [Comment importer des données dans des fichiers Excel sans utiliser de stockage.](/cells/fr/import/without-using-storage)
- [Comment importer des données dans des fichiers Excel en utilisant le stockage.](/cells/fr/import/with-using-storage)
- [Comment importer des données de lot dans la feuille de calcul Excel](/cells/fr/import/batch-data/)
- [Comment importer des données CSV dans la feuille de calcul Excel](/cells/fr/import/csv-data/)
- [Comment importer une image dans la feuille de calcul Excel](/cells/fr/import/picture/)
- [Comment importer un tableau d'entiers dans la feuille de calcul Excel](/cells/fr/import/integer-array/)
- [Comment importer Double Array dans la feuille de calcul Excel](/cells/fr/import/double-array/)
- [Comment importer un tableau de chaînes dans la feuille de calcul Excel](/cells/fr/import/string-array/)
- [Comment importer un tableau d'entiers à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import/2dimension-integer-array/)
- [Comment importer un tableau double à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import/2dimension-double-array/)
- [Comment iImporter un tableau de chaînes à 2 dimensions dans la feuille de calcul Excel](/cells/fr/import/2dimension-string-array/)
