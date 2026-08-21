---
title: "Dissocier les cellules dans une plage"
second_title: "Document"
linktype: "Dissocier"
type: docs
url: /fr/ranges/unmerge/
aliases: [  /fr/unmerge-merged-cells-of-the-range/ ]
keywords: "Aspose.Cells Cloud, dissocier les cellules, API Excel, plage de feuille de calcul, API REST"
description: "Découvrez comment utiliser l’API Aspose.Cells Cloud pour dissocier les cellules fusionnées dans une plage spécifique d’une feuille de calcul Excel. Inclut l’endpoint, les paramètres, des exemples cURL et des extraits de code SDK pour C#, Java, Python, et plus encore."
weight: 20
---

Cette API REST dissocie les cellules fusionnées dans une plage spécifiée d’une feuille de calcul Excel.

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                     |
|------------------|--------|-------------|-------------|-------------------------------------------------|
| name             | string | path        | Oui         | Nom du classeur.                                |
| sheetName        | string | path        | Oui         | Nom de la feuille de calcul.                    |
| range            | object | body        | Oui         | Objet plage définissant les cellules à dissocier. |
| folder           | string | query       | Non         | Dossier contenant le classeur.                  |
| storageName      | string | query       | Non         | Nom du stockage.                                |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
    "RowCount": 1,
    "RowHeight": 15,
    "Worksheet": "Sheet1"
}'
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

L’utilisation d’un SDK est la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}