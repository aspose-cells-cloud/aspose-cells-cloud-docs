---
title: "Obtenir un graphique à partir d'une feuille de calcul"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, obtenir un graphique, feuille de calcul, API REST, Excel, API graphique, récupération de graphique, graphique Excel"
description: "Récupérer les informations d’un graphique, y compris ses métadonnées et le format d’export, à partir d’une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud."
ArticleTitle: "Obtenir un graphique à partir d'une feuille de calcul – API Aspose.Cells Cloud"
---

Cet API REST permet de récupérer les informations relatives à un graphique.

**Prérequis** – Pour appeler ce point de terminaison, vous devez disposer d’un compte Aspose.Cells Cloud valide, d’un emplacement de stockage actif et d’un jeton d’accès JWT. Obtenez ce jeton en suivant les instructions du guide d’authentification avant de passer toute demande à l’API.

## API GetWorksheetChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                          |
| ---------------- | ------- | ----------- | ---------------------------------------------------- |
| name             | string  | path        | Nom du fichier Excel.                                |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant le graphique. |
| chartNumber      | integer | path        | Index de base zéro du graphique à récupérer.        |
| format           | string  | query       | Format d’export souhaité (par exemple, png, jpeg). |
| folder           | string  | query       | Chemin du dossier où le document est stocké.       |
| storageName      | string  | query       | Nom du service de stockage.                         |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**Codes d’état HTTP**

| Code | Signification            | Description                                                           |
|------|--------------------------|-----------------------------------------------------------------------|
| 200  | OK                       | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request              | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized             | Jeton JWT invalide ou manquant.                                      |
| 413  | Payload Too Large        | Le fichier envoyé dépasse la taille maximale autorisée.            |
| 500  | Internal Server Error    | Erreur serveur inattendue.                                           |

## Comment utiliser l’API GetWorksheetChart à l’aide des SDK

### Spécification de l’API GetWorksheetChart

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}