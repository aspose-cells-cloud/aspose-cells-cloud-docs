---
title: Tri par plage
second title: "Document"
linktitle: "Tri"
type: docs
keywords: "Tri par plage, Aspose.Cells Cloud, API REST, Classeur, Excel, API"
url: /fr/ranges/sort/
description: Fournit une API permettant de trier une plage de cellules au sein d’un classeur à l’aide d’Aspose.Cells Cloud.
weight: 20
---

Cette API REST permet de trier une plage spécifique de cellules.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description                                      |
|------------------|--------|-------------|--------------------------------------------------|
| name             | String | Path        | Le nom du classeur.                              |
| sheetName        | String | Path        | Le nom de la feuille de calcul.                  |
| rangeOperate     | Class  | Body        | L'objet de requête de tri par plage.             |
| folder           | String | Query       | Le dossier contenant le classeur original.       |
| storageName      | String | Query       | Le nom du stockage.                              |

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web d’Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell
# (Exemple de réponse sera affiché ici)
```

{{< /tab >}}
{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le dépôt GitHub pour obtenir la liste complète des SDK d’Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web d’Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}