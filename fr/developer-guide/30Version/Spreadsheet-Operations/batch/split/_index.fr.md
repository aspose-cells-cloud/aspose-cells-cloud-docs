---
title: Séparation par lots
second_title: Documen
type: docs
url: /fr/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API prend en charge le fractionnement de fichiers par lots. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Fractionnement par lots
---
Ce REST API indique au `batch split` du dossier éligible.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| Demande de fractionnement de lot|| corps||

**Propriétés de BatchSplitRequest**

Nom | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 SourceFolder | chaîne | | [optionnel]SourceStorage | chaîne | | [optionnel]MatchCondition | MatchConditionRequest | | [optionnel]Format | chaîne | | [optionnel]FromIndex | entier | | [optionnel]ToIndex | entier | | [optionnel]OutFolder | chaîne | | [optionnel]SaveOptions | SaveOptions | | [optionnel]**Propriétés de MatchConditionRequest**

Nom | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 RegexPattern | chaîne | | [facultatif]FullMatchConditions | chaîne[]| | [facultatif]Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches fractionnées. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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

{{< /tabs >}}
