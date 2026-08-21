---
title: "Obtenir l'axe des catégories d'un graphique"
type: docs
url: /fr/charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Axe des catégories de graphique, Excel, API REST, Stockage cloud, OAuth2, Documentation de l'API"
description: "Récupère l'axe des catégories d'un graphique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud."
ArticleTitle: "Obtenir l'axe des catégories d'un graphique – Documentation de l'API Aspose.Cells Cloud"
---

Cet API REST récupère l’**axe des catégories** d’un graphique.  
Pour appeler ce point de terminaison, vous devez fournir un jeton d’accès OAuth 2.0 valide, et le classeur doit être stocké dans le stockage Aspose Cloud.

**Conditions préalables**  
Avant d’utiliser ce point de terminaison, assurez-vous que :  

- Un jeton OAuth 2.0 a été obtenu et est valide pour les services Aspose Cloud.  
- Le fichier classeur est téléversé dans le stockage Aspose Cloud (par défaut ou dans un dossier spécifié).  
- Vous utilisez la version **v3.0** de l’API, comme indiqué dans l’URL de la requête.  
- L’application appelante dispose des autorisations de lecture du classeur et d’accès à ses feuilles de calcul.

## API GetChartCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Contexte** – Supprimer tous les graphiques d’une feuille de calcul est utile lorsque vous devez réinitialiser la mise en page visuelle d’une feuille, remplacer des visualisations obsolètes ou préparer un classeur pour une réutilisation sans conserver les données des graphiques précédents.

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                            |
| ---------------- | ------- | ----------- | ------------------------------------------------------ |
| name             | string  | path        | Le nom du fichier classeur.                            |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer | path        | Indice de graphique (indexé à partir de zéro) dont l’axe est demandé. |
| folder           | string  | query       | Le chemin du dossier dans le stockage où réside le classeur. |
| storageName      | string  | query       | Le nom du service de stockage (si différent de celui par défaut). |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Payload trop volumineux     | Le fichier téléversé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

## Comment utiliser l’API GetChartCategoryAxis avec les SDK

### Spécification de l’API GetChartCategoryAxis

La <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- Exemple C# placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Exemple Java placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- Exemple PHP placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Exemple Ruby placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Exemple Python placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Exemple Android placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Exemple Swift placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Exemple Perl placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Exemple Go placeholder -->

{{< /tab >}}

{{< /tabs >}}
---