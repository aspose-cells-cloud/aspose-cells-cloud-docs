---
title: "Obtenir toutes les feuilles de calcul"
second_title: "Document"
linktitle: "Toutes"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, API Cloud, Obtenir les feuilles de calcul, Excel, REST, SDK"
description: "Récupérer la liste des feuilles de calcul dans un classeur Excel via l’API REST Aspose.Cells Cloud (v3.0). Inclut un exemple cURL, des extraits de code SDK et le format de réponse."
weight: 10
---

Cet API REST renvoie des informations sur les feuilles de calcul contenues dans un classeur.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                              |
| ---------------- | ------ | ----------- | ---------------------------------------- |
| name             | string | path        | Le nom du document Excel.                |
| folder           | string | query       | Le dossier contenant le document.        |
| storageName      | string | query       | Le nom du stockage à utiliser.           |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder aux services Aspose.Cells Cloud. L’exemple ci-dessous illustre une requête GET permettant de récupérer les feuilles de calcul.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Gestion des erreurs

Codes d’état HTTP typiques renvoyés par ce point de terminaison :

| Code | Signification         | Description                                    |
| ---- | --------------------- | ---------------------------------------------- |
| 400  | Bad Request           | Paramètre obligatoire manquant (par ex. `name`). |
| 401  | Unauthorized          | Jeton JWT invalide ou manquant.                |
| 404  | Not Found             | Le classeur spécifié n’existe pas.             |
| 500  | Internal Server Error | Condition inattendue côté serveur.             |

Les réponses d’erreur sont renvoyées au format JSON, par exemple :

```json
{
  "Code": "401",
  "Message": "Jeton d’accès invalide."
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}