---
title: "Importer un tableau de chaînes à deux dimensions dans une feuille Excel"
second_title: "Document"
linktitle: "Importer un tableau de chaînes à deux dimensions"
type: docs
url: /fr/import-a-2D-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud, importer un tableau de chaînes à deux dimensions, Excel, API REST, SDK"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour importer un tableau de chaînes à deux dimensions dans une feuille Excel. Inclut le format de la requête, les détails des paramètres et des exemples de code SDK pour C#, PHP et Ruby."
weight: 20
---

Cette API REST **importe un tableau de chaînes à deux dimensions** dans une feuille Excel.

La requête est une requête HTTP avec un contenu multipart (voir [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu multipart contient les données `Import2DimensionStringArrayOption`, tandis que la deuxième partie contient le fichier de données.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

Les paramètres importants sont décrits dans le tableau suivant :

### **Import2DimensionStringArrayOption**

| Nom du paramètre     | Type                | Description                                                                   |
| -------------------- | ------------------- | ----------------------------------------------------------------------------- |
| FirstRow             | int                 | Index de ligne (à base zéro) à partir duquel l’importation commence.          |
| FirstColumn          | int                 | Index de colonne (à base zéro) à partir duquel l’importation commence.        |
| Data                 | String[,]           | Tableau à deux dimensions contenant les chaînes à importer.                   |
| DestinationWorksheet | string              | Nom de la feuille qui recevra les données importées.                          |
| IsInsert             | string (true/false) | Si **true**, les données sont insérées et les cellules existantes sont déplacées en conséquence. |
| ImportDataType       | string              | Spécifie le type de données ; pour cette opération, utilisez `TwoDimensionStringArray`. |
| Source               | FileSource          | Indique l’emplacement du fichier de données lorsque le paramètre `BatchData` est null. |

### Exemple de corps de requête

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) définit une interface de programmation accessible publiquement qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}