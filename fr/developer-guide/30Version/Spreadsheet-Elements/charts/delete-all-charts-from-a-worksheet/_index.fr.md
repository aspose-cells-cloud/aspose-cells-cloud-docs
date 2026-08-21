---
title: "Supprimer tous les graphiques d'une feuille de calcul"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, Cloud, suppression, tous les graphiques, feuille de calcul, API REST, DELETE, SDK"
description: "Découvrez comment supprimer tous les graphiques d'une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL de l’endpoint, les paramètres, un exemple cURL, des extraits de code SDK, les étapes d’authentification et la gestion des erreurs."
ArticleTitle: "Supprimer tous les graphiques d'une feuille de calcul à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST supprime tous les graphiques de la feuille de calcul spécifiée.

**Contexte** – La suppression de tous les graphiques d’une feuille de calcul est utile lorsque vous devez réinitialiser la mise en page visuelle d’une feuille, remplacer des visualisations obsolètes ou préparer un classeur pour une réutilisation sans conserver les données de graphiques précédentes.

Avant d’appeler l’API, veuillez vous assurer que les conditions préalables suivantes sont remplies :

- Un jeton JWT valide est disponible pour l’authentification.  
- Le fichier classeur existe à l’emplacement et dans le dossier de stockage spécifiés.  
- Vous utilisez la version **v3.0** de l’API.

## API DeleteWorksheetClearCharts

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                      |
| ---------------- | ------ | ----------- | ------------------------------------------------ |
| name             | string | path        | Nom du fichier classeur.                         |
| sheetName        | string | path        | Nom de la feuille de calcul.                     |
| folder           | string | query       | Dossier dans lequel le classeur est stocké.     |
| storageName      | string | query       | Nom du stockage.                                 |

**En-têtes de la requête**

| En-tête         | Description                    |
|-----------------|--------------------------------|
| Authorization   | Bearer `<jeton jwt>`           |
| Accept          | `application/json`             |
| Content-Type    | `application/json` (aucun corps)|

**Corps de la requête**

L’opération DELETE **n’exige pas** de corps de requête.

**Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                           |
|------|-----------------------------|-----------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                      |
| 413  | Charge utile trop volumineuse | Le fichier envoyé dépasse la taille maximale autorisée.            |
| 500  | Erreur interne du serveur   | Erreur inattendue survenue sur le serveur.                           |

*Exemples de réponses d’erreur*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Paramètre non valide : 'sheetName' est obligatoire."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Échec de l’authentification. Jeton JWT invalide."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "La charge utile de la requête dépasse la taille maximale autorisée."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Une erreur inattendue s’est produite sur le serveur."
}
```

## Comment utiliser l’API DeleteWorksheetClearCharts avec les SDK

### Spécification de l’API DeleteWorksheetClearCharts

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```


{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode optimale pour accélérer le développement lorsqu’il s’agit de **supprimer tous les graphiques** d’une feuille de calcul. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---