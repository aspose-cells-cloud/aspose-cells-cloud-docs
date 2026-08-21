---
title: "Supprimer une colonne d'une feuille de calcul Excel à l'aide de l'API Aspose.Cells Cloud"
description: "Découvrez comment supprimer une ou plusieurs colonnes d'une feuille de calcul Excel via l'API REST Aspose.Cells Cloud. Inclut l'authentification, la syntaxe des requêtes, les paramètres, les réponses, la gestion des erreurs et des exemples d'SDK."
keywords: ["Aspose.Cells", "Supprimer une colonne", "API Excel", "REST", "Cloud", "Feuille de calcul", "Colonnes"]
date: 2026-07-30
api_version: "v3.0"
---

# Supprimer une colonne d'une feuille de calcul Excel

**Endpoint** : `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

L’opération supprime une seule colonne ou une plage de colonnes d’une feuille de calcul. Les références de cellules (y compris les formules) peuvent être mises à jour automatiquement après la suppression.

---

## Table des matières
1. [Prérequis](#prerequisites)  
2. [Authentification](#authentication)  
3. [URL de la requête et méthode HTTP](#request-url--http-method)  
4. [Paramètres](#parameters)  
   - [Paramètres de chemin](#path-parameters)  
   - [Paramètres de requête](#query-parameters)  
5. [Exemple cURL](#curl-example)  
6. [Réponses](#responses)  
7. [Codes d’erreur](#error-codes)  
8. [Exemples d'SDK](#sdk-samples)  
9. [Notes supplémentaires](#additional-notes)  

---

## Prérequis
- Un **jeton d'accès JWT** valide obtenu via le flux d'authentification d'Aspose Cloud.  
- Le classeur (`{name}`) doit déjà être téléchargé dans le stockage Aspose Cloud (ou accessible via les paramètres de requête `folder`/`storageName`).  

---

## Authentification
Toutes les requêtes vers Aspose.Cells Cloud nécessitent une authentification par **jeton Bearer**.

```http
Authorization: Bearer <access_token>
```

Consultez le [guide d'authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) pour plus de détails sur l'obtention d'un jeton JWT.

---

## URL de la requête et méthode HTTP
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – nom du fichier de classeur (par exemple `test.xlsx`).  
- **`{sheetName}`** – nom de la feuille de calcul (par exemple `Sheet1`).  
- **`{columnIndex}`** – index de base zéro de la première colonne à supprimer.

---

## Paramètres

| Nom                  | Emplacement | Type    | Obligatoire | Description |
|----------------------|-------------|---------|-------------|-------------|
| **name**             | path        | string  | ✅ Oui      | Nom du fichier de classeur. |
| **sheetName**        | path        | string  | ✅ Oui      | Nom de la feuille de calcul. |
| **columnIndex**      | path        | integer | ✅ Oui      | Index de base zéro de la première colonne à supprimer. |
| **startColumn**      | query       | integer | ❌ Non      | Index de base zéro à partir duquel la suppression commence. Par défaut, égal à `columnIndex` si omis. |
| **totalColumns**     | query       | integer | ❌ Non      | Nombre de colonnes à supprimer. Si omis, seule la colonne identifiée par `columnIndex` est supprimée. |
| **updateReference**  | query       | boolean | ❌ Non      | Si `true`, met à jour les références de cellules (y compris les formules) dans tout le classeur après la suppression. |
| **folder**           | query       | string  | ❌ Non      | Chemin du dossier contenant le classeur. |
| **storageName**      | query       | string  | ❌ Non      | Nom du service de stockage Aspose Cloud. |

> **Remarque** – Le paramètre `columns`, mentionné dans la spécification de bas niveau de l'API, a été remplacé par les paramètres plus expressifs `startColumn` et `totalColumns`. Les deux approches sont acceptées pour des raisons de rétrocompatibilité.

---

## Exemple cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Explication
- Supprime la colonne **B** (`columnIndex = 1`) de `Sheet1` dans `test.xlsx`.  
- `startColumn=1` et `totalColumns=1` spécifient la suppression d’une seule colonne.  
- `updateReference=true` garantit que les formules et autres références sont automatiquement ajustées.

---

## Réponses

| Code HTTP | Description | Exemple |
|-----------|-------------|---------|
| **200** | Succès – la ou les colonnes ont été supprimées. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code": 400, "Message": "Valeur non valide pour totalColumns." }` |
| **401** | Non autorisé – jeton JWT manquant ou non valide. | `{ "Code": 401, "Message": "Échec de l'authentification." }` |
| **404** | Non trouvé – le classeur ou la feuille de calcul n'existe pas. | `{ "Code": 404, "Message": "Feuille de calcul 'Sheet1' introuvable." }` |
| **500** | Erreur interne du serveur – condition inattendue sur le serveur. | `{ "Code": 500, "Message": "Une erreur inattendue s'est produite." }` |

Le corps de la réponse suit le modèle générique **`CellsCloudResponse`**.

---

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Fichier téléchargé dépassant la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |
---

## Exemples d'SDK

Ci-dessous figurent des extraits prêts à l’emploi pour les SDK les plus populaires. Remplacez les valeurs génériques (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>`, etc.) par vos propres données.

| Langage | Exemple |
|---------|---------|
| **C#** | <details><summary>Afficher le code</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Afficher le code</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Afficher le code</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception lors de l’appel à CellsApi->delete_worksheet_columns :', e)\n```</details> |
| **Node.js** | <details><summary>Afficher le code</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status :', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Afficher le code</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Erreur :\", err)\n        return\n    }\n    fmt.Println(\"Statut :\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Afficher le code</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Statut : #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception : #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Afficher le code</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Statut : \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception lors de l’appel à CellsApi->deleteWorksheetColumns : ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Afficher le code</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Statut : \", $response->{Status}, \"\\n\";\n```</details> |

*Tous les SDK ajoutent automatiquement l’en-tête `Authorization` requis lorsque `access_token` est configuré.*

---

## Notes supplémentaires

### En-têtes de sécurité (recommandé pour la production)
Lors du rendu de la page de documentation, incluez les en-têtes HTTP de réponse suivants pour renforcer la sécurité :

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Conseils de performance
- Charger les scripts d’analyse tiers (`gtag.js`, `containerize.js`) avec l’attribut `async` ou les différer jusqu’à ce que la page soit rendue.  
- Minifier les bundles JavaScript/CSS personnalisés.  
- Précharger les petites icônes SVG s’ils bloquent le rendu :

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### Améliorations SEO (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Supprimer une colonne d'une feuille de calcul Excel à l'aide de l'API Aspose.Cells Cloud",
  "description": "Découvrez comment supprimer une ou plusieurs colonnes d'une feuille de calcul Excel via l'API REST Aspose.Cells Cloud.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Supprimer une colonne", "Excel", "API REST"]
}
```

Placer cet extrait dans une balise `<script type="application/ld+json">` dans l’en-tête HTML.

### Accessibilité
- Toutes les images décoratives utilisent `alt=""` ou sont masquées avec `aria-hidden="true"`.  
- L’image Open Graph inclut désormais un attribut `alt` dans la balise méta pour plus de complétude.

---

## Voir aussi
- [Spécification OpenAPI pour DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Vue d’ensemble de l’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDK Aspose.Cells Cloud sur GitHub](https://github.com/aspose-cells-cloud)  

---
---