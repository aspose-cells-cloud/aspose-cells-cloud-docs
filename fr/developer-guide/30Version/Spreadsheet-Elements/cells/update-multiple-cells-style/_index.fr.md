---
title: "Mettre à jour le style de plusieurs cellules – Référence de l’API Aspose.Cells Cloud (v3.0)"
type: docs
url: /fr/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "mettre à jour le style de plusieurs cellules", "API de style de cellule Excel", "SDK cloud", "API REST", "exemple cURL", "requête JSON", "authentification JWT"]
description: "Découvrez comment mettre à jour le style d'une plage de cellules dans un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut l’endpoint, la méthode HTTP, les paramètres, les exemples cURL et SDK, l’authentification, la gestion des erreurs et les informations de version."
ArticleTitle: "Mettre à jour le style de plusieurs cellules – Référence de l’API Aspose.Cells Cloud (v3.0)"
---

## API REST

Cette API REST définit le **style** pour une plage de cellules dans un classeur Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| **name**         | string | path        | Nom du classeur. |
| **sheetName**    | string | path        | Nom de la feuille de calcul. |
| **range**        | string | query       | Plage de cellules (par exemple, `A1:A10`). |
| **style**        | object | body        | Objet JSON définissant le style à appliquer. |
| **folder**       | string | query       | Dossier contenant le classeur. |
| **storageName**  | string | query       | Nom du stockage. |

#### Objet style
L'objet JSON `style` représente le formatage des cellules. Il peut contenir l'une ou plusieurs des propriétés facultatives suivantes :

- **Font** – Paramètres de police (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, etc.).  
- **BackgroundColor** – Couleur d’arrière-plan au format ARGB.  
- **ForegroundColor** – Couleur de premier plan au format ARGB.  
- **Name**, **CultureCustom**, **Custom** – Métadonnées supplémentaires du style.

## **Réponse**

Renvoie un `CellCloudResponse`.

- **Aperçu des champs de réponse**

| Champ             | Type    | Description                                           |
| ----------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                                                       |
| `Code`            | integer | 200, 400, 401, 500, ...                               |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                         |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |
## Comment utiliser l’API PostUpdateWorksheetRangeStyle avec les SDK

### Spécification de l’API PostUpdateWorksheetRangeStyle

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) fournit le schéma complet.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
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

L'utilisation d'un SDK est le moyen le plus efficace d'accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}