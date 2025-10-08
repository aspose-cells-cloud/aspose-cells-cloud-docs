---
title: Obtenir la version du fichier
second_title: Documen
linktitle: Obtenir la version du fichier
type: docs
url: /fr/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Récupérez et gérez les versions des fichiers stockés dans le Cloud Aspose.Cells, améliorant ainsi la gestion des documents et la collaboration
weight: 100
kwords: Obtenir les versions de fichiers, Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, gestion de documents
---
## **Excel API : Obtenir les versions des fichiers**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Description de la fonction**

 Le**Obtenir les versions de fichiers** API permet aux utilisateurs de récupérer les différentes versions d'un fichier spécifié stocké dans le Cloud Aspose.Cells. Cette fonctionnalité est essentielle pour préserver l'intégrité du document et suivre les modifications au fil du temps.

###  Les paramètres de la requête de**Obtenir les versions de fichiers** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| chemin| Chaîne| Chemin| Le chemin d'accès au fichier pour lequel les versions doivent être récupérées.|
| nom de stockage| Chaîne| Requête| Le nom du stockage où se trouve le fichier.|

### **Description de la réponse**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)fournit une interface de programmation complète pour exécuter des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 L'utilisation d'un SDK simplifie le développement en abstrayant les complexités de bas niveau, permettant ainsi aux développeurs de se concentrer sur les fonctionnalités essentielles. Explorez[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells dans différents langages de programmation :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
