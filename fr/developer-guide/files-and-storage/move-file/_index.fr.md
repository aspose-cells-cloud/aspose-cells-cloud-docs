---
title: Déplacer le fil
second_title: Documen
linktitle: Déplacer le fil
type: docs
url: /fr/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Apprenez à utiliser MoveFile API pour gérer les fichiers dans le stockage cloud Aspose.Cells
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdown, Déplacer un fichier, Gestion de fichiers, Stockage Cloud
---
## **Excel API : Déplacer le fichier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Description de la fonction**

 Le**déplacer le fichier** API vous permet de déplacer un fichier d'un emplacement à un autre dans le stockage cloud Aspose.Cells. Ceci est particulièrement utile pour organiser les fichiers et gérer efficacement le stockage.

###  Les paramètres de la requête de**déplacer le fichier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|---------------|--|------------------------|--------------------------------------|
| chemin source| Chaîne| Chemin| Le chemin source du fichier à déplacer.|
| chemin de destination| Chaîne| Requête| Le chemin de destination où le fichier sera déplacé.|
| srcStorageName| Chaîne| Requête| Le nom du stockage source, le cas échéant.|
| destStorageName| Chaîne| Requête|Le nom du stockage de destination, le cas échéant.|
| versionId| Chaîne| Requête| L'ID de version du fichier, le cas échéant.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
