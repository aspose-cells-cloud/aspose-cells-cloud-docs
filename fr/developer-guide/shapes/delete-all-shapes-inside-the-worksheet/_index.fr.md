---
title: Supprimer toutes les formes sur une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Cléa
type: docs
url: /fr/shapes/clear/
aliases: [/delete-all-shapes-inside-the-worksheet/]
keywords: Delete all shapes on an Excel workshee
description: Aspose.Cells Cloud REST API prend en charge la suppression de toutes les formes sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 40
---
Ce REST API indique de supprimer toutes les formes sur une feuille de calcul Excel.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| NomFeuille| chaîne| chemin| nom de la feuille de calcul.|
| dossier| chaîne| mettre en doute| Dossier du document.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
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
 
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-DeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "a92427978a88b27918aeec5929efff97" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-DeleteWorksheetShapes.swift" >}}

{{< /tab >}}

{{< /tabs >}}
