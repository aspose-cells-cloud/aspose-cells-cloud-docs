---
title: Ajouter une zone de cellules à la mise en forme conditionnelle
description: Ajouter une zone de cellules à une règle de mise en forme conditionnelle dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut le point de terminaison, les paramètres, les exemples cURL et SDK, le schéma de réponse et la gestion des erreurs.
keywords: Aspose.Cells, mise en forme conditionnelle, CellArea, API REST, Excel, SDK cloud
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Ajouter une zone de cellules à la mise en forme conditionnelle

**Résumé** – Ajoute une zone de cellules à une règle de mise en forme conditionnelle existante dans une feuille.

---

## Conditions préalables

1. **Compte Aspose.Cells Cloud** – Obtenez votre **App SID** et votre **App Key**.  
2. **Jeton JWT** – Générez un jeton JWT à l’aide de l’App SID/Key (voir le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Le fichier Excel cible doit déjà exister dans le stockage/dossier spécifié.

---

## Authentification

Tous les appels nécessitent une **authentification basée sur un jeton JWT**. Transmettez le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <jeton jwt>
```

---

## Requête HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Paramètres de chemin

| Nom          | Type   | Description                                     |
|--------------|--------|-------------------------------------------------|
| `name`       | string | Nom du fichier Excel (par exemple, `Book1.xlsx`). |
| `sheetName`  | string | Nom de la feuille contenant la règle (par exemple, `Sheet1`). |
| `index`      | entier | Index de la règle de mise en forme conditionnelle (indexation à partir de 0). |

### Paramètres de requête

| Nom            | Type   | Obligatoire | Description                                               |
|----------------|--------|-------------|-----------------------------------------------------------|
| `cellArea`     | string | **Oui**     | Plage de cellules à ajouter, en notation A1 (par exemple, `A1:C3`). |
| `folder`       | string | Non         | Chemin du dossier où le fichier est stocké.              |
| `storageName`  | string | Non         | Nom du service de stockage.                               |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

### Réponse attendue en cas de succès

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Schéma de réponse – `CellArea`**

| Propriété       | Type | Description                                    |
|-----------------|------|------------------------------------------------|
| `StartRow`      | int  | Index de la première ligne (indexation à partir de 0). |
| `StartColumn`   | int  | Index de la première colonne (indexation à partir de 0). |
| `EndRow`        | int  | Index de la dernière ligne (indexation à partir de 0). |
| `EndColumn`     | int  | Index de la dernière colonne (indexation à partir de 0). |

---

**Codes de statut HTTP**

| Code | Signification             | Description                                                  |
|------|---------------------------|--------------------------------------------------------------|
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                   |
---

## Exemples de SDK

Ci-dessous figurent de courts extraits pour les SDK les plus courants. Remplacez `YOUR_APP_SID` et `YOUR_APP_KEY` par vos identifiants, puis définissez le jeton JWT généré le cas échéant.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Notes et conseils

- **Format de CellArea** – Doit être une plage A1 valide (`A1`, `A1:C3`, `Sheet2!B2:D5`). Les formats non valides renvoient **400 Bad Request**.
- **Zones superposées** – L’ajout d’une plage chevauchant une zone existante de la même règle déclenche une erreur **409 Conflict**.
- **Indexation à partir de 0** – Les index de ligne et de colonne dans la réponse commencent à `0`. Convertissez-les en notation Excel (à partir de 1) si nécessaire.
- **Stockage** – Si vous omettez `folder` et `storageName`, l’API utilise le stockage par défaut ou le dossier racine.

---

## Opérations connexes

- **Supprimer une zone de cellules** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Ajouter une condition à la mise en forme conditionnelle** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Obtenir la mise en forme conditionnelle** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Ces opérations peuvent être combinées pour construire des workflows complets de mise en forme conditionnelle.

---
---