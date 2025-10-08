---
title: Stockage existant
second_title: Documen
linktitle: Stockage existant
type: docs
url: /fr/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Découvrez comment vérifier l'existence d'un espace de stockage à l'aide du REST Aspose.Cells API. Ce guide fournit des informations détaillées sur le point de terminaison API, les paramètres de requête et les descriptions de réponse.
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Correspond à toutes les cellules vides d'une feuille de calcul Excel
---
## **Excel API : Stockage existant**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Description de la fonction**

 Le**stockageExiste**API vérifie si un stockage spécifié existe dans le service cloud Aspose.Cells. Cette fonctionnalité est essentielle pour garantir que toutes les opérations dépendant du stockage se déroulent sans erreur.

###  Les paramètres de la requête de**stockageExiste** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom de stockage|Chaîne|Chemin|Le nom du stockage dont l'existence doit être vérifiée.|

### **Description de la réponse**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
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

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) définit une interface de programmation accessible au public, permettant aux développeurs d'interagir de manière transparente avec le REST API directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est l'approche la plus efficace pour accélérer le développement. Un SDK résume les détails d'implémentation de bas niveau, permettant aux développeurs de se concentrer sur leurs projets. Pour une liste complète des SDK Cloud Aspose.Cells disponibles, veuillez consulter le site[Dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment effectuer des appels API vers des services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
