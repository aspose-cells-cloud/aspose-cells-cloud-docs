---
title: "Ajouter un filtre dans une feuille Excel"
second_title: "Document"
linktitle: "Ajouter un filtre"
type: docs
url: /fr/autofilter/add-filter/
aliases: [  /fr/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, Ajouter un filtre, REST API, SDK"
description: "Découvrez comment ajouter un filtre automatique à une colonne d'une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut des exemples cURL, des exemples SDK et un guide des paramètres."
weight: 60
ArticleTitle: "Ajouter un filtre dans une feuille Excel à l’aide d’Aspose.Cells Cloud"
---

**Conditions préalables :** Avant d’appeler cette API, vous devez obtenir un jeton JWT valide, vous assurer que le classeur cible est téléchargé dans le stockage spécifié, et disposer des autorisations nécessaires pour accéder au fichier. Une version récente de cURL (7.68 ou ultérieure) est recommandée pour les exemples en ligne de commande.

Cette API REST ajoute un filtre pour une colonne spécifique dans une feuille Excel.

## API PutWorksheetFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description |
|------------------|---------|-------------|-------------|
| name             | string  | Path        | Le nom du classeur. |
| sheetName        | string  | Path        | Le nom de la feuille de calcul. |
| range            | string  | Query       | La plage de cellules contenant le filtre (par exemple, `A1:B1`). |
| fieldIndex       | integer | Query       | Index de base zéro de la colonne à laquelle le filtre est appliqué. |
| criteria         | string  | Query       | Les critères du filtre (par exemple, une valeur ou une expression). |
| matchBlanks      | boolean | Query       | Définir sur `true` pour inclure les cellules vides dans le filtre ; sinon `false`. |
| refresh          | boolean | Query       | Définir sur `true` pour actualiser le filtre après application ; sinon `false`. |
| folder           | string  | Query       | Le dossier où le classeur original est stocké. |
| storageName      | string  | Query       | Le nom du service de stockage. |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

## Comment utiliser l’API PutWorksheetFilter avec les SDK

### Spécification de l’API PutWorksheetFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}