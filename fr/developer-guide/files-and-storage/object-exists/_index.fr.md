---
title: Objet existant
second_title: Documen
linktitle: Objet existant
type: docs
url: /fr/object-exists/
keywords: Excel API, Object Exists, REST API, Aspose, File Management, Excel, Office Cloud, Spreadsheet, PDF, CSV, JSON, Markdow
description: L'objet existe API vérifie si un fichier ou un dossier spécifié existe dans le stockage cloud Aspose.Cells
weight: 100
kwords: Excel API, Objet existant, REST API, Aspose, Office Cloud, Gestion de fichiers, Tableur, PDF, CSV, JSON, Markdown, Vérifier l'existence du fichier dans Excel
---
## **Excel API : L'objet existe**

```
GET http://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **Description de la fonction**

Le `objectExists` API permet aux développeurs de vérifier l'existence d'un fichier ou d'un dossier spécifié dans le stockage cloud Aspose.Cells.

###  Les paramètres de la requête de**objetExiste** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|chemin|Chaîne|Chemin|Le chemin d'accès au fichier ou au dossier dans le stockage cloud.|
|nom de stockage|Chaîne|Requête|Le nom du stockage où se trouve le fichier.|
|versionId|Chaîne|Requête|L'ID de version du fichier (le cas échéant).|

### **Description de la réponse**

```json
{
  "Name": "ObjectExist",
  "Description": [
    "Object exists"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates that the file or folder exists."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    },
    {
      "Name": "IsFolder",
      "Description": [
        "True if it is a folder, false if it is a file."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
