---
title: Répartition par lots
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API prend en charge les fichiers fractionnés par lots. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, fractionnement par lots
---
Ce REST API indique le `batch split` du dossier éligible.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
|BatchSplitRequest|| corps||

**Propriétés BatchSplitRequest**
 
Nom | Tapez | Descriptif | Remarques
------------ | ------------- | ------------- | -------------
 Dossier Source | chaîne | | [facultatif]SourceStorage | chaîne | | [facultatif]Condition de correspondance | CorrespondanceConditionRequest | | [facultatif]Formater | chaîne | | [facultatif]DeIndex | entier | | [facultatif]VersIndex | entier | | [facultatif]OutFolder | chaîne | | [facultatif]EnregistrerOptions | EnregistrerOptions | | [facultatif]**Propriétés MatchConditionRequest**
 
Nom | Tapez | Descriptif | Remarques
------------ | ------------- | ------------- | -------------
 Modèle Regex | chaîne | | [facultatif]Conditions FullMatch | chaîne[]| | [facultatif]Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
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
 
## Famille de SDK Cloud
 
 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur vos tâches fractionnées. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}

