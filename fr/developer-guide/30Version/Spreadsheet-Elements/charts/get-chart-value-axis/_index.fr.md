---
title: "Obtenir l'axe des valeurs d'un graphique"
type: docs
url: /charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Axe des valeurs d'un graphique, API REST, Excel, SDK Cloud, Obtenir l'axe des valeurs d'un graphique
description: "API REST Aspose.Cells Cloud – Récupérer l'axe des valeurs d’un graphique dans une feuille Excel."
ArticleTitle: "Obtenir l'axe des valeurs d'un graphique – Aspose.Cells Cloud REST API"
---

Cette API REST récupère l'axe des valeurs d’un graphique. Elle fait partie de l’**API REST Aspose.Cells Cloud** et fonctionne avec des feuilles Excel stockées dans le cloud.

Pour des opérations connexes, consultez le point de terminaison **[Obtenir l'axe des catégories d'un graphique](/charts/category-axis/get/)**.

## API GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                               |
|------------------|---------|-------------|-----------------------------------------------------------|
| name             | string  | path        | Le nom du fichier Excel (incluant l’extension).          |
| sheetName        | string  | path        | Le nom de la feuille contenant le graphique.             |
| chartIndex       | integer | path        | L’indice de base zéro du graphique dans la feuille.      |
| folder           | string  | query       | Le dossier dans le stockage cloud où le fichier se trouve. |
| storageName      | string  | query       | Le nom du service de stockage (par exemple, Aspose Cloud). |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Valeurs",
    "Format": {
      "NumberFormat": "Général",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Codes d’état HTTP possibles**

| Code | Description                                                         |
|------|---------------------------------------------------------------------|
| 200  | Succès – les informations relatives à l’axe des valeurs sont retournées. |
| 400  | Requête incorrecte – des paramètres obligatoires sont manquants ou invalides. |
| 401  | Non autorisé – le jeton d’authentification est manquant ou invalide. |
| 404  | Introuvable – le classeur, la feuille ou le graphique spécifié n’existe pas. |
| 500  | Erreur interne du serveur – une erreur inattendue s’est produite côté serveur. |

La réponse contient un objet détaillé `ValueAxis` comportant des propriétés telles que `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` et `Format`. Dans une implémentation complète, des détails supplémentaires de formatage pourraient être fournis.

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L'utilisation d'un SDK est le moyen le plus efficace d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
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