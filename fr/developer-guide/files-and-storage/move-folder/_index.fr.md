---
title: Déplacer le dossier
second_title: Documen
linktitle: Déplacer le dossier
type: docs
url: /fr/move-folder/
keywords: Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storag
description: Cette documentation fournit un guide complet sur l'utilisation du Move Folder API pour la gestion des dossiers dans le stockage cloud Aspose.Cells
weight: 100
kwords: Excel API, Déplacer le dossier API, Office Cloud, REST API, Gestion des feuilles de calcul, PDF, CSV, JSON, Markdown, Faire correspondre toutes les cellules vides dans une feuille de calcul Excel
---
## **Excel API : Déplacer le dossier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Description de la fonction**

Ce fichier API permet aux utilisateurs de déplacer un dossier d'un emplacement à un autre dans le stockage cloud Aspose.Cells. Il est essentiel pour organiser les fichiers et gérer efficacement le stockage cloud.

###  Les paramètres de la requête de**déplacer le dossier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|----------------|--|------------------------|--------------------------------------------------------|
| chemin source| Chaîne| Chemin| Le chemin source du dossier à déplacer.|
| chemin de destination| Chaîne| Requête| Le chemin de destination où le dossier doit être déplacé.|
| srcStorageName| Chaîne| Requête| Le nom du stockage source.|
| destStorageName| Chaîne| Requête| Le nom du stockage de destination.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
