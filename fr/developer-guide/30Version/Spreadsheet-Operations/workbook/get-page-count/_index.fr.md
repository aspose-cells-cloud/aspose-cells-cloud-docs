---
title: "Obtenir le nombre de pages à partir d’un fichier Excel"
second_title: "Document"
linktitle: "Pages"
type: docs
url: /fr/get-page-count-from-an-excel-file/
aliases: [  /fr/workbook/page-count/ , /fr/workbook/get/page-count/ ]
keywords: "Aspose.Cells, API Cloud, nombre de pages Excel, pagination du classeur"
description: "Récupérer le nombre total de pages imprimables dans un classeur Excel via l’API REST Aspose.Cells Cloud (v3.0). Inclut le format de la requête, les paramètres requis, un exemple cURL, le schéma de réponse, la gestion des erreurs et des extraits de code SDK pour plusieurs langages."
weight: 10
version: "v3.0"
ArticleTitle: "Obtenir le nombre de pages à partir d’un fichier Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST renvoie le **nombre de pages** d’un classeur.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                              |
| ---------------- | ------ | ----------- | ----------- | ---------------------------------------- |
| name             | string | path        | Oui         | Le nom du fichier Excel.                 |
| folder           | string | query       | Non         | Le dossier contenant le document.        |
| storageName      | string | query       | Non         | Le nom du stockage à utiliser.           |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement à l’API REST Aspose.Cells. L’exemple suivant montre comment appeler le point de terminaison avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/VotreFichier.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

*Remplacez `VotreFichier.xlsx` par le nom réel du classeur que vous souhaitez interroger.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Schéma de réponse

| Statut HTTP | Type de données | Description                                                  |
| ----------- | --------------- | ------------------------------------------------------------ |
| 200         | integer         | Le nombre total de pages imprimables dans le classeur (par ex., `13`). |
| 4xx‑5xx     | JSON            | Objet d’erreur (voir la section _Gestion des erreurs_).      |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Gestion des erreurs

| Statut HTTP | Description                                    | Exemple de corps JSON                                                                     |
| ----------- | ---------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 401         | Jeton JWT invalide ou manquant.                | `{ "Code": "InvalidAuthenticationToken", "Message": "Le jeton d’accès est manquant ou invalide." }` |
| 404         | Le classeur spécifié est introuvable.          | `{ "Code": "FileNotFound", "Message": "Le fichier demandé n’existe pas." }`              |
| 400         | Requête incorrecte – paramètres obligatoires manquants. | `{ "Code": "BadRequest", "Message": "Le paramètre obligatoire 'name' est manquant." }` |
| 500         | Erreur interne du serveur.                     | `{ "Code": "InternalError", "Message": "Une erreur inattendue s’est produite." }`        |
---