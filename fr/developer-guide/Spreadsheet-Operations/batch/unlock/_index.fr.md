﻿---
title: Déblocage par lots
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/batch/unlock
keywords: Batch unlock of multiple Excel files
description: Aspose.Cells Cloud API prend en charge le déverrouillage par lots de plusieurs fichiers Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Déverrouillage par lots
---
Ce REST API indique `batch unlock` de fichiers éligibles.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| Demande de verrouillage par lots|| corps||

**Propriétés de BatchLockRequest**

Nom | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 SourceFolder | chaîne | | [facultatif]MatchCondition | MatchConditionRequest | | [facultatif]Password | chaîne | | [facultatif]OutFolder | chaîne | | [facultatif]**Propriétés de MatchConditionRequest**

Nom | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 RegexPattern | chaîne | | [facultatif]FullMatchConditions | chaîne[]| | [facultatif]Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}" 
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

Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de déverrouillage. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}
