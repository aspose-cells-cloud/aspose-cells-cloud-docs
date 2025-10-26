---
title: Obtenir la liste des fichiers - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Obtenir la liste des fichiers
type: docs
url: /fr/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Apprenez à récupérer une liste de fichiers d'un dossier spécifié à l'aide de Aspose.Cells API. Ce guide fournit des détails sur les paramètres de requête, la structure de la réponse et des exemples de code dans divers langages de programmation.
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Gestion de fichiers Cloud, Obtenir la liste des fichiers
---
## **Excel API : Obtenir la liste des fichiers**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Description de la fonction**

 Le**obtenir la liste des fichiers**API permet aux utilisateurs de récupérer une liste complète des fichiers et dossiers contenus dans un répertoire spécifié du stockage cloud Aspose.Cells. Ce point de terminaison est essentiel pour une gestion efficace des fichiers et prend en charge différents formats de fichiers.

###  Les paramètres de la requête de**obtenir la liste des fichiers** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| chemin| Chaîne| Chemin| Le chemin d'accès au dossier dans le stockage cloud à partir duquel récupérer la liste des fichiers.|
| nom de stockage| Chaîne| Requête| Le nom du stockage auquel accéder.|

### **Description de la réponse**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) définit une interface de programmation accessible au public qui permet des interactions REST directement à partir d'un navigateur Web, facilitant ainsi l'intégration et les tests.

## Excel API Kit de développement logiciel

 Utiliser un SDK est la meilleure approche pour accélérer votre processus de développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Pour obtenir la liste complète des SDK Cloud Aspose.Cells, veuillez consulter le site[Dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
