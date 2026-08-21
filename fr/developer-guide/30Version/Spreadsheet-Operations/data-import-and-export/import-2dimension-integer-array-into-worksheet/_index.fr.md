---
title: "Importer un tableau d’entiers à 2 dimensions dans une feuille Excel"
second_title: "Document"
linktitle: "Importer un tableau d’entiers à 2 dimensions"
type: docs
url: /import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, importation d’un tableau d’entiers à 2 dimensions, feuille Excel, API REST, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "L’API REST Aspose.Cells Cloud permet d’importer des tableaux d’entiers à deux dimensions dans des feuilles Excel. Des SDK sont disponibles pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 20
---

Cette API REST **importe un tableau d’entiers à deux dimensions** dans une feuille Excel.

La requête est une requête HTTP dont le contenu est multiparte (voir [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu multiparte contient les données `Import2DimensionIntegerArrayOption`, tandis que la deuxième partie contient le fichier de données.

Les paramètres importants sont décrits dans le tableau suivant :

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Import2DimensionIntegerArrayOption**

| Nom du paramètre     | Type       | Description                                                                                                                                                                                  |
| -------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Index 1‑basé de la première ligne où les données seront placées.                                                                                                                            |
| FirstColumn          | int        | Index 1‑basé de la première colonne où les données seront placées.                                                                                                                         |
| Data                 | Integer[,] | Tableau d’entiers à deux dimensions contenant les valeurs à importer.                                                                                                                               |
| DestinationWorksheet | string     | Nom de la feuille de calcul de destination.                                                                                                                                                           |
| IsInsert             | string     | `"true"` pour insérer les données (décalage des cellules existantes), `"false"` pour remplacer les cellules existantes.                                                                                                |
| ImportDataType       | string     | Spécifie le format des données. Valeurs prises en charge : `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source               | FileSource | Indique l’emplacement du fichier de données lorsque le paramètre `BatchData` est `null`.                                                                                                                   |

### **Exemple**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Fichier téléchargé dépassant la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) définit une interface de programmation accessible publiquement qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utilisation des SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}