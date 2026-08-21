---
title: "Obtenir toutes les tables croisées dynamiques dans une feuille Excel"
second_title: "Document"
linktitle: Obtenir toutes les tables croisées dynamiques
type: docs
url: /pivot-tables/get-all/
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "obtenir toutes les tables croisées dynamiques, API Aspose.Cells Cloud, Excel PivotTable, API REST"
description: "Récupérer toutes les tables croisées dynamiques d'une feuille Excel via l'API Aspose.Cells Cloud. Inclut l'endpoint, les paramètres, les étapes d'authentification, les exemples cURL et les SDK pour l'API PivotTables."
weight: 20
ArticleTitle: "Obtenir toutes les tables croisées dynamiques dans une feuille Excel – API Aspose.Cells Cloud"
---

Une **table croisée dynamique (PivotTable)** est un outil de synthèse de données dans Excel qui vous permet de réorganiser et d’analyser de grands jeux de données. Cette API REST permet de récupérer les informations concernant **toutes** les tables croisées dynamiques présentes dans une feuille spécifiée.

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                      |
| ---------------- | ------ | ----------- | ------------------------------------------------ |
| name             | string | path        | Nom du document Excel.                           |
| sheetName        | string | path        | Nom de la feuille de calcul.                     |
| folder           | string | query       | Dossier dans lequel le document est stocké.     |
| storageName      | string | query       | Nom du service de stockage.                      |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Requête

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

### Réponse

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Réponses d’erreur

| Code HTTP | Description                                                          | Exemple de charge utile JSON                                    |
| --------- | -------------------------------------------------------------------- | --------------------------------------------------------------- |
| 400       | Requête incorrecte – paramètre requis manquant.                     | `{ "Code": "400", "Message": "Paramètre requis manquant." }`   |
| 401       | Non autorisé – jeton invalide ou manquant.                          | `{ "Code": "401", "Message": "Échec de l’authentification." }` |
| 404       | Non trouvé – classeur, feuille ou table croisée dynamique introuvable. | `{ "Code": "404", "Message": "Ressource introuvable." }`       |
| 500       | Erreur interne du serveur – condition inattendue sur le serveur.   | `{ "Code": "500", "Message": "Erreur serveur." }`              |

## Famille de SDK Cloud

L'utilisation d'un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}
---