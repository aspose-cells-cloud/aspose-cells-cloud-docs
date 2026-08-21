---
title: "Importer un tableau à deux dimensions de doubles dans une feuille Excel"
second_title: "Document"
linktitle: "Importer un tableau à deux dimensions de doubles"
type: docs
url: /fr/import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "Importer un tableau à deux dimensions de doubles, Excel, Aspose Cells Cloud, API REST, Classeur, Importation de données"
description: "Découvrez comment importer un tableau à deux dimensions de valeurs décimales dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le format de la requête, les paramètres et des exemples de code SDK."
weight: 20
---

Cette API REST **importe un tableau à deux dimensions de doubles** dans une feuille Excel.

La requête est une HTTP `POST` avec un contenu multipart (voir [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du corps multipart contient les données **Import2DimensionDoubleArrayOption**, tandis que la deuxième partie contient le fichier de données source.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Les paramètres importants sont décrits dans le tableau suivant :

### Import2DimensionDoubleArrayOption

| Nom du paramètre         | Type         | Description                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | Indice de ligne (à base 1) à partir duquel l’importation commence.                                                     |
| **FirstColumn**          | `int`        | Indice de colonne (à base 1) à partir duquel l’importation commence.                                                   |
| **Data**                 | `Double[,]`  | Tableau à deux dimensions de valeurs décimales à importer.                                                             |
| **DestinationWorksheet** | `string`     | Nom de la feuille qui recevra les données.                                                                             |
| **IsInsert**             | `string`     | `"true"` pour insérer des lignes, `"false"` pour écraser les cellules existantes.                                      |
| **ImportDataType**       | `string`     | Type de données à importer (par exemple, `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, etc.). |
| **Source**               | `FileSource` | Indique l’emplacement du fichier de données lorsque le paramètre `BatchData` est null.                                 |

**Exemple**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                           |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                                           |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) définit une interface de programmation accessible publiquement qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}