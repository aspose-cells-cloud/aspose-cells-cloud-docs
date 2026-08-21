---
title: "Importer un tableau de doubles dans une feuille Excel"
second_title: "Document"
linktitle: "Importer un tableau de doubles"
type: docs
url: /fr/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, importer un tableau de doubles, API Excel, SDK cloud"
description: "Découvrez comment importer un tableau de doubles dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’authentification, le format des requêtes, les paramètres, des exemples XML/JSON et les détails de la réponse."
weight: 20
ArticleTitle: "Importer un tableau de doubles dans une feuille Excel – Guide Aspose.Cells Cloud"
---

Cette API REST **importe des données de type tableau de doubles** dans une feuille Excel.

> **Prérequis :** Vous devez disposer d’un jeton JWT valide avant d’appeler cette API. Consultez le guide d’authentification pour plus de détails.

Vous envoyez une requête HTTP dont le contenu est de type **multipart** (voir [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La première partie du corps multipart contient les données **ImportDoubleArrayOption**, tandis que la seconde partie contient le fichier de données.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### Paramètres de la requête

#### **ImportDoubleArrayOption**

| Nom du paramètre     | Type       | Description                                                                                                 |
| --------------------- | ---------- | ----------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Indice de la première ligne (indexé à partir de 0) où les données seront insérées.                         |
| FirstColumn          | int        | Indice de la première colonne (indexé à partir de 0) où les données seront insérées.                       |
| IsVertical           | boolean    | `true` / `false` – détermine si le tableau est inséré verticalement (`true`) ou horizontalement (`false`). |
| Data                 | Double[]   | Tableau de valeurs doubles à importer.                                                                      |
| DestinationWorksheet | string     | Nom de la feuille cible.                                                                                    |
| IsInsert             | boolean    | `true` / `false` – si `true`, les données sont insérées ; si `false`, les cellules existantes sont remplacées. |
| ImportDataType       | string     | Type de données importées (par exemple, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`). |
| Source               | FileSource | Indique l’emplacement du fichier de données lorsque le paramètre `BatchData` est null.                      |

#### Exemple (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Exemple (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### Réponse

Une requête réussie renvoie **HTTP 200** avec une charge utile JSON similaire à :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes de statut possibles :

| Code | Signification                                  |
| ---- | ---------------------------------------------- |
| 200  | Importation réussie                            |
| 400  | Requête incorrecte – données manquantes ou invalides |
| 401  | Non autorisé – jeton invalide ou manquant      |
| 500  | Erreur interne du serveur                      |

### Gestion des erreurs

Lorsqu’une erreur se produit, l’API renvoie un objet JSON contenant le code d’erreur et un message descriptif. Exemple pour une requête non autorisée :

```json
{
  "Code": 401,
  "Status": "Error"
}
```

Pour plus d’informations sur les opérations d’importation connexes, consultez les pages de documentation « Importer un tableau de doubles à deux dimensions » et « Importer un tableau d’entiers ».

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}