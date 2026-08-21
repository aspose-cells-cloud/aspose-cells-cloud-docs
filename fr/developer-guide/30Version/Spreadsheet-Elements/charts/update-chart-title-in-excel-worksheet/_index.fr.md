---
title: "Mettre à jour le titre d’un graphique dans une feuille Excel"
type: docs
url: /charts/title/update/
aliases: [/update-chart-title-in-excel-worksheet/]
weight: 160
keywords: Excel, Aspose.Cells, API REST, Titre de graphique, Mise à jour, SDK cloud
description: Découvrez comment mettre à jour le titre d’un graphique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud, de cURL et de divers SDK.
ArticleTitle: "Mettre à jour le titre d’un graphique dans une feuille Excel – Documentation Aspose.Cells Cloud"
---

Cette API REST met à jour le titre d’un graphique.

**Prérequis :** Vous devez disposer d’un compte Aspose Cloud valide et d’un jeton JWT pour l’authentification. Les étapes typiques comprennent :

- Créer un compte Aspose Cloud.  
- Générer un jeton JWT via le point de contact d’authentification.  
- Vérifier que le classeur cible est stocké dans un espace de stockage cloud pris en charge (par défaut ou personnalisé).

## API PostWorksheetChartTitle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Tous les appels à l’API doivent être effectués via **HTTPS** afin d’éviter les avertissements liés aux contenus mixtes.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                           |
| ---------------- | ------- | ----------- | ------------------------------------- |
| name             | string  | path        | Nom du classeur.                      |
| sheetName        | string  | path        | Nom de la feuille de calcul.          |
| chartIndex       | integer | path        | Indice du graphique (base zéro).      |
| title            | string  | body        | Nouveau titre du graphique.           |
| folder           | string  | query       | Dossier contenant le classeur.        |
| storageName      | string  | query       | Nom de l’espace de stockage.          |

### Codes de statut de la réponse

| Code | Description                                              |
| ---- | -------------------------------------------------------- |
| 200  | OK – Le titre du graphique a été mis à jour avec succès. |
| 400  | Requête incorrecte – Paramètres manquants ou non valides. |
| 401  | Non autorisé – Jeton JWT invalide ou manquant.          |
| 404  | Non trouvé – Classeur, feuille de calcul ou graphique introuvable. |
| 500  | Erreur interne du serveur – Condition inattendue sur le serveur. |

**Remarque :** L’index `chartIndex` est en base zéro ; le premier graphique sur une feuille de calcul est référencé avec `0`.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Bourse de valeurs"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
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

## Famille de SDK cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}