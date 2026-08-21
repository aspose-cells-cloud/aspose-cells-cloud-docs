---
title: "Ajouter un filtre de couleur dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter un filtre de couleur"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, filtre de couleur, Aspose.Cells Cloud, API REST, filtre automatique, authentification JWT"
description: "Découvrez comment appliquer un filtre de couleur à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Inclut le point de terminaison, les paramètres, un exemple cURL, la gestion des erreurs et des exemples de SDK."
weight: 65
ArticleTitle: "Ajouter un filtre de couleur dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Découvrez comment ajouter un filtre de couleur à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Ce guide couvre le point de terminaison requis, les paramètres, les conditions préalables d’authentification, une requête cURL d’exemple, des exemples de SDK et la gestion des réponses.

Cette API REST ajoute un **filtre de couleur** à une feuille de calcul Excel.

## API PutWorksheetColorFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête :

| Nom du paramètre | Type    | Emplacement | Description                                                                 |
|------------------|---------|-------------|-----------------------------------------------------------------------------|
| name             | string  | path        | Le nom du fichier Excel.                                                    |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant les données à filtrer.            |
| range            | string  | query       | La plage de cellules à laquelle le filtre est appliqué (par exemple, `A1:B10`). |
| fieldIndex       | integer | query       | Index de colonne à base zéro sur lequel le filtre de couleur est appliqué. |
| colorFilter      | object  | body        | Objet JSON qui définit les couleurs de premier plan et d’arrière-plan à filtrer. |
| matchBlanks      | boolean | query       | Indique si les lignes contenant des cellules vides doivent être incluses dans les résultats du filtre. |
| refresh          | boolean | query       | Si `true`, la feuille de calcul est actualisée après application du filtre. |
| folder           | string  | query       | Le dossier dans le stockage où se trouve le fichier Excel.                 |
| storageName      | string  | query       | Le nom du service de stockage (par exemple, Aspose Cloud Storage).         |

**Schéma JSON de `colorFilter`**

| Propriété         | Type   | Description                                                                    | Obligatoire |
|-------------------|--------|--------------------------------------------------------------------------------|-------------|
| Pattern           | string | Motif de filtrage (par exemple, `"Solid"`).                                   | Oui         |
| ForegroundColor   | object | Définit la couleur de premier plan. Contient des sous‑propriétés telles que `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` et `Type`. | Non |
| BackgroundColor   | object | Définit la couleur d’arrière-plan. Mêmes sous‑propriétés que `ForegroundColor`. | Non |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification                | Description                                                                 |
|------|------------------------------|-----------------------------------------------------------------------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur.                                               |

## Comment utiliser l’API PutWorksheetColorFilter à l’aide des SDK

### Spécification de l’API PutWorksheetColorFilter

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

L’utilisation d’un SDK est la meilleure façon d’accélérer le développement. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi :** [Ajouter un filtre personnalisé](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Ajouter un filtre de date](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Supprimer un filtre automatique](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
---