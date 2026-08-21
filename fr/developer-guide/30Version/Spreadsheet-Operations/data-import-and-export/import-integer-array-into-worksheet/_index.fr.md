---
title: "Importer un tableau d'entiers dans une feuille Excel"
linktitle: "Importer un tableau d'entiers"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, import de tableau d'entiers, API REST, SDK, C#, PHP, Ruby, Java, Python"
description: "Découvrez comment importer un tableau d'entiers dans une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe de requête, les paramètres, des exemples de code pour plusieurs SDK et les détails de la réponse."
weight: 30
ArticleTitle: "Importer un tableau d'entiers dans une feuille Excel – API Aspose.Cells Cloud"
---

Cette API REST importe un tableau d'entiers dans une feuille Excel.

La requête doit être une méthode HTTP **POST** avec un contenu multipart (voir [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du corps multipart contient la charge utile JSON **ImportIntegerArrayOption**, et la deuxième partie contient le fichier de données source (par exemple, un fichier Excel CSV ou binaire).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Les deux points de terminaison acceptent la même charge utile multipart. Le premier point de terminaison effectue une opération d'importation générique, tandis que le second cible un classeur spécifique identifié par `{name}`.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

### ImportIntegerArrayOption

| Nom du paramètre         | Type       | Description                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Index de base zéro de la première ligne où les données seront placées.                                                                                                                        |
| **FirstColumn**          | int        | Index de base zéro de la première colonne où les données seront placées.                                                                                                                      |
| **IsVertical**           | boolean    | `true` pour insérer le tableau verticalement (vers le bas dans une colonne) ; `false` pour l’insérer horizontalement (sur une ligne).                                                         |
| **Data**                 | Integer[]  | Le tableau d’entiers à importer.                                                                                                                                                              |
| **DestinationWorksheet** | string     | Nom de la feuille de calcul qui recevra les données.                                                                                                                                          |
| **IsInsert**             | boolean    | `true` pour insérer des lignes/colonnes avant d’écrire les données ; `false` pour écraser les cellules existantes.                                                                           |
| **ImportDataType**       | string     | Type des données à importer. Valeurs valides : `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indique la position du fichier de données lorsque le paramètre **BatchData** est `null`.                                                                                                      |

#### Exemple de corps de requête

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Réponse

Une requête réussie renvoie **HTTP 200** avec une charge utile JSON similaire à :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes d’état possibles :

| Code | Signification                               |
| ---- | ------------------------------------------- |
| 200  | Importation réussie                         |
| 400  | Requête incorrecte – données manquantes ou invalides |
| 401  | Non autorisé – jeton invalide ou manquant  |
| 500  | Erreur interne du serveur                   |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK masquent les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}