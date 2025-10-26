---
title: Supprimer le dossier
second_title: Documen
linktitle: Supprimer le dossier
type: docs
url: /fr/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: Apprenez à supprimer un dossier dans Aspose.Cells à l'aide de deleteFolder API, y compris les paramètres et les exemples de code
weight: 100
kwords: Excel API, Office Cloud, REST API, Gestion des feuilles de calcul, PDF, CSV, JSON, Markdown, supprimer le dossier dans la feuille de calcul Excel
---
## **Excel API : Supprimer le dossier**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Description de la fonction**

Le `deleteFolder` API permet aux utilisateurs de supprimer un dossier spécifié du stockage cloud associé à Aspose.Cells. Cela peut être utile pour maintenir l'organisation et gérer efficacement le stockage.

###  Les paramètres de la requête de**supprimer le dossier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| chemin| Chaîne| Chemin| Le chemin du dossier à supprimer.|
| nom de stockage| Chaîne| Requête| Le nom du stockage où se trouve le dossier.|
| récursif| Booléen| Requête| Indique si la suppression doit être récursive, en supprimant également tout le contenu du dossier.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
