---
title: "Mettre à jour les propriétés d’un graphique"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, graphique, mise à jour, Excel, API REST, SDK"
description: "Découvrez comment mettre à jour les propriétés d’un graphique (type, titre, légende, etc.) dans un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint, les paramètres, un exemple cURL et des extraits de code SDK pour C#, Java, PHP, Ruby, Node.js, Perl et Go."
ArticleTitle: "Mettre à jour les propriétés d’un graphique – Aspose.Cells Cloud REST API"
---

Cet API REST permet de mettre à jour les propriétés d’un graphique.

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API PostWorksheetChart

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                   |
| ---------------- | ------- | ----------------------------------------------------- | ------------------------------------------------------------- |
| name             | string  | path                                                  | Nom du fichier Excel.                                         |
| sheetName        | string  | path                                                  | Nom de la feuille de calcul contenant le graphique.          |
| chartIndex       | integer | path                                                  | Index (à zéro) du graphique à mettre à jour.                  |
| chart            | object  | body                                                  | Objet JSON définissant les propriétés du graphique à modifier. |
| folder           | string  | query                                                 | Dossier dans le stockage où le fichier est situé.             |
| storageName      | string  | query                                                 | Nom du service de stockage.                                   |

### Schéma du corps de la requête

L’objet **`chart`** contient les propriétés que vous pouvez modifier. Voici un exemple JSON représentatif incluant plusieurs champs couramment utilisés :

```json
{
  "Title": {
    "Text": "Chiffre d'affaires trimestriel"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Remarque :** Vous devez uniquement fournir les champs que vous souhaitez modifier. Les propriétés omises conservent leurs valeurs actuelles.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton JWT>"
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

## Réponse

L’API renvoie un objet JSON indiquant le résultat de l’opération. Une mise à jour réussie renvoie :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut en cas de succès**

| Statut HTTP | Description                                            |
| ----------- | ------------------------------------------------------ |
| 200         | OK – les propriétés du graphique ont été mises à jour. |

**En-têtes de réponse**

| En-tête         | Description                                                                 |
| --------------- | -------------------------------------------------------------------------- |
| `Content-Type`  | `application/json` – indique que le corps de la réponse est au format JSON. |
| `X-RequestId`   | Identifiant unique de la requête (utile pour le débogage).                |

Les réponses d’erreur possibles incluent :

| Statut HTTP | Description                                                |
| ----------- | ---------------------------------------------------------- |
| 400         | Requête incorrecte – paramètres ou corps invalide          |
| 401         | Non autorisé – jeton manquant ou invalide                  |
| 404         | Non trouvé – fichier, feuille de calcul ou graphique introuvable |
| 500         | Erreur interne du serveur                                  |

Pour d’autres opérations liées aux graphiques, voir les sujets connexes tels que [Mettre à jour le titre du graphique](/charts/title/update/) et [Mettre à jour la légende du graphique](/charts/legend/update/).

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}