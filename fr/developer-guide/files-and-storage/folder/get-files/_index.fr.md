﻿---
title: Obtenir le fichier
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/folder/get-files/
keywords: Learn how to get files from folder with Aspose Cells Cloud REST API
description: Découvrez comment obtenir un fichier à partir d'un dossier avec Aspose Cells Cloud REST API SDK prenant en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, obtenir des fichiers
---
Ce REST API indique `get files`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du dossier, par exemple '/folder'|
| Nom de stockage| chaîne| requête| Nom de stockage|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille de SDK Cloud
 
 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
 
 
 

