---
title: Créer un dossier
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/folder/create/
keywords: Learn how to create folder with Aspose Cells Cloud REST API
description: Apprenez à créer un dossier avec Aspose Cells Cloud REST API SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 100
---
Ce REST API indique `create folder`.

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin|Chemin du dossier à créer par exemple 'dossier_1/dossier_2/' |
| nom_stockage| chaîne| mettre en doute| Nom de stockage|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
 
 

