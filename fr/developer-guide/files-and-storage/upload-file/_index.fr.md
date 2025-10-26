---
title: Télécharger le fichier sur la cellule Aspose
second_title: Developer Guide for File Uploa
linktitle: Télécharger le fichier
type: docs
url: /fr/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: Guide complet sur la façon de télécharger des fichiers à l'aide du Aspose Cells API, y compris les paramètres et la structure de réponse
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, faire correspondre toutes les cellules vides dans une feuille de calcul Excel, télécharger le fichier
---
## **Aspose Cells API : Télécharger le fichier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Description de la fonction**

 Le**télécharger un fichier** API permet aux développeurs de télécharger des fichiers directement sur le stockage cloud pour traitement avec Aspose Cells.

###  Les paramètres de la requête de**télécharger un fichier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Télécharger des fichiers| Déposer| Données de formulaire|Téléchargez des fichiers vers le stockage cloud.|
| chemin| Chaîne| Chemin| Chemin de destination dans le stockage cloud. Spécifiez le chemin où le fichier doit être téléchargé.|
| nom de stockage| Chaîne| Requête| Le nom du stockage où le fichier sera téléchargé.|

### **Description de la réponse**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) fournit une description détaillée du API, permettant aux développeurs d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Aspose Cells API Kit de développement logiciel

 L'utilisation d'un SDK améliore l'efficacité du développement en gérant les détails de bas niveau, permettant ainsi aux développeurs de se concentrer sur les tâches du projet. Visitez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
