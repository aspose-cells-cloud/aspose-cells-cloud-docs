﻿---
title: Ajouter un objet de liste dans une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Publicité
type: docs
url: /fr/list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/,/tables/add/]
keywords: Add a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'un objet de liste (table) dans une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 10
---
Ce REST API indique `add a list object(table)` dans une feuille de calcul Excel.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| NomFeuille| chaîne| chemin| Le nom de la feuille de calcul.|
| startRow| entier| mettre en doute| La ligne de début de la plage de liste.|
| startColumn| entier| mettre en doute| La ligne de début de la plage de liste.|
| endRow| entier| mettre en doute| La ligne de début de la plage de liste.|
| finColonne| entier| mettre en doute| La ligne de début de la plage de liste.|
| hasHeaders| booléen| mettre en doute| Vrai|
| listeObjet|| corps| Objet de liste|
| dossier| chaîne| mettre en doute| Dossier du document.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="4" tabID="4" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="Go" >}}

{{< tab tabNum="1" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "6da60ae8d508b08871b2a0b692732ce7" >}}

{{< /tab >}}

{{< /tabs >}}
