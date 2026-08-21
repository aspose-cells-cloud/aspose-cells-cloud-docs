---
title: "Ajouter un graphique à une feuille de calcul"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Découvrez comment ajouter un graphique à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud v3.0. Inclut l’endpoint, les paramètres, un exemple cURL et des extraits de code SDK."
keywords:
  - "ajouter un graphique Aspose.Cells"
  - "API Aspose.Cells pour ajouter un graphique"
  - "API REST pour graphiques"
  - "exemples de SDK Aspose.Cells"
ArticleTitle: "Ajouter un graphique à une feuille de calcul – Guide de l’API Aspose.Cells Cloud"
---

Cette API REST ajoute un nouveau graphique à une feuille de calcul.

**Prérequis**  
Avant d’appeler cette opération, obtenez un jeton d’accès JWT valide et assurez-vous que le classeur cible est stocké dans le dossier ou l’emplacement de stockage spécifié.

## API PutWorksheetAddChart

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre        | Type    | Emplacement | Description                                                                                                                                                                              |
| ----------------------- | ------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | string  | path        | Nom du classeur.                                                                                                                                                                         |
| **sheetName**           | string  | path        | Nom de la feuille de calcul.                                                                                                                                                            |
| **chartType**           | string  | query       | Type de graphique (voir la propriété **Type** dans la ressource graphique). Les types de graphiques pris en charge incluent **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar**, etc. |
| **upperLeftRow**        | integer | query       | Index de ligne supérieure gauche de la zone du graphique (indexé à partir de 0).                                                                                                       |
| **upperLeftColumn**     | integer | query       | Index de colonne supérieure gauche de la zone du graphique (indexé à partir de 0).                                                                                                     |
| **lowerRightRow**       | integer | query       | Index de ligne inférieure droite de la zone du graphique (indexé à partir de 0).                                                                                                       |
| **lowerRightColumn**    | integer | query       | Index de colonne inférieure droite de la zone du graphique (indexé à partir de 0).                                                                                                     |
| **area**                | string  | query       | Plage fournissant les valeurs à représenter (par exemple, `A1:B5`).                                                                                                                     |
| **isVertical**          | boolean | query       | Indique si l’orientation du graphique est verticale.                                                                                                                                    |
| **categoryData**        | string  | query       | Plage des valeurs de l’axe des catégories (par exemple, `D1:E10`).                                                                                                                      |
| **isAutoGetSerialName** | boolean | query       | Si **true**, les noms de séries sont générés automatiquement.                                                                                                                           |
| **title**               | string  | query       | Titre du graphique.                                                                                                                                                                     |
| **folder**              | string  | query       | Dossier contenant le classeur.                                                                                                                                                          |
| **storageName**         | string  | query       | Nom du stockage.                                                                                                                                                                        |
| **dataLabels**          | boolean | query       | Afficher les étiquettes de données si **true**.                                                                                                                                         |
| **dataLabelsPosition**  | string  | query       | Position des étiquettes de données (par exemple, `Above`).                                                                                                                              |
| **pivotTableSheet**     | string  | query       | Nom de la feuille contenant le tableau croisé dynamique.                                                                                                                                |
| **pivotTableName**      | string  | query       | Nom du tableau croisé dynamique.                                                                                                                                                        |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT invalide ou manquant.                                             |
| 413  | Payload Too Large           | Le fichier téléchargé dépasse la taille limite.                           |
| 500  | Internal Server Error       | Erreur serveur inattendue.                                                  |

## Comment utiliser l’API PutWorksheetAddChart avec les SDK

### Spécification de l’API PutWorksheetAddChart

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Aucun corps de requête n’est requis pour cette opération
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

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK abstrait les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}