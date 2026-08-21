---
title: "Obtenir les cellules fusionnées à partir d'une feuille Excel – API Aspose.Cells Cloud"
type: docs
url: /fr/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, cellules fusionnées, feuille Excel, API REST, SDK Aspose.Cells, cellules fusionnées Excel"
description: "Découvrez comment récupérer les plages de cellules fusionnées à partir d'une feuille Excel à l’aide de l’API Aspose.Cells Cloud (v3.0). Inclut les étapes d’authentification, la requête cURL complète, le schéma de réponse, la gestion des erreurs et des exemples de SDK en C#, Java, Python, et plus encore."
---

Cette API REST renvoie des informations sur les **cellules fusionnées** dans une feuille Excel.

> **Remarque** – L’objet API s’appelle **MergedCell** (au singulier). Dans le texte, nous désignons le *concept* de cellules fusionnées (au pluriel).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                              |
|------------------|--------|-------------|------------------------------------------|
| **name**         | string | path        | Nom du fichier Excel.                    |
| **sheetName**    | string | path        | Nom de la feuille de calcul.             |
| **folder**       | string | query       | Dossier contenant le document.           |
| **storageName**  | string | query       | Nom du stockage à utiliser.              |

## **Réponse**

Renvoie un objet `MergedCellsResponse`.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                               |
|------|----------------------------|-----------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                           |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite.          |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue.                                |

## Comment utiliser l’API GetWorksheetMergedCells avec les SDK

### Spécification de l’API GetWorksheetMergedCells

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande `cURL` pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer un appel à l’API Cloud avec `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer avec l’API. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}