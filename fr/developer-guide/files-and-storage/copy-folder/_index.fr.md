---
title: Copier le dossier
second_title: Documen
linktitle: Copier le dossier
type: docs
url: /fr/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: Apprenez à utiliser CopyFolder API pour copier efficacement des dossiers dans l'environnement cloud Aspose.Cells
weight: 100
kwords: Excel, Office Cloud, REST API, Copier un dossier, Gestion de fichiers, PDF, CSV, JSON, Markdown, Correspondance de toutes les cellules vides dans une feuille de calcul Excel
---
## **Excel API : Copier le dossier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Description de la fonction**

 Le**Copier le dossier**API permet aux utilisateurs de dupliquer un dossier existant dans le stockage cloud Aspose.Cells. Cette fonctionnalité est essentielle pour gérer efficacement les fichiers, permettant aux utilisateurs de créer des sauvegardes ou d'organiser leur travail sans transférer manuellement le contenu.

###  Les paramètres de la requête**Copier le dossier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|----------------|--|-----------------------|-------------------------------------|
| chemin source| Chaîne| Chemin| Le chemin du dossier source à copier.|
| chemin de destination| Chaîne| Requête| Le chemin où le nouveau dossier sera créé.|
| srcStorageName| Chaîne| Requête| Le nom du stockage contenant le dossier source.|
| destStorageName| Chaîne| Requête| Le nom du stockage de destination où le dossier doit être copié.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
