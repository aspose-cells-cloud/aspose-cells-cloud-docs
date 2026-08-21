---
title: "Convertir un graphique Excel en image – Aspose.Cells Cloud REST API"
type: docs
url: /fr/charts/to-image/
aliases: [  /fr/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud, conversion graphique en image, conversion graphique Excel, API REST, format d’image, PNG, JPEG, BMP, TIFF, GIF"
description: "Découvrez comment convertir des objets graphiques Excel en images PNG, JPEG, BMP, TIFF ou GIF à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails des points de terminaison, des paramètres, un exemple cURL, des extraits de code SDK, un exemple de réponse et la gestion des erreurs."
ArticleTitle: "Convertir un graphique Excel en image – Aspose.Cells Cloud REST API"
---

Cet API REST explique comment convertir un **graphique Excel** en image à l’aide d’**Aspose.Cells Cloud**.

## API PutWorksheetAddChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Les formats d’image pris en charge sont les suivants : `png`, `jpeg`, `bmp`, `tiff` et `gif`.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                     |
| ---------------- | ------- | ----------- | ------------------------------- |
| name             | string  | path        | Nom du document.                |
| sheetName        | string  | path        | Nom de la feuille de calcul.    |
| chartNumber      | integer | path        | Numéro du graphique.            |
| format           | string  | query       | Format du fichier exporté.      |
| folder           | string  | query       | Dossier du document.            |
| storageName      | string  | query       | Nom du stockage.                |

### **Réponse**

Le point de terminaison renvoie le fichier image dans le format demandé sous forme de flux binaire (par exemple, `byte[]`). L’en-tête `Content-Type` de la réponse correspond au format d’image sélectionné, par exemple `image/png`, `image/jpeg`, etc.

**Codes de statut HTTP**

| Code | Signification              | Description                                           |
|------|----------------------------|-------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                       |
| 413  | Charge utile trop grande   | Le fichier uploadé dépasse la limite de taille.     |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                         |

## Comment utiliser l’API PutWorksheetAddChart à l’aide des SDK

### Spécification de l’API PutWorksheetAddChart

La <a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <votre_jeton_jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, ce qui vous permet de vous concentrer sur les tâches de votre projet. Consultez le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Exemple à venir bientôt.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}