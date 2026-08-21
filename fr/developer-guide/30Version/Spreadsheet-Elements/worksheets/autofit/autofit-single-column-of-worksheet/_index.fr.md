---
title: "Ajuster automatiquement la largeur d'une colonne dans Excel à l’aide de l’API Aspose.Cells Cloud – Guide rapide"
second_title: "Document"
linktitle: "Colonne"
type: docs
url: /worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: "Aspose.Cells Cloud, ajustement automatique de colonne, API Excel, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Découvrez comment redimensionner automatiquement une colonne (ou une plage de colonnes) dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL, des exemples de SDK (C#, Java, Python, etc.) et tous les détails complets de la requête/réponse."
weight: 10
---

Cette API REST ajuste automatiquement la largeur d'une colonne unique ou d'une plage contiguë de colonnes dans une feuille Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                                      |
| ----------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| name              | string  | chemin      | Le nom du fichier Excel.                                                                         |
| sheetName         | string  | chemin      | Le nom de la feuille de calcul.                                                                  |
| firstColumn       | integer | requête     | Index de base zéro de la première colonne à ajuster automatiquement.                             |
| lastColumn        | integer | requête     | Index de base zéro de la dernière colonne à ajuster automatiquement.                             |
| autoFitterOptions | object  | corps       | Options contrôlant le comportement d’ajustement automatique (voir [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow          | integer | requête     | Index de base zéro de la première ligne prise en compte lors du calcul de la largeur de colonne. |
| lastRow           | integer | requête     | Index de base zéro de la dernière ligne prise en compte lors du calcul de la largeur de colonne. |
| folder            | string  | requête     | Le dossier dans le stockage où le fichier est situé.                                             |
| storageName       | string  | requête     | Le nom du service de stockage.                                                                   |

### Réponses d’erreur

| Statut HTTP | Signification                               | Corps JSON d’exemple                                         |
| ----------- | ------------------------------------------- | ------------------------------------------------------------ |
| 400         | Paramètre(s) invalide(s)                    | `{"Code":400,"Message":"Paramètre invalide 'firstColumn'."}` |
| 401         | Non autorisé – token JWT manquant ou invalide | `{"Code":401,"Message":"Échec de l'authentification."}`      |
| 404         | Fichier ou feuille non trouvé               | `{"Code":404,"Message":"Feuille 'Sheet1' introuvable."}`     |
| 500         | Erreur interne du serveur                   | `{"Code":500,"Message":"Une erreur inattendue s'est produite."}` |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services Aspose.Cells Cloud. L’exemple ci-dessous montre comment invoquer le point de terminaison d’ajustement automatique de colonne.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’intégrer l’API dans votre application. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler le point de terminaison d’ajustement automatique de colonne à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}