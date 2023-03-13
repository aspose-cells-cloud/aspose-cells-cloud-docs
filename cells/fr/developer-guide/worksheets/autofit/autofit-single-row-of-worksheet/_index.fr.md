---
title: Ajuster automatiquement une ligne sur une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ro
type: docs
url: /fr/worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
keywords: Autofit rows on an Excel workshee
description: Aspose.Cells Cloud REST API prend en charge l'ajustement automatique d'une ligne sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 30
---
Ce REST API indique d'ajuster automatiquement une ligne sur une feuille de calcul Excel.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| NomFeuille| chaîne| chemin||
| index de ligne| entier| mettre en doute||
| première colonne| entier| mettre en doute||
| dernièreColonne| entier| mettre en doute||
| autoFitterOptions|| corps||
| dossier| chaîne| mettre en doute||
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRow) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&lastColumn=10&firstColumn=1" \
-X POST \
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
 
 
 
{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "5b27cb12deedc47e434c4d0bf70ef00b" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "4df97bb1460dcfa974cb04303e643583" >}}

{{< /tab >}}

{{< /tabs >}}
