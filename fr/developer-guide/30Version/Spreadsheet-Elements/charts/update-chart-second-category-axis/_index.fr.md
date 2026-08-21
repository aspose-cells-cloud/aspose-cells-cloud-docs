---
title: "Mettre à jour l'axe de catégorie secondaire d'un graphique"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, graphique, axe de catégorie secondaire, API REST, mettre à jour un graphique, Excel, API cloud"
description: "Découvrez comment mettre à jour l'axe de catégorie secondaire d’un graphique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud."
ArticleTitle: "Mettre à jour l’axe de catégorie secondaire d’un graphique – Aspose.Cells Cloud API"
---

Cet API REST met à jour l’axe de catégorie secondaire d’un graphique.

## API PostChartSecondCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                              |
| ---------------- | ------- | ----------- | -------------------------------------------------------- |
| name             | string  | path        | Le nom du fichier Excel.                                 |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant le graphique.  |
| chartIndex       | integer | path        | L’index à base zéro du graphique à mettre à jour.       |
| axis             | object  | body        | L’objet représentant l’axe de catégorie secondaire avec les nouveaux paramètres. |
| folder           | string  | query       | Le chemin du dossier où le fichier est stocké.          |
| storageName      | string  | query       | Le nom du service de stockage.                           |

**Authentification** – L’API exige un jeton d’accès OAuth 2.0 valide. Générez un jeton JWT en suivant le [Guide d’authentification](https://docs.aspose.cloud/cells/authentication/). Incluez le jeton dans l’en-tête `Authorization`, comme indiqué dans l’exemple cURL ci-dessous.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{ 
        "axis": {
          /* paramètres de l’axe, par ex. : "Title": "Nouveau titre d’axe", "IsVisible": true */
        }
      }'
```

*Remplacez `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` et `{storageName}` par vos valeurs réelles. Le corps de la requête doit contenir l’objet `axis` avec les paramètres souhaités.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Réponse réussie (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Nouveau titre d’axe",
      "IsVisible": true,
      /* propriétés supplémentaires de l’axe */
    }
  }
}
```

**Réponses d’erreur**  

| Code d’état | Description                                               |
|-------------|-----------------------------------------------------------|
| 400         | Requête incorrecte – paramètres manquants ou non valides. |
| 401         | Non autorisé – jeton JWT invalide ou manquant.            |
| 404         | Non trouvé – le fichier, la feuille ou le graphique spécifié n’existe pas. |
| 500         | Erreur interne du serveur – condition inattendue sur le serveur. |

```json
{
  "Code": 400,
  "Message": "Charge utile de requête non valide."
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Les SDK simplifient le développement en gérant les détails de bas niveau et en vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- Exemple C# (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Exemple Java (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- Exemple PHP (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Exemple Ruby (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Exemple Python (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Exemple Android (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Exemple Swift (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Exemple Perl (espace réservé) -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Exemple Go (espace réservé) -->

{{< /tab >}}

{{< /tabs >}}

**Notes et bonnes pratiques**

* Le paramètre `chartIndex` est à base zéro ; le premier graphique d’une feuille de calcul a l’index 0.  
* L’API prend en charge les formats de classeur `.xlsx` et `.xls`.  
* Incluez uniquement les propriétés nécessaires dans l’objet `axis` ; les propriétés non spécifiées conservent leurs valeurs actuelles.  
* Respectez les limites de taux (généralement 100 requêtes par minute par compte) pour éviter la limitation.