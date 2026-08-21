---
title: "Obtenir la zone de graphique à partir d'une feuille de calcul"
type: docs
url: /charts/area/get/
aliases: [/get-chart-area-from-a-worksheet/]
weight: 60
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "ChartArea"
  - "Worksheet"
  - "cURL"
  - "SDK"
  - "GetChartArea"
description: "Découvrez comment récupérer les informations de zone de graphique à partir d'une feuille de calcul à l'aide de l'API REST Aspose.Cells Cloud, avec des exemples pour cURL et plusieurs SDK."
ArticleTitle: "Obtenir la zone de graphique à partir d'une feuille de calcul - API Aspose.Cells Cloud"
---

Cette API REST renvoie les informations relatives à la zone de graphique.

**Conditions préalables :** Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès JWT valide, le classeur cible doit être téléchargé dans le stockage Aspose Cloud, et le format de fichier doit être pris en charge par Aspose.Cells.

**Contexte :** Une zone de graphique définit la boîte englobante extérieure la plus large d’un graphique Excel, incluant les titres, les légendes et la zone de tracé. Récupérer ses propriétés vous permet d’ajuster de manière programmatique la mise en page et le style.

## API GetChartArea

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                      |
| ---------------- | ------ | ----------- | ------------------------------------------------ |
| name             | string | path        | Nom du fichier du classeur.                      |
| sheetName        | string | path        | Nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer| path        | Index de graphique (à partir de zéro).           |
| folder           | string | query       | Dossier dans lequel le classeur est stocké.      |
| storageName      | string | query       | Nom du service de stockage.                      |

### **Réponse**

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                            |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                      |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.    |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                             |

## Comment utiliser l’API GetChartArea à l’aide des SDK

### Spécification de l’API GetChartArea

La <a href="https://apireference.aspose.cloud/cells/#/ChartArea/GetChartArea" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer un appel vers l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartArea-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartArea-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_info-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartArea-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartArea-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "e00e3bbfdf94f400244f1974c3488036" >}}
{{< /tab >}}

{{< /tabs >}}

**Requête HTTP générique (par exemple, à l’aide de fetch) :**

```javascript
fetch('https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'Authorization': 'Bearer <jeton JWT>'
  }
})
  .then(response => response.json())
  .then(data => console.log(data));
```