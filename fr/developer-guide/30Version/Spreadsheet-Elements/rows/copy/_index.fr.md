---
title: "Copier des lignes sur une feuille Excel"
description: "Copier les données et les formats à partir de lignes entières spécifiques dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’authentification, les détails des requêtes/réponses, la gestion des erreurs et des exemples d’SDK."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Copier des lignes sur une feuille Excel <span style="float:right;">v3.0</span>

Copier les données et les formats à partir de lignes entières spécifiques d'une feuille de calcul.

---

## Conditions préalables

| # | Exigence |
|---|----------|
| 1 | Un jeton **JWT** valide. Voir le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | Le classeur (`{name}`) doit déjà exister dans le **dossier** / **stockage** sélectionné. |
| 3 | La feuille cible (`{sheetName}`) doit être présente dans le classeur. |
| 4 | (Facultatif) Connaître le **dossier** et le **storageName** si le fichier n’est pas situé à l’emplacement par défaut. |

---

## Point de terminaison

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Tous les paramètres de chemin sont sensibles à la casse.*

### Paramètres de chemin

| Paramètre | Type   | Obligatoire | Description |
|-----------|--------|-------------|-------------|
| `name`    | string | ✅ | Nom du fichier de classeur (par exemple, `test.xlsx`). |
| `sheetName` | string | ✅ | Nom de la feuille de calcul (par exemple, `Sheet1`). |

### Paramètres de requête

| Paramètre            | Type    | Obligatoire | Description |
|----------------------|---------|-------------|-------------|
| `sourceRowIndex`     | integer | ✅ | Index de base zéro de la ligne source. |
| `destinationRowIndex`| integer | ✅ | Index de base zéro où les lignes seront placées. |
| `rowNumber`          | integer | ✅ | Nombre de lignes à copier. |
| `worksheet`          | string  | ❌ | Identifiant de la feuille de calcul ; généralement identique à **sheetName**. |
| `folder`             | string  | ❌ | Chemin vers le dossier contenant le classeur. |
| `storageName`        | string  | ❌ | Nom du service de stockage. |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

> **Remarque**  
> Remplacer `<jeton jwt>` par un jeton JWT valide obtenu auprès du service d’authentification.

---

## Réponse réussie

| Code | Description |
|------|-------------|
| **200** | Lignes copiées avec succès. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Le corps de la réponse est une instance de `CellsCloudResponse`.

---

## Gestion des erreurs

| Code HTTP | Signification                              | Corps d’exemple |
|-----------|--------------------------------------------|-----------------|
| **400**   | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code": 400, "Message": "sourceRowIndex non valide." }` |
| **401**   | Non autorisé – jeton JWT invalide ou manquant. | `{ "Code": 401, "Message": "Échec de l’authentification." }` |
| **404**   | Introuvable – le classeur ou la feuille de calcul n’existe pas. | `{ "Code": 404, "Message": "Fichier introuvable." }` |
| **500**   | Erreur interne du serveur – condition inattendue du serveur. | `{ "Code": 500, "Message": "Une erreur inattendue s’est produite." }` |

**Directives de gestion**

* **400** – Vérifier que tous les paramètres de requête obligatoires sont présents et correctement formatés.  
* **401** – Régénérer ou actualiser le jeton JWT.  
* **404** – Confirmer les noms du classeur et de la feuille de calcul, et vérifier que le fichier existe dans le dossier/le stockage spécifié.  
* **500** – Réessayer après un court délai ; si le problème persiste, contacter le support Aspose.

---

## Exemples de SDK

Les extraits suivants montrent comment appeler l’opération **Copier des lignes** à l’aide des SDK officiels Aspose.Cells Cloud.

| Langage | Exemple |
|---------|---------|
| **C#**   | <details><summary>Afficher le code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Afficher le code</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Afficher le code</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Afficher le code</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Afficher le code</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Afficher le code</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Afficher le code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Afficher le code</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Les fichiers sources complets sont disponibles sur le [dépôt GitHub Aspose‑Cells‑Cloud](https://github.com/aspose-cells-cloud).*

---

## Voir aussi

- [Ajouter une ligne sur une feuille Excel](/rows/add/)  
- [Supprimer une ligne sur une feuille Excel](/rows/delete/)  
- [Mettre à jour une ligne sur une feuille Excel](/rows/update/)  

--- 

*Page générée le **{{DATE}}**. Pour la version la plus récente de cette API, voir la [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*