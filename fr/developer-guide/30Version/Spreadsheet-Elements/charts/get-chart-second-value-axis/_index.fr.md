---
title: "Obtenir l'axe des valeurs secondaire d'un graphique"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, axe des valeurs secondaire d'un graphique, Excel, API REST, cloud, API, axe de graphique Excel
description: Récupère l'axe des valeurs secondaire d'un graphique spécifié dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud.
ArticleTitle: "Obtenir l'axe des valeurs secondaire d'un graphique – API Aspose.Cells Cloud"
---

Cette API REST récupère l'axe des valeurs secondaire d'un graphique.

## API GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                             |
| ---------------- | ------- | ----------- | ------------------------------------------------------- |
| name             | string  | path        | Le nom du fichier Excel.                                |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer | path        | L’index de base zéro du graphique.                      |
| folder           | string  | query       | Le dossier dans lequel le fichier est stocké.          |
| storageName      | string  | query       | Le nom du stockage Aspose Cloud.                        |

**Prérequis** : Un jeton d’accès JWT valide obtenu via le flux OAuth2 Aspose Cloud doit être fourni dans l’en-tête `Authorization` de chaque requête.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST à partir d’un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL. Tous les points de terminaison Aspose Cloud utilisent HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Axe des valeurs secondaire"
  }
}
```

**Champs de la réponse**

- **Code** – Code d’état HTTP de l’opération (par exemple, `200` pour succès).  
- **Status** – Description textuelle de l’état (`"OK"` pour succès).  
- **Axis** – Objet contenant les détails de l’axe des valeurs secondaire :  
  - **AxisId** – Identifiant de l’axe.  
  - **IsVisible** – Booléen indiquant si l’axe est affiché.  
  - **MinimumScale** – Valeur minimale affichée sur l’axe.  
  - **MaximumScale** – Valeur maximale affichée sur l’axe.  
  - **MajorUnit** – Intervalle entre les graduations majeures.  
  - **MinorUnit** – Intervalle entre les graduations mineures.  
  - **Title** – Texte du titre de l’axe.

**Réponses d’erreur** (non 200)

- `400 Bad Request` – Paramètres invalides ou requête mal formée.  
- `401 Unauthorized` – Jeton JWT manquant ou invalide.  
- `404 Not Found` – Le fichier, la feuille de calcul ou le graphique spécifié n’existe pas.  
- `500 Internal Server Error` – Erreur serveur inattendue.

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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
---