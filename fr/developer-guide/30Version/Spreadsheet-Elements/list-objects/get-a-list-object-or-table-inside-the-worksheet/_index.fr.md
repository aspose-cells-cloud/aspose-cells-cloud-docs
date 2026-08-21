---
title: "Aspose.Cells Cloud API – Obtenir un objet liste (tableau) à partir d'une feuille de calcul"
description: "Récupérer un objet liste (tableau) à partir d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Prise en charge de l'export vers plusieurs formats (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - API Cloud
  - Excel
  - ListObject
  - Tableau
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Obtenir un objet liste (tableau) à partir d'une feuille de calcul

Récupérez un **objet liste** (également appelé *tableau*) à partir d'une feuille de calcul spécifique dans un classeur Excel. Le point de terminaison permet également d'exporter directement le tableau dans un format choisi à l'aide du paramètre de requête facultatif `format`.

---

## Conditions préalables

| Exigence | Détails |
|----------|---------|
| **Authentification** | Un token **JWT** (Bearer) valide est requis. Obtenez le token via le flux d’authentification **OAuth2** décrit dans le [guide d’authentification](/authentication/). |
| **Stockage** | Le classeur doit être stocké dans un emplacement de stockage Aspose Cloud. Si le fichier réside dans un stockage non par défaut, spécifiez le paramètre de requête `storageName`. |
| **Limites de débit** | L’API suit la politique standard de limites de débit Aspose Cloud (par défaut = 100 demandes/minute par compte). |
| **SDK (facultatif)** | L’utilisation d’un des SDK officiels (C#, Java, Python, …) simplifie la construction des demandes et la gestion des réponses. Voir la section **Exemples de SDK** ci-dessous. |

---

## Demande

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Paramètre | Type | Emplacement | Obligatoire | Description |
|-----------|------|-------------|-------------|-------------|
| **name** | `string` | Chemin | ✔️ | Nom du fichier Excel (incluant l’extension). |
| **sheetName** | `string` | Chemin | ✔️ | Feuille de calcul contenant l’objet liste. |
| **listobjectindex** | `integer` | Chemin | ✔️ | Index de base zéro de l’objet liste à récupérer. |
| **format** | `string` | Requête | ❌ | Format d’export souhaité (par ex. `pdf`, `csv`, `json`). |
| **folder** | `string` | Requête | ❌ | Chemin du dossier où le classeur est stocké. |
| **storageName** | `string` | Requête | ❌ | Nom du stockage Aspose Cloud à utiliser. |

#### Notes

* Tous les appels **doivent** être effectués via HTTPS.  
* Lorsque le paramètre `format` est fourni, le corps de la réponse est le flux binaire du fichier exporté (par ex. `application/pdf`).  
* Sans `format`, l’API renvoie une description JSON de l’objet liste.

---

## Exemple cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Remplacez `<your_jwt_token>` par un JWT valide obtenu via le point de terminaison d’authentification.*

---

## Réponse réussie (JSON)

Lorsque **`format` est omis**, l’API renvoie une charge utile JSON décrivant l’objet liste.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

Lorsque **`format` est fourni**, le corps de la réponse est un flux binaire du type de fichier demandé (par ex. `Content-Type: text/csv`).

---

## Gestion des erreurs

| Code HTTP | Signification | Exemple JSON |
|-----------|---------------|--------------|
| **400** | Requête incorrecte – paramètres manquants ou non valides. | `{"Code":400,"Message":"Paramètre de format non valide."}` |
| **401** | Non autorisé – token JWT manquant ou non valide. | `{"Code":401,"Message":"Échec de l’authentification."}` |
| **404** | Non trouvé – le classeur, la feuille de calcul ou l’objet liste n’existe pas. | `{"Code":404,"Message":"ListObject introuvable."}` |
| **500** | Erreur interne du serveur. | `{"Code":500,"Message":"Erreur inattendue du serveur."}` |

### Pièges courants (notes)

* **Index de base zéro** – `listobjectindex` commence à **0**. Une requête avec l’index `1` renverra le deuxième tableau de la feuille.  
* **Dossier et stockage** – Si le classeur est stocké dans un sous-dossier, incluez le paramètre de requête `folder` (par ex. `?folder=Rapports/2024`).  
* **Format d’export** – Seuls les formats pris en charge par le moteur de conversion Aspose.Cells sont autorisés (`pdf`, `xlsx`, `csv`, `json`, …). Fournir une valeur non prise en charge entraîne une erreur **400**.

---

## Exemples de SDK

Les extraits ci-dessous illustrent comment appeler le point de terminaison à l’aide des SDK officiels Aspose.Cells Cloud. Remplacez les valeurs génériques (`<YOUR_CLIENT>`, `<YOUR_JWT>`, etc.) par vos propres configurations.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initialiser le client API
var apiInstance = new ListObjectsApi();

// Construire la requête
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // ex. "csv" pour l'export
    folder: null,
    storageName: null
);

// Exécuter
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## Voir aussi

| Point de terminaison connexe | Description |
|------------------------------|-------------|
| **Ajouter un objet liste** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – créer un nouveau tableau. |
| **Mettre à jour un objet liste** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – modifier les propriétés du tableau. |
| **Supprimer un objet liste** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – supprimer un tableau. |
| **Lister tous les objets liste** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – énumérer les tableaux dans une feuille de calcul. |

---

## Références

* **Spécification OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Guide d’authentification** – <https://docs.aspose.cloud/cells/authentication/>  
* **Dépôt GitHub (SDK)** – <https://github.com/aspose-cells-cloud>  

---