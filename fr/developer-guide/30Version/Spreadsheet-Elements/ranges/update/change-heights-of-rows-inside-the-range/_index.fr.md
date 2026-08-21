---
title: "Définir la hauteur de ligne pour une plage dans Excel – Aspose.Cells Cloud API (v3.0)"
description: "Modifiez la hauteur des lignes dans une plage spécifique d'une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL de l’endpoint, les paramètres, un exemple cURL, des réponses d’exemple et des extraits de code SDK pour plusieurs langages."
keywords: "Aspose.Cells, hauteur de ligne, plage, Excel, API REST, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Définir la hauteur de ligne pour une plage dans Excel

Cette opération met à jour la hauteur de ligne d’une plage spécifiée sur une feuille de calcul stockée dans le stockage Aspose Cloud.

## Conditions préalables / Authentification

Vous devez obtenir un token d'accès JWT à partir du service OAuth Aspose Cloud avec la portée **Cells.ReadWrite**.

Incluez le token dans l’en-tête `Authorization` de chaque requête :

```http
Authorization: Bearer <jeton jwt>
```

Si vous ne disposez pas encore de token, suivez le **guide d’authentification Aspose Cloud** pour en demander un.

## Requête HTTP

| Méthode | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Paramètres de chemin

| Nom | Type | Description |
|------|------|-------------|
| `name` | `string` | **Obligatoire.** Le nom du fichier Excel stocké dans le cloud. |
| `sheetName` | `string` | **Obligatoire.** La feuille de calcul contenant la plage cible. |

### Paramètres de requête

| Nom | Type | Obligatoire | Description |
|------|------|-------------|-------------|
| `value` | `number` | **Oui** | Hauteur de ligne souhaitée (en points) à appliquer à la plage. |
| `folder` | `string` | Non | Chemin du dossier dans le stockage où se trouve le fichier. |
| `storageName` | `string` | Non | Nom du service de stockage (si plusieurs stockages sont configurés). |

### Corps de la requête (JSON)

Le corps doit contenir un objet **Range** qui définit quelles lignes sont concernées.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Schéma JSON pour Range

| Propriété | Type | Obligatoire | Description |
|-----------|------|-------------|-------------|
| `FirstRow` | entier | **Oui** | Index de base zéro de la première ligne dans la plage. |
| `RowCount` | entier | **Oui** | Nombre de lignes auxquelles la hauteur sera appliquée. |
| `FirstColumn` | entier | Non | Index de base zéro de la première colonne (facultatif pour l’opération de hauteur de ligne uniquement). |
| `ColumnCount` | entier | Non | Nombre de colonnes couvertes par la plage (facultatif). |

Seules les propriétés répertoriées ci-dessus sont utilisées pour l’opération de hauteur de ligne ; tous les champs supplémentaires sont ignorés.

## Exemple de requête

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Réponse d’exemple (succès)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Token JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

Toutes les réponses contiennent un `Code` numérique et un `Status` lisible par un humain (ou `Message` en cas d’erreur). Des détails supplémentaires peuvent être fournis dans `ErrorDetails` en cas d’erreur.

## Exemples SDK

Les extraits suivants montrent comment appeler **Set Row Height for a Range** à l’aide des SDK officiels Aspose.Cells Cloud.

| Langage | Exemple |
|---------|---------|
| **C#** | <details><summary>Afficher le code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Afficher le code</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Afficher le code</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jeton jwt>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Afficher le code</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jeton jwt>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Hauteur de ligne définie'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Afficher le code</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jeton jwt>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Afficher le code</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jeton jwt>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Afficher le code</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jeton jwt>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Afficher le code</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jeton jwt>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Remarque :** Tous les SDK ajoutent automatiquement l’en-tête `Authorization: Bearer` requis lorsque le jeton d’accès est configuré.

## Voir aussi

- **Spécification OpenAPI** – Contrat détaillé pour cette opération : <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Dépôt GitHub des SDK Aspose.Cells Cloud** – Code source et liaisons supplémentaires pour d’autres langages : <https://github.com/aspose-cells-cloud>
- **Guide d’authentification** – Comment obtenir un token JWT : <https://docs.aspose.cloud/cells/authentication/>

---