---
title: "Mettre à jour l’axe des catégories d’un graphique"
type: docs
url: /fr/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, graphique, axe des catégories, API REST, Excel, SDK cloud"
description: "Met à jour l’axe des catégories d’un graphique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud."
ArticleTitle: "Mettre à jour l’axe des catégories d’un graphique – Aspose.Cells Cloud API"
---

Cet API REST met à jour l’axe des catégories d’un graphique.

## API PostChartCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description |
| ---------------- | ------- | ----------- | ----------- |
| name             | string  | path        | Nom du fichier Excel. |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer | path        | Index de base zéro du graphique à mettre à jour. |
| axis             | object  | body        | Objet JSON définissant les propriétés de l’axe des catégories. |
| folder           | string  | query       | Dossier dans le stockage cloud où se trouve le fichier (facultatif). |
| storageName      | string  | query       | Nom du stockage (facultatif). |

**Schéma du corps de la requête – objet `axis`**

| Propriété                | Type    | Description |
|--------------------------|---------|-------------|
| IsAutomaticMajorUnit     | boolean | Indique si l’unité majeure est calculée automatiquement. |
| MajorUnit                | number  | Valeur de l’unité majeure lorsque `IsAutomaticMajorUnit` est `false`. |
| IsAutomaticMinorUnit     | boolean | Indique si l’unité mineure est calculée automatiquement. |
| MinorUnit                | number  | Valeur de l’unité mineure lorsque `IsAutomaticMinorUnit` est `false`. |
| Title                    | object  | Paramètres du titre de l’axe (par exemple, `Text`, `Font`, `Visible`). |
| TickLabelPosition        | string  | Position des étiquettes de graduation (par exemple, `Low`, `High`, `NextToAxis`). |
| ...                      | ...     | Propriétés supplémentaires de l’axe, comme défini dans la spécification de l’API. |

**Codes d’état HTTP**

| Code | Signification               | Description |
|------|-----------------------------|-------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléversé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

**Prérequis / Authentification**

Pour appeler ce point de terminaison, vous devez obtenir un jeton d’accès JWT auprès du service d’authentification Aspose.Cells Cloud (`/connect/token`). Incluez ce jeton dans l’en-tête `Authorization`, comme indiqué dans l’exemple ci-dessous.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Axe des catégories",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Exemple de réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Notes

* Le point de terminaison exige l’utilisation de HTTPS ; l’utilisation de HTTP peut provoquer des avertissements de contenu mixte dans les navigateurs.
* Toutes les valeurs de substitution (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) doivent être remplacées par des identifiants réels.
* Les types de graphiques pris en charge pour la mise à jour de l’axe des catégories sont listés dans la référence de l’API.

## Famille de SDK cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}