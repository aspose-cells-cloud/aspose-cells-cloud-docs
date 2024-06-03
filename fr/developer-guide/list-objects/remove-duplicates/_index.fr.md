---
title:  Objet de liste supprimer les doublons
second_title: Aspose.Cells Cloud Documen
linktitle: Supprimer le doublon
type: docs
keywords: list object(table) remove duplicates 
url: /fr/list-objects/remove-duplicates/
description:  Supprimez les doublons sur l’objet de liste.
weight: 20
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, objet liste supprimer les doublons
---
 Ce REST API indique la suppression des doublons sur l'objet de liste.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 Les paramètres de la requête sont :

| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin||
|Nom de la feuille|Chaîne|Chemin||
|listeObjetIndex|Entier|Chemin||
|dossier|Chaîne|Requête||
|Nom de stockage|Chaîne|Requête||



 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le référentiel GitHub pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
