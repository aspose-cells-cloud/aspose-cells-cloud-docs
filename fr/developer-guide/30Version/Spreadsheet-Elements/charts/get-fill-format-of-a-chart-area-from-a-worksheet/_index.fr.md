---
title: "Obtenir le format de remplissage de la zone de graphique – API Aspose.Cells Cloud (v3.0)"
type: docs
url: /fr/charts/chart-area/fill-format/get/
aliases: [  /fr/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Zone de graphique"
  - "Format de remplissage"
  - "API REST"
  - "Excel"
description: "Récupérer le format de remplissage (couleur, motif, dégradé) d'une zone de graphique dans une feuille de calcul Excel via l'API Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK, les étapes d'authentification et les détails de la réponse."
ArticleTitle: "Obtenir le format de remplissage de la zone de graphique – API Aspose.Cells Cloud v3.0"
---

Cet API REST permet de récupérer les informations de format de remplissage d'une **zone de graphique**.

**Prérequis**  
Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès OAuth/JWT valide. Obtenez ce jeton en suivant le flux d’authentification d’Aspose.Cells Cloud, puis incluez-le dans l’en-tête `Authorization` sous la forme `Bearer <jeton jwt>`. Si vous utilisez l’un des SDK, assurez-vous que le SDK est configuré avec vos identifiants `client_id` et `client_secret` avant d’invoquer la méthode.

## API GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                              |
| ---------------- | ------- | ----------- | ---------------------------------------- |
| name             | string  | path        | Nom du classeur.                         |
| sheetName        | string  | path        | Nom de la feuille de calcul.             |
| chartIndex       | integer | path        | Index du graphique.                      |
| folder           | string  | query       | Dossier contenant le classeur.           |
| storageName      | string  | query       | Nom du stockage.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler cette API à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Remarques**  
- Une requête réussie renvoie le code HTTP 200 accompagné des détails du format de remplissage.  
- Le code HTTP 401 indique une défaillance d’authentification (jeton invalide ou manquant).  
- Le code HTTP 404 est renvoyé si le classeur, la feuille de calcul ou l’index du graphique spécifié n’existe pas.  
- Le code HTTP 500 signale une erreur côté serveur ; réessayez la requête ou contactez le support si le problème persiste.

| Code | Signification                                           |
|------|---------------------------------------------------------|
| 200  | Succès – format de remplissage renvoyé                  |
| 401  | Non autorisé – jeton invalide ou manquant               |
| 404  | Non trouvé – classeur, feuille de calcul ou graphique introuvable |
| 500  | Erreur interne du serveur                               |

Pour des opérations connexes, consultez les points de terminaison **Get Chart Area Border** (Obtenir la bordure de la zone de graphique) et **Get Chart Title** (Obtenir le titre du graphique).

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}