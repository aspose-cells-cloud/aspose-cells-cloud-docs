---
title: "Définir une formule de cellule dans des feuilles de calcul Excel"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, API REST, Définir une formule, Feuille de calcul, Cellule, SDK Cloud, cURL"
description: "Découvrez comment définir une formule pour une cellule spécifique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut un exemple cURL, une liste complète des paramètres, la gestion des erreurs et des exemples de code SDK."
---

Cette API REST définit une **formule de cellule** dans un fichier Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                      |
|------------------|--------|-------------|-------------|--------------------------------------------------|
| name             | string | path        | Oui         | Nom du document Excel.                           |
| sheetName        | string | path        | Oui         | Nom de la feuille de calcul.                     |
| cellName         | string | path        | Oui         | Adresse de la cellule cible (par exemple, **A1**). |
| value            | string | query       | Non         | Valeur à affecter à la cellule.                  |
| type             | string | query       | Non         | Type de données de la valeur (par exemple, **string**). |
| formula          | string | query       | Non         | Formule à appliquer à la cellule (par exemple, **sum(A1,A2)**). |
| folder           | string | query       | Non         | Dossier contenant le document.                   |
| storageName      | string | query       | Non         | Nom du service de stockage.                      |

## **Réponse**

Retourne un objet CellResponse.

- **Aperçu des champs de réponse**

| Champ             | Type    | Description                                                   |
| ----------------- | ------- | ------------------------------------------------------------- |
| `Name`            | string  | Adresse de la cellule (par exemple, `F341`).                  |
| `Row`             | integer | Index de ligne (base zéro).                                   |
| `Column`          | integer | Index de colonne (base zéro).                                 |
| `Value`           | string  | Valeur affichée de la cellule.                                |
| `Type`            | string  | Type de données de la cellule (par exemple, `IsString`).      |
| `Formula`         | string  | Texte de la formule si la cellule en contient une.            |
| `IsFormula`       | bool    | Indique si la cellule contient une formule.                   |
| `IsMerged`        | bool    | Indique si la cellule fait partie d'une plage fusionnée.      |
| `IsArrayHeader`   | bool    | Indique si la cellule est une en‑tête de tableau.             |
| `IsInArray`       | bool    | Indique si la cellule appartient à un tableau.                |
| `IsErrorValue`    | bool    | Indique si la cellule contient une valeur d’erreur.           |
| `IsInTable`       | bool    | Indique si la cellule se trouve dans un tableau.              |
| `IsStyleSet`      | bool    | Indique si un style est appliqué à la cellule.                |
| `HtmlString`      | string  | Représentation HTML‑encodée de la valeur de la cellule.       |
| `Style.link`      | object  | Lien hypertexte vers la ressource de style.                   |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                   |

## Comment utiliser l'API PostWorksheetCellSetValue avec les SDK

### Spécification de l'API PostWorksheetCellSetValue

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) définit une interface de programmation accessible publiquement et permet d'effectuer des interactions REST directement depuis un navigateur web.

Utilisez l'outil en ligne de commande cURL pour appeler les services web Aspose.Cells.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Exemple en C# – définir une formule pour une cellule
// Remplacez <access-token>, <file-name>, etc. par vos propres valeurs.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Exemple en Java – définir une formule pour une cellule
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Exemple en PHP – définir une formule pour une cellule
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Exemple en Ruby – définir une formule pour une cellule
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Exemple en Python – définir une formule pour une cellule
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Exemple en Node.js – définir une formule pour une cellule
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Exemple Android (Java) – définir une formule pour une cellule
// Similaire à l'exemple Java standard ; assurez-vous d'utiliser le SDK compatible Android.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Exemple Swift non disponible**. Le SDK Swift est actuellement en cours de développement.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Exemple en Perl – définir une formule pour une cellule
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Exemple en Go – définir une formule pour une cellule
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}