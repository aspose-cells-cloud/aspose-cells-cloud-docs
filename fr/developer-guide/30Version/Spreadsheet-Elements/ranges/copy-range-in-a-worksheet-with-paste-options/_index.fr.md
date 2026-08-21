---
title: "Copier une plage dans une feuille de calcul avec des options de collage"
second_title: "Document"
linktype: "copier"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, API REST, Excel, copier une plage, feuille de calcul, options de collage"
description: "Utilisez l’API REST Aspose.Cells Cloud pour copier une plage au sein d’une feuille de calcul Excel avec prise en charge complète des options de collage. Inclut des exemples de SDK pour plusieurs langages de programmation."
weight: 20
ArticleTitle: "Copier une plage dans une feuille de calcul avec des options de collage – API Aspose.Cells Cloud"
---

Cette API REST copie une plage dans une feuille de calcul d’un classeur Excel. Pour les opérations connexes, consultez la documentation **Get Range** (Obtenir une plage) et **Update Range** (Mettre à jour une plage).

**Prérequis :** Pour utiliser ce point de terminaison, vous devez disposer d’un jeton OAuth 2.0 / JWT valide et vous assurer que votre version d’API correspond à l’URL de la requête.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                                 |
|------------------|--------|-------------|-----------------------------------------------------------------------------|
| name             | string | path        | Le nom du classeur.                                                        |
| sheetName        | string | path        | Le nom de la feuille de calcul.                                            |
| rangeOperate     | string | body        | L’opération à effectuer : `copydata`, `copystyle`, `copyto` ou `copyvalue`. |
| folder           | string | query       | Le dossier contenant le classeur.                                          |
| storageName      | string | query       | Le nom du service de stockage.                                             |

**Remarques :** Le champ `rangeOperate` détermine ce qui est copié. Utilisez `copydata` pour copier uniquement les valeurs des cellules, `copystyle` pour le formatage, `copyto` pour les données et le style, et `copyvalue` pour copier les valeurs sans les formules. L’API prend en charge des plages allant jusqu’à 1 million de cellules ; des plages plus grandes peuvent entraîner un délai d’attente dépassé.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
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

En cas de succès, la réponse renvoie un statut `200 OK`. En cas d’erreur, l’API peut renvoyer des charges utiles telles que :

```json
{
  "Code": 400,
  "Message": "Requête incorrecte – paramètres non valides."
}
```

ou

```json
{
  "Code": 401,
  "Message": "Non autorisé – jeton d’authentification manquant ou non valide."
}
```

Ces objets d’erreur incluent un code d’état HTTP et un message descriptif pour vous aider à diagnostiquer les problèmes.

{{< /tab >}}

{{< /tabs >}}

Vous pouvez télécharger un classeur d’exemple pour tester l’opération de copie [ici](https://example.com/sample.xlsx).

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}