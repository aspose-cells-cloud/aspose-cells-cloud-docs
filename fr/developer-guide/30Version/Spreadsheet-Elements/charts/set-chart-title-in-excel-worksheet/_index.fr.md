---
title: "Aspose.Cells Cloud API – Définir le titre d’un graphique dans une feuille Excel"
type: docs
url: /fr/chart/title/add/
aliases: [  /fr/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, API de titre de graphique, titre de graphique Excel, API REST, exemples de SDK"
description: "Découvrez comment ajouter ou mettre à jour le titre d’un graphique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL et SDK, les paramètres requis, les étapes d’authentification et la gestion des erreurs."
---

Ajoute un titre de graphique ou rend visible un titre existant.

## API PutWorksheetChartTitle

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                              |
| ---------------- | ------ | ----------- | ---------------------------------------- |
| name             | string | path        | Nom du classeur.                         |
| sheetName        | string | path        | Nom de la feuille de calcul.             |
| chartIndex       | integer| path        | Index du graphique.                      |
| title            | string | body        | Texte du titre du graphique.             |
| folder           | string | query       | Dossier contenant le classeur.           |
| storageName      | string | query       | Nom du stockage.                         |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Réponses d’erreur**

| Code HTTP | Charge utile d’exemple                                                           | Description                                                    |
| --------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| 400       | `{ "Code": "400", "Message": "Charge utile de requête invalide." }`             | Le corps de la requête est mal formé ou des champs obligatoires sont absents. |
| 401       | `{ "Code": "401", "Message": "Échec de l’authentification. Jeton JWT invalide ou expiré." }` | Le jeton bearer est manquant, invalide ou expiré.              |
| 404       | `{ "Code": "404", "Message": "Classeur, feuille de calcul ou graphique introuvable." }` | La ressource spécifiée n’existe pas.                            |
| 500       | `{ "Code": "500", "Message": "Erreur interne du serveur." }`                    | Une erreur inattendue s’est produite sur le serveur.           |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK abstrait les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}