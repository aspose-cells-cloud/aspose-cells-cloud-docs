---
---
title: "Obtenir AutoFilter"
description: "Récupérer la description AutoFilter à partir d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Récupérer la description AutoFilter à partir d'une feuille de calcul

**Version :** v3.0  
**Point de terminaison :** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Remarque :** Toutes les demandes d’exemple utilisent **HTTPS**. N’envoyez jamais de jetons JWT sur une connexion non sécurisée.

---

## Vue d’ensemble

Un **AutoFilter** permet aux utilisateurs de filtrer des lignes dans une feuille de calcul en fonction des valeurs des colonnes, des couleurs, de critères personnalisés, etc. Cette API renvoie la configuration complète de l’AutoFilter — y compris les colonnes filtrées, la plage et les détails de tri — afin que vous puissiez inspecter ou reproduire les paramètres de filtre par programmation.

---

## Conditions préalables

| Exigence | Description |
|----------|-------------|
| **Authentification** | Un jeton JWT valide est requis. Voir le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Emplacement du fichier** | Le classeur doit être stocké dans le stockage Aspose Cloud (ou dans un stockage externe connecté). |
| **Formats pris en charge** | Tout format Excel pris en charge par Aspose.Cells (par ex., `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (facultatif)** | Si vous préférez utiliser un SDK, installez le paquet approprié (par ex., `dotnet add package Aspose.Cells-Cloud` pour .NET). |

---

## Demande

### Demande HTTP

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Paramètres de chemin

| Paramètre | Type   | Description |
|-----------|--------|-------------|
| `name`      | string | **Obligatoire.** Nom du fichier de classeur, incluant l’extension. |
| `sheetName` | string | **Obligatoire.** Nom de la feuille de calcul à partir de laquelle récupérer l’AutoFilter. |

### Paramètres de requête

| Paramètre     | Type   | Description |
|---------------|--------|-------------|
| `folder`      | string | Chemin du dossier dans le stockage où se trouve le classeur. |
| `storageName` | string | Nom du stockage à utiliser. |

### Sécurité

L’API utilise **l’authentification basée sur un jeton JWT**. Incluez le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <votre_jeton_jwt>
```

---

## Exemple de demande (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton_jwt>"
```

---

## Réponse

Le service renvoie un objet JSON qui encapsule le modèle `AutoFilter`.

### Schéma de réponse réussie

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### Exemple de réponse

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**Codes de statut HTTP**

| Code | Signification                  | Description |
|------|--------------------------------|-------------|
| 200  | OK                             | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte             | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                   | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande        | Le fichier chargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur       | Erreur inattendue du serveur. |
---

## Exemples de SDK

L’opération est disponible dans tous les SDK Aspose.Cells Cloud. Ci-dessous figurent des extraits prêts à l’emploi.

| Langage | Exemple |
|---------|---------|
| **C#** | <details><summary>Afficher le code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Afficher le code</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Afficher le code</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Afficher le code</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Afficher le code</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Afficher le code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Afficher le code</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Afficher le code</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

Pour une liste complète des SDK et des instructions d’installation, rendez-vous sur le [dépôt GitHub Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).

---

## Voir aussi

- [AutoFilter – Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Opérations sur le stockage](https://docs.aspose.cloud/cells/storage/)  

---
---