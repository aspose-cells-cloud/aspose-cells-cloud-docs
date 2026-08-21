---
title: "Mettre à jour un lien hypertexte dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
description: "Découvrez comment mettre à jour un lien hypertexte dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint, les paramètres, le schéma du corps de la requête, un exemple cURL, des extraits de code SDK, la gestion des erreurs, le limites de débit et les prérequis."
keywords:
  - "Aspose.Cells"
  - "mise à jour du lien hypertexte"
  - "API Excel"
  - "API REST"
  - "feuille de calcul cloud"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Mettre à jour un lien hypertexte dans une feuille de calcul Excel  

**Version de l’API :** v3.0  

L’opération **PostWorksheetHyperlink** met à jour un lien hypertexte existant dans une feuille de calcul identifiée par son index à base zéro.

---

## Table des matières
1. [Prérequis](#prerequisites)  
2. [Limites de débit](#rate-limiting)  
3. [Endpoint](#endpoint)  
4. [Paramètres](#parameters)  
   - [Paramètres de chemin](#path-parameters)  
   - [Paramètres de requête](#query-parameters)  
   - [Schéma du corps de la requête](#request-body-schema)  
5. [Réponses](#responses)  
   - [Réponse de succès](#success-response)  
   - [Réponses d’erreur](#error-responses)  
6. [Exemple cURL](#curl-example)  
7. [Extraits de code SDK](#sdk-code-samples)  
8. [Voir aussi](#see-also)  

---

## Prérequis <a name="prerequisites"></a>

| Exigence | Description |
|----------|-------------|
| **Authentification** | Authentification basée sur un jeton JWT. Obtenez un jeton comme décrit dans le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Stockage** | Le classeur doit être stocké dans un espace de stockage pris en charge par Aspose Cloud (par défaut : **Default**). |
| **Permissions** | Le jeton JWT doit disposer des autorisations de lecture et d’écriture sur le classeur cible. |
| **En-têtes** | `Content-Type: application/json` et `Accept: application/json` sont requis pour toutes les requêtes. |

---

## Limites de débit <a name="rate-limiting"></a>

Aspose.Cells Cloud impose une **limite maximale de 60 requêtes par minute et par jeton d’accès**. Dépasser cette limite renvoie une erreur HTTP **429 Too Many Requests**. Mettez en œuvre une remise en route exponentielle ou respectez l’en-tête `Retry-After` en cas de throttling.

---

## Endpoint <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Met à jour le lien hypertexte identifié par `hyperlinkIndex` dans la feuille de calcul `sheetName` du fichier `name`.*

---

## Paramètres <a name="parameters"></a>

### Paramètres de chemin <a name="path-parameters"></a>

| Nom             | Type   | Obligatoire | Description |
|-----------------|--------|-------------|-------------|
| `name`          | string | ✅ | Nom du fichier Excel (incluant l’extension). |
| `sheetName`     | string | ✅ | Nom de la feuille de calcul contenant le lien hypertexte. |
| `hyperlinkIndex`| integer| ✅ | Index à base zéro du lien hypertexte à mettre à jour. |

### Paramètres de requête <a name="query-parameters"></a>

| Nom            | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `folder`       | string | ❌ | Chemin du dossier dans lequel se trouve le classeur, dans l’espace de stockage. |
| `storageName`  | string | ❌ | Nom du service de stockage (par exemple, `Default`). |

### Schéma du corps de la requête <a name="request-body-schema"></a>

Le corps de la requête doit contenir un objet **`hyperlink`**. Seuls les champs que vous souhaitez modifier doivent être fournis ; les champs optionnels omis conservent leurs valeurs actuelles.

| Champ            | Type   | Obligatoire | Description |
|------------------|--------|-------------|-------------|
| `Address`        | string | ✅ | URL cible du lien hypertexte. |
| `Area`           | object | ✅ | Plage de cellules dans laquelle le lien hypertexte est placé. Doit contenir `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (tous des entiers, à base zéro). |
| `ScreenTip`      | string | ❌ | Info-bulle affichée au survol de la souris. |
| `TextToDisplay`  | string | ❌ | Texte affiché dans la cellule. |
| `link`           | object| ❌ | Liens hypertexte (`Href`, `Rel`, `Title`, `Type`). Généralement omis dans les charges utiles de requête. |

**Définition de l’objet `Area`**

| Sous-champ       | Type   | Obligatoire | Description |
|------------------|--------|-------------|-------------|
| `StartRow`       | integer| ✅ | Index de ligne de départ, à base zéro. |
| `StartColumn`    | integer| ✅ | Index de colonne de départ, à base zéro. |
| `EndRow`         | integer| ✅ | Index de ligne de fin, à base zéro. |
| `EndColumn`      | integer| ✅ | Index de colonne de fin, à base zéro. |

---

## Réponses <a name="responses"></a>

### Réponse de succès <a name="success-response"></a>

| Champ         | Type   | Description |
|---------------|--------|-------------|
| `Code`        | integer| Code d’état HTTP (200 en cas de succès). |
| `Status`      | string| État textuel (`OK`). |
| `Hyperlink`   | object (facultatif) | Objet lien hypertexte mis à jour, renvoyé uniquement si l’objet secondaire `link` est demandé. |

**Exemple JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Réponses d’erreur <a name="error-responses"></a>

| Code HTTP | Raison | Corps d’exemple |
|-----------|--------|-----------------|
| **400** | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Non autorisé – jeton JWT manquant ou non valide. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Non trouvé – le classeur, la feuille de calcul ou le lien hypertexte n’existe pas. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | Trop de requêtes – limite de débit dépassée. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Erreur interne du serveur – défaillance inattendue du serveur. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Exemple cURL <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Conseil :* Enregistrez la charge utile JSON dans un fichier (par exemple, `payload.json`) et référez-vous-y avec `--data @payload.json` pour un copier-coller plus propre.

---

## Extraits de code SDK <a name="sdk-code-samples"></a>

Les extraits suivants montrent comment appeler **PostWorksheetHyperlink** à l’aide des SDK officiels Aspose.Cells Cloud. Remplacez les valeurs génériques (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>`, etc.) par des données réelles.

| Langage | Exemple |
|---------|---------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Tous les SDK sont open source et peuvent être trouvés sur le [dépôt GitHub Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Voir aussi <a name="see-also"></a>

- **Authentification** – [Démarrage avec les jetons JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Opérations de stockage** – [Télécharger un fichier](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Autres opérations sur les liens hypertexte** – [Ajouter un lien hypertexte](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Supprimer un lien hypertexte](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **Spécification OpenAPI** – Définition complète de l’endpoint : <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Document mis à jour pour la dernière fois le : 2026‑07‑30*