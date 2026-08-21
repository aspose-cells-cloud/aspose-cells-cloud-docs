---
title: "Ajuster automatiquement une ligne dans une feuille Excel"
second_title: "Document"
linktitle: "Ligne"
type: docs
url: /worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
description: "Découvrez comment utiliser l'API REST Aspose.Cells Cloud pour ajuster automatiquement une ligne dans une feuille Excel. Inclut l'endpoint, les paramètres, l'authentification, la gestion des erreurs, la requête cURL et des exemples d'SDK."
keywords: "ajuster automatiquement une ligne, Aspose.Cells Cloud, API Excel, REST, feuille de calcul, SDK, feuille de calcul, API cloud"
weight: 30
ArticleTitle: "Ajuster automatiquement une ligne dans une feuille Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cet API REST **ajuste automatiquement une ligne** dans une feuille Excel.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Paramètres de la requête**

| Nom du paramètre  | Type    | Emplacement | Description                                                                                                                                                                                                      |
| ----------------- | ------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name              | string  | path        | Nom du fichier Excel.                                                                                                                                                                                            |
| sheetName         | string  | path        | Nom de la feuille de calcul.                                                                                                                                                                                     |
| rowIndex          | integer | query       | Index de ligne (à partir de zéro) à ajuster automatiquement.                                                                                                                                                     |
| firstColumn       | integer | query       | Index de la première colonne incluse dans l’opération.                                                                                                                                                           |
| lastColumn        | integer | query       | Index de la dernière colonne incluse dans l’opération.                                                                                                                                                           |
| autoFitterOptions | object  | body        | Objet permettant de contrôler le comportement de l’ajustement automatique (par exemple, prise en compte des cellules fusionnées, texte automatique, etc.). Voir [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Contrôle du comportement d’ajustement automatique"}. |
| folder            | string  | query       | Dossier dans lequel le fichier est stocké.                                                                                                                                                                       |
| storageName       | string  | query       | Nom du stockage.                                                                                                                                                                                                 |

**Exemple de corps JSON pour `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Définitions des entités

| Entité              | Description                                                                                   |
| ------------------- | --------------------------------------------------------------------------------------------- |
| `rowIndex`          | Index de la ligne cible (à partir de zéro).                                                  |
| `firstColumn`       | Colonne de départ pour l’opération d’ajustement automatique.                                 |
| `lastColumn`        | Colonne de fin pour l’opération d’ajustement automatique.                                    |
| `autoFitterOptions` | Paramètres facultatifs influençant la façon dont la ligne est ajustée automatiquement (cellules fusionnées, texte automatique, etc.). |

La [spécification OpenAPI](/cells/#/Worksheets/PostAutofitWorksheetRow) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande `cURL` pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API avec `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Champ  | Description                                          |
| ------ | ---------------------------------------------------- |
| Code   | `200` – la requête a réussi.                         |
| Status | `"OK"` – la ligne a été ajustée automatiquement.     |

{{< /tab >}}

{{< /tabs >}}

## Gestion des erreurs

L’API renvoie des codes d’état HTTP standard. Les réponses d’erreur courantes pour cet endpoint sont :

| Code HTTP | Exemple de charge utile                              | Signification                                                                              |
| --------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 400       | `{ "Code": 400, "Message": "Index de ligne hors limites." }`   | L’`rowIndex` fourni n’existe pas dans la feuille de calcul.                               |
| 401       | `{ "Code": 401, "Message": "Jeton invalide ou expiré." }`     | Échec de l’authentification – vérifiez le jeton JWT et assurez-vous que la requête utilise HTTPS. |
| 404       | `{ "Code": 404, "Message": "Fichier introuvable." }`          | Le fichier Excel ou la feuille de calcul spécifié ne peut être trouvé.                   |
| 500       | `{ "Code": 500, "Message": "Erreur interne du serveur." }`    | Un problème inattendu est survenu côté serveur.                                           |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Voir aussi :** [Ajuster automatiquement une colonne](/worksheets/autofit/column/), [Ajuster automatiquement plusieurs lignes](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).