﻿---
title: Ajouter un espacement de page horizontal
second_title: Aspose.Cells Cloud Documen
linktitle: Ajouter un espacement de page horizontal
type: docs
url: /fr/page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: Add a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'un saut de page dans une feuille de calcul Excel. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Ajouter un saut de page horizontal
---
Ce REST API indique d'insérer `vertical` saut de page.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| Nom de la feuille| chaîne| chemin||
| nom de cellule| chaîne| requête||
| rangée| entier| requête||
| colonne| entier| requête||
| colonneDébut| entier| requête||
| finColonne| entier| requête||
| dossier| chaîne| requête||
| Nom de stockage| chaîne| requête| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
-X PUT \
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
 
## Famille de SDK Cloud
 
 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0742361abdbe07508ef0054a3b8a0bb4" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2462937944298a09a75b64f4c34889b7" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "e82a5628425ae5f59cd211c579b30073" >}}

{{< /tab >}}

{{< /tabs >}}
