---
title: "Importer des données en lots dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Importer des données en lots"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, API cloud, importation de données en lots, Excel, CSV, JSON, XML, tableaux"
description: "Découvrez comment importer des données en lots (CSV, JSON, XML, tableaux) dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’authentification, des exemples de requête/réponse, des extraits de code SDK et la gestion des erreurs."
weight: 19
ArticleTitle: "Importer des données en lots dans une feuille de calcul Excel – Documentation Aspose.Cells Cloud"
---

Cet **API REST permet d’importer des données en lots** dans une feuille de calcul Excel. Elle accepte une requête multipart, dont la première partie contient l’objet **ImportBatchDataOption**, et la deuxième partie contient le fichier de données réel (CSV, JSON, XML, etc.).

L’opération utilise une requête HTTP avec contenu multipart (voir [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### ImportBatchDataOption

| Nom du paramètre         | Type              | Description                                                                                                                                                        |
| ------------------------ | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **BatchData**            | `List<CellValue>` | Collection de valeurs de cellules à écrire directement.                                                                                                            |
| **DestinationWorksheet** | `string`          | Nom de la feuille de calcul dans laquelle les données seront importées.                                                                                            |
| **IsInsert**             | `bool`            | Si `true`, les données sont insérées et les cellules existantes sont décalées ; si `false`, les données remplacent les cellules existantes.                        |
| **ImportDataType**       | `string`          | Format des données à importer. Valeurs autorisées : `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | Spécifie l’emplacement du fichier de données lorsque **BatchData** est `null`.                                                                                     |

### CellValue

| Nom du paramètre | Type     | Description                                           |
| ---------------- | -------- | ----------------------------------------------------- |
| **rowIndex**     | `int`    | Index de ligne (à partir de 0) de la cellule cible.  |
| **columnIndex**  | `int`    | Index de colonne (à partir de 0) de la cellule cible. |
| **type**         | `string` | Type de données de la valeur (par ex. `int`, `double`, `string`). |
| **value**        | `string` | Valeur réelle à écrire dans la cellule.              |
| **style**        | `Style`  | Informations facultatives de style pour la cellule.  |

### FileSource

| Nom du paramètre   | Type     | Description                                                              |
| ------------------ | -------- | ------------------------------------------------------------------------ |
| **FileSourceType** | `string` | Source du fichier : `InMemoryFiles`, `CloudFileSystem` ou `RequestFiles`. |
| **FilePath**       | `string` | Chemin ou identifiant du fichier dans la source choisie.                |

### Exemple (XML)

```xml
<ImportBatchDataOption>
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
</ImportBatchDataOption>
```

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                               |
|------|-----------------------------|---------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                           |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.                       |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) définit une interface de programmation accessible publiquement qui vous permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utilisation des SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de différents SDK :

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