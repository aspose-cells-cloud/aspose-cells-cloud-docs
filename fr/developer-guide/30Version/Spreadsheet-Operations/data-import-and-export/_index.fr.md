---
title: "Importer des données dans des fichiers Excel et exporter des données depuis des fichiers Excel"
second_title: "Document"
linktitle: "Importation et exportation de données"
type: docs
url: /data-import-and-export/
keywords: "Aspose.Cells Cloud, importation de données, exportation Excel, API, CSV, JSON, image, tableau"
description: "Découvrez comment importer des données à partir de fichiers CSV, JSON, de tableaux et d’images dans des fichiers Excel, ainsi que comment exporter des classeurs, des graphiques et des formes vers PDF, PNG et d’autres formats à l’aide de l’API Aspose.Cells Cloud (v3.0)."
weight: 25
---

L’API Aspose.Cells Cloud permet d’importer des données provenant de nombreuses sources différentes, ainsi que d’exporter des classeurs, des graphiques et d’autres objets Excel vers divers formats, notamment **XLSX**, **CSV**, **PDF**, **HTML**, **PNG**, etc. Cela simplifie la gestion et le partage des données.

**Version de l’API :** **v3.0** – Dernière mise à jour : **2024‑03‑15**

### Guide de démarrage rapide

1. **Préparer le corps de la requête (payload)** – Construisez un corps JSON décrivant les options d’importation ou d’exportation (par exemple, `ImportCSVDataOption`, `ExportOptions`).
2. **Envoyer la requête** – Utilisez `curl`, Postman ou un SDK pour appeler le point de terminaison approprié (`POST /cells/import` ou `POST /cells/export`).
3. **Gérer la réponse** – En cas de succès, vous recevez le fichier traité (binaire ou en Base64). En cas d’erreur, examinez le code de statut HTTP et le message d’erreur renvoyé dans le corps JSON.

#### Conditions préalables

- Un compte Aspose Cloud actif et un jeton JWT valide.
- Le classeur cible doit exister à l’emplacement de stockage spécifié (pour les API basées sur le stockage).
- En-têtes `Content-Type` corrects (`multipart/form-data` pour les téléchargements de fichiers, `application/json` pour les corps JSON).

## Comment importer des données à partir de diverses sources

L’importation de données dans un fichier Excel implique plusieurs considérations à prendre en compte pendant le processus. La capacité à importer de nombreux formats et types de données avec une qualité professionnelle constitue l’une des principales fonctionnalités d’Aspose.Cells Cloud.

### Informations sur les API d’importation de données

Les API suivantes sont fournies pour importer des données dans un ou plusieurs fichiers Excel :

| API                                                                                                | Description                                                         |
| :------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------ |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Importer des données dans des fichiers Excel sans utiliser de stockage. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Importer des données dans un fichier Excel stocké dans le cloud.   |

### Paramètres de la requête

#### Sans utilisation de stockage

| Nom du paramètre | Type          | Emplacement | Description                                                                                           |
| :---------------- | :------------ | :---------- | :---------------------------------------------------------------------------------------------------- |
| file              | fichier       | formData    | Fichier à télécharger                                                                                 |
| ImportOption      | ImportOptions | body        | Spécifie le format d’importation (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Avec utilisation de stockage

| Nom du paramètre | Type          | Emplacement | Description                |
| :---------------- | :------------ | :---------- | :------------------------- |
| name              | string        | path        | Nom du fichier Excel       |
| folder            | string        | query       | Chemin du dossier dans le stockage |
| storageName       | string        | query       | Nom du stockage            |
| importData        | ImportOptions | body        | Corps de données à importer |

#### Paramètres des options d’importation de données

**Les paramètres importants sont décrits dans les tableaux suivants :**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Données en lot à importer</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Indique s’il faut convertir les données numériques (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Séparateur de colonnes</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Configurations des analyseurs personnalisés</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indique si l’image est placée verticalement (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Données d’image (chaînes en Base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Tableau d’entiers à deux dimensions</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Tableau de nombres à virgule flottante à deux dimensions</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Tableau de chaînes à deux dimensions</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indique si le tableau est vertical (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Tableau d’entiers à une dimension</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index de la première ligne</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index de la première colonne</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indique si le tableau est vertical (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Tableau de nombres à virgule flottante à une dimension</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Index de la ligne supérieure gauche</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Index de la colonne supérieure gauche</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Index de la ligne inférieure droite</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Index de la colonne inférieure droite</td></tr>
    <tr><td>Filename</td><td>string</td><td>Nom du fichier source</td></tr>
    <tr><td>Data</td><td>string</td><td>Données textuelles à importer</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nom de la feuille de calcul de destination</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indique s’il faut insérer les données (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Emplacement du fichier de données lorsque BatchData est null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Index de ligne de la cellule</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Index de colonne de la cellule</td></tr>
    <tr><td>type</td><td>string</td><td>Type de données de la valeur de la cellule</td></tr>
    <tr><td>value</td><td>string</td><td>Valeur de la cellule</td></tr>
    <tr><td>style</td><td>Style (objet)</td><td>Définition du style de cellule</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Paramètre</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem ou RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Chemin vers le fichier source</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Comment exporter des objets Excel vers divers formats de fichier

Si vous avez initialement créé un fichier Excel dans un format tel que **XLS**, **XLSX**, **XLSB** ou **CSV**, vous souhaiterez peut-être le convertir vers un autre format afin de tirer parti de fonctionnalités spécifiques. Par exemple, l’exportation vers **PDF** protège le contenu contre les modifications non autorisées tout en facilitant sa lecture et son partage.

L’exportation d’objets Excel implique plusieurs considérations. Aspose.Cells Cloud permet d’exporter des classeurs, des graphiques, des formes et des images vers de nombreux formats, avec une qualité élevée :

_Formats à usage uniquement d’exportation_ : PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_Formats supportant à la fois l’importation et l’exportation_ : XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

La requête utilise un contenu multiparte tel que défini dans [RFC 2046] et [RFC 1341]. La première partie contient le fichier de données ; la deuxième partie contient les options d’enregistrement.

### Informations sur l’API d’exportation

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                   |
| :---------------- | :----- | :---------- | :-------------------------------------------------------------------------------------------- |
| file              | fichier | formData    | Fichier à télécharger                                                                         |
| objectType        | string | query       | Type d’objet (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format            | string | query       | Format de fichier de sortie souhaité (voir [Formats de fichier pris en charge](/cells/supported-file-formats/)) |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation accessible publiquement qui permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler l’API. L’exemple ci-dessous illustre une requête et sa réponse JSON.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'file1=@exemple1.xlsx' \
  -F 'file2=@exemple2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "exemple1.pdf",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    },
    {
      "Filename": "exemple2.pdf",
      "FileSize": 274022,
      "FileContent": "-----ChaîneBase64--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Codes de statut HTTP courants

| Statut | Signification                                                    | Action recommandée                            |
| :----- | :--------------------------------------------------------------- | :-------------------------------------------- |
| 200    | Succès – le fichier a été exporté                                | Traiter le ou les fichiers renvoyés           |
| 400    | Requête incorrecte – paramètres manquants ou non valides         | Vérifier le corps et les chaînes de requête   |
| 401    | Non autorisé – jeton JWT invalide ou expiré                      | Actualiser le jeton et réessayer              |
| 404    | Introuvable – le classeur ou la feuille de calcul spécifié n’existe pas | Vérifier le nom du fichier et le chemin de stockage |
| 500    | Erreur interne du serveur – condition inattendue sur le serveur  | Contacter le support Aspose avec l’ID de la requête |

## Comment appeler les API d’importation et d’exportation

Les articles suivants expliquent chaque API en détail et contiennent des exemples cURL et SDK :

- [Comment importer des données dans des fichiers Excel sans utiliser de stockage.](/cells/import/without-using-storage)
- [Comment importer des données dans des fichiers Excel en utilisant du stockage.](/cells/import/with-using-storage)
- [Comment importer des données en lot dans une feuille de calcul Excel](/cells/import-batch-data-into-excel-worksheet/)
- [Comment importer des données CSV dans une feuille de calcul Excel](/cells/import-CSV-data-into-excel-worksheet/)
- [Comment importer une image dans une feuille de calcul Excel](/cells/import-picture-into-excel-worksheet/)
- [Comment importer un tableau d’entiers dans une feuille de calcul Excel](/cells/import-integer-array-into-excel-worksheet/)
- [Comment importer un tableau de nombres à virgule flottante dans une feuille de calcul Excel](/cells/import-double-array-into-excel-worksheet/)
- [Comment importer un tableau de chaînes dans une feuille de calcul Excel](/cells/import-string-array-into-excel-worksheet/)
- [Comment importer un tableau d’entiers à deux dimensions dans une feuille de calcul Excel](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Comment importer un tableau de nombres à virgule flottante à deux dimensions dans une feuille de calcul Excel](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Comment importer un tableau de chaînes à deux dimensions dans une feuille de calcul Excel](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Exporter un graphique Excel vers un autre format de fichier](/cells/export-excel-chart-to-different-formats/)
- [Exporter un objet liste Excel vers un autre format de fichier](/cells/export-excel-listobject-to-different-formats/)
- [Exporter un objet OLE Excel vers un autre format de fichier](/cells/export-excel-ole-object/)
- [Exporter une image Excel vers un autre format de fichier](/cells/export-excel-picture-to-different-formats/)
- [Exporter une forme Excel vers un autre format de fichier](/cells/export-excel-shape-to-different-formats/)
- [Exporter un classeur Excel vers un autre format de fichier](/cells/export-excel-to-different-formats/)
- [Exporter une feuille de calcul Excel vers un autre format de fichier](/cells/export-excel-worksheet-to-different-formats/)

---