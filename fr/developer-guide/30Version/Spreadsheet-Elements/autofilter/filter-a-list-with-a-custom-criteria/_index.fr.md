---
title: "Ajouter un critère personnalisé dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter un filtre personnalisé"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, filtre personnalisé, Aspose.Cells Cloud, API REST, filtre automatique, feuille de calcul, critère personnalisé"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour ajouter un filtre personnalisé à une feuille de calcul Excel. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages de programmation."
weight: 65
ArticleTitle: "Ajouter un critère personnalisé dans une feuille de calcul Excel – Aspose.Cells Cloud API"
---

Cette API REST permet de filtrer une liste à l’aide d’un **critère personnalisé**.

## API PutWorksheetCustomFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête :

| Nom du paramètre | Type    | Emplacement                   | Description                                                                 |
|------------------|---------|-------------------------------|-----------------------------------------------------------------------------|
| name             | string  | path                          | Nom du fichier Excel.                                                       |
| sheetName        | string  | path                          | Nom de la feuille de calcul contenant les données à filtrer.               |
| range            | string  | query                         | Plage de cellules à laquelle le filtre sera appliqué (par ex. `A1:B1`).    |
| fieldIndex       | integer | query                         | Index (à partir de 0) de la colonne sur laquelle le filtre est appliqué.   |
| operatorType1    | string  | query                         | Premier opérateur de comparaison (par ex. `LessOrEqual`, `Equal`).         |
| criteria1        | string  | query                         | Première valeur ou expression de filtrage.                                 |
| isAnd            | boolean | query                         | Si `true`, combine les deux critères avec **ET** ; sinon **OU**.           |
| operatorType2    | string  | query                         | Deuxième opérateur de comparaison (facultatif).                            |
| criteria2        | string  | query                         | Deuxième valeur ou expression de filtrage (facultatif).                    |
| matchBlanks      | boolean | query                         | Si `true`, les cellules vides sont incluses dans les résultats du filtre.  |
| refresh          | boolean | query                         | Si `true`, force le rafraîchissement de la feuille de calcul après application du filtre. |
| folder           | string  | query                         | Chemin du dossier dans le stockage où le fichier est situé.                |
| storageName      | string  | query                         | Nom du service de stockage.                                                 |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                                 |
|------|----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier envoyé dépasse la taille limite autorisée.                     |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                                          |

## Comment utiliser l’API PutWorksheetCustomFilter à l’aide des SDK

### Spécification de l’API PutWorksheetCustomFilter

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur la logique de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Pour d'autres opérations d'AutoFilter, telles que l'ajout d'un filtre standard ou d'un filtre de date, veuillez consulter les pages de documentation associées dans la section AutoFilter.