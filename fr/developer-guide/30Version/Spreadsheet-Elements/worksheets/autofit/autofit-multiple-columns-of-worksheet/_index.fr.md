---
title: "Ajuster automatiquement plusieurs colonnes sur une feuille Excel"
second_title: "Document"
linktitle: "Colonnes"
type: docs
url: /fr/worksheets/autofit/columns/
aliases: [  /fr/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, ajuster automatiquement les colonnes, API Excel, feuille de calcul cloud, REST"
description: "Découvrez comment ajuster automatiquement plusieurs colonnes sur une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint, les paramètres, un exemple cURL, la gestion des erreurs et des extraits de code SDK pour C#, Java, Python, et plus encore."
weight: 20
---

Cette API REST permet d’ajuster automatiquement **plusieurs colonnes** sur une feuille Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Paramètres de la requête**

| Nom du paramètre    | Type    | Emplacement | Description                                                                                                                                                      |
| ------------------- | ------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string  | path        | Le nom du fichier.                                                                                                                                               |
| sheetName           | string  | path        | Le nom de la feuille de calcul.                                                                                                                                  |
| firstColumn         | integer | query       | L’index de la colonne de départ.                                                                                                                                 |
| lastColumn          | integer | query       | L’index de la colonne de fin.                                                                                                                                    |
| autoFitterOptions\* | object  | body        | Options d’ajustement automatique (voir [Options de l’ajusteur automatique](/cells/auto-fitter-options/)). Inclut `AutoFitMergedCells`, `IgnoreHidden` et `OnlyAuto`. |
| firstRow            | integer | query       | L’index de la ligne de départ pour l’ajustement automatique (**facultatif**).                                                                                   |
| lastRow             | integer | query       | L’index de la ligne de fin pour l’ajustement automatique (**facultatif**).                                                                                      |
| folder              | string  | query       | Chemin du dossier dans le stockage (**facultatif**).                                                                                                             |
| storageName         | string  | query       | Nom du stockage (**facultatif**).                                                                                                                                |

\*Le nom du paramètre est affiché sous forme de lien vers la documentation associée.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
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

L’utilisation d’un SDK est la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

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

---