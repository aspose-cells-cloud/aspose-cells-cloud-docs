---
title: "Supprimer un graphique d'une feuille de calcul"
type: docs
url: /charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Supprimer un graphique"
  - "Feuille de calcul"
  - "Excel"
  - "Cloud SDK"
  - "Suppression de graphique"
  - "Référence API"
description: "Supprime un graphique d'une feuille de calcul à l’aide de son index à base zéro via l’API REST Aspose.Cells Cloud."
ArticleTitle: "Supprimer un graphique d'une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud"
---

Cet API REST supprime un graphique de feuille de calcul à l’aide de son index.

Pour les opérations connexes, consultez les pages **[Ajouter un graphique](#)** et **[Obtenir un graphique](#)**.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                             |
| ---------------- | ------- | ----------- | ------------------------------------------------------- |
| name             | string  | path        | Le nom du classeur.                                     |
| sheetName        | string  | path        | Le nom de la feuille de calcul.                         |
| chartIndex       | integer | path        | L'index à base zéro du graphique à supprimer.           |
| folder           | string  | query       | Le dossier contenant le classeur.                       |
| storageName      | string  | query       | Le nom du stockage à utiliser.                          |


### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                                 |
|------|----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise demande           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la taille limite.                            |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                                               |

## Comment utiliser l’API PutWorksheetAddChart à l’aide des SDK

### Spécification de l’API PutWorksheetAddChart

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

L’API renvoie les codes de statut suivants :

| Code | Description                                    |
|------|------------------------------------------------|
| 200  | Graphique supprimé avec succès                |
| 400  | Mauvaise demande (par exemple, index invalide) |
| 401  | Non autorisé (jeton JWT manquant ou invalide)  |
| 404  | Classeur, feuille de calcul ou graphique introuvable |
| 500  | Erreur serveur                                 |

**Gestion des erreurs :** Pour des informations détaillées sur les erreurs, reportez-vous au modèle d’erreur générique dans la spécification OpenAPI.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}