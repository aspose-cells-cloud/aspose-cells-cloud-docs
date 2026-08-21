---
title: "Ajuster automatiquement plusieurs lignes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Lignes"
type: docs
url: /fr/worksheets/autofit/rows/
aliases: [  /fr/autofit-multiple-rows-of-worksheet/ ]
keywords: "ajuster automatiquement les lignes, Excel, Aspose.Cells Cloud, API REST, feuille de calcul, classeur"
description: "Découvrez comment utiliser l'API REST Aspose.Cells Cloud pour ajuster automatiquement plusieurs lignes dans une feuille de calcul Excel. Inclut la syntaxe de la requête, les paramètres, un exemple cURL, des extraits de code SDK et la gestion des erreurs."
weight: 40
ArticleTitle: "Ajuster automatiquement plusieurs lignes dans une feuille de calcul Excel – Documentation de l'API Aspose.Cells Cloud"
---

Cette API REST ajuste automatiquement la hauteur des lignes dans une feuille de calcul Excel.

## Sécurité et authentification
Les API REST Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Paramètres de la requête**

| Nom du paramètre      | Type    | Emplacement | Description                                                                                                                          | Obligatoire |
| --------------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------- |
| **name**              | string  | path        | Le nom du fichier Excel.                                                                                                             | ✔ |
| **sheetName**         | string  | path        | Le nom de la feuille de calcul.                                                                                                      | ✔ |
| **autoFitterOptions** | object  | body        | Options contrôlant la façon dont les lignes sont ajustées automatiquement (par exemple, ignorer les lignes masquées). Voir la description brève des champs ci-dessous. | ✖ |
| **startRow**          | integer | query       | La première ligne à ajuster automatiquement (index basé sur 1).                                                                      | ✔ |
| **endRow**            | integer | query       | La dernière ligne à ajuster automatiquement (inclus).                                                                                | ✔ |
| **onlyAuto**          | boolean | query       | Si `true`, l'API ajuste uniquement les lignes dont la hauteur est calculée automatiquement par Excel. Si `false`, un ajustement complet est effectué. | ✖ |
| **folder**            | string  | query       | Le dossier contenant le document.                                                                                                    | ✖ |
| **storageName**       | string  | query       | Le nom du service de stockage.                                                                                                       | ✖ |

Champs de **autoFitterOptions** (tous facultatifs) :

- `AutoFitMergedCells` _(boolean)_ – Si `true`, les cellules fusionnées sont prises en compte lors du calcul de la hauteur des lignes.
- `IgnoreHidden` _(boolean)_ – Si `true`, les lignes masquées sont ignorées pendant le processus d’ajustement automatique.
- `OnlyAuto` _(boolean)_ – Reprend la valeur du paramètre de requête `onlyAuto` ; lorsqu’il est défini, il remplace la valeur du paramètre de requête.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Les réponses d’erreur typiques incluent :

- **400 Bad Request** – Valeurs de paramètres invalides ou corps JSON mal formé.
- **401 Unauthorized** – Jeton JWT manquant ou invalide.
- **404 Not Found** – Le fichier ou la feuille de calcul spécifié n’existe pas.
- **500 Internal Server Error** – Une erreur serveur inattendue s’est produite.

**Codes de statut HTTP**

| Code | Signification               | Description                                        |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT invalide ou manquant. |
| 413  | Payload Too Large           | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Internal Server Error       | Erreur serveur inattendue. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}