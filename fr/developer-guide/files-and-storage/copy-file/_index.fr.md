---
title: Copier le fichier - Excel AP
second_title: Documen
linktitle: Copier le fichier
type: docs
url: /fr/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Apprenez à utiliser CopyFile API pour Excel pour dupliquer efficacement des feuilles de calcul et gérer différents formats de fichiers
weight: 100
kwords: Excel API, Office Cloud, REST API, Copie de feuille de calcul, PDF Conversion, Export CSV, Gestion JSON, Prise en charge Markdown, Copie de fichier Excel, Correspondance de cellule vide
---
## **Excel API : Copier le fichier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Description de la fonction**

 Le**copier le fichier** API permet aux utilisateurs de dupliquer un fichier Excel d'un chemin source spécifié vers un chemin de destination, prenant en charge diverses options de stockage.

###  Les paramètres de la requête de**copier le fichier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|-------------- ||--------------------- |-------------------------------------- |
| chemin source| Chaîne| Chemin| Le chemin source du fichier à copier.|
| chemin de destination| Chaîne| Requête| Le chemin de destination où le fichier sera enregistré.|
| srcStorageName| Chaîne| Requête| Le nom du stockage source.|
| destStorageName| Chaîne| Requête| Le nom du stockage de destination.|
| versionId| Chaîne| Requête| ID de version facultatif du fichier à copier.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/CopyFile) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
