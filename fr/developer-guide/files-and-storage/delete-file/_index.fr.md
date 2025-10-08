---
title: Supprimer le fichier - Excel AP
second_title: Documen
linktitle: Supprimer le fichier
type: docs
url: /fr/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Découvrez comment supprimer des fichiers dans Excel à l'aide de Aspose.Cells API. Ce guide fournit des informations détaillées sur le point de terminaison deleteFile API, les paramètres de requête et la structure de réponse.
weight: 100
kwords: Supprimer le fichier, Excel API, REST API, Office Cloud, Gestion des feuilles de calcul, Suppression de fichiers, Stockage cloud, API usag
---
## **Excel API : Supprimer le fichier**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Description de la fonction**

 Le**supprimer le fichier** API permet aux utilisateurs de supprimer des fichiers spécifiés du stockage cloud, garantissant ainsi une gestion efficace des ressources et des données.

###  Les paramètres de la requête pour le**supprimer le fichier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|chemin|Chaîne|Chemin|Le chemin vers le fichier qui doit être supprimé.|
|nom de stockage|Chaîne|Requête|Nom du stockage où se trouve le fichier. Facultatif si le stockage par défaut est utilisé.|
|versionId|Chaîne|Requête|L'ID de version du fichier à supprimer, le cas échéant.|

### **Description de la réponse**

```json
{
Void
}
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
