---
title: "Aspose.Cells Cloud API – Mettre à jour l’axe des valeurs d’un graphique (POST /valueaxis)"
description: "Mettre à jour l’axe des valeurs d’un graphique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le point de terminaison, les paramètres, le schéma du corps de requête, des exemples (cURL et SDK), les réponses et la gestion des erreurs."
keywords:
  - Aspose.Cells Cloud
  - Mettre à jour l’axe des valeurs d’un graphique
  - API REST
  - Axe de graphique Excel
  - POST valueaxis
  - Exemple cURL
  - SDK
  - Payload JSON
  - Paramètres de l’axe du graphique
last_updated: 2026-07-30
---

# Mettre à jour l’axe des valeurs d’un graphique (POST /valueaxis)

**Résumé :**  
Modifiez l’axe des valeurs d’un graphique spécifique dans un classeur Excel stocké dans Aspose Cloud. Vous pouvez définir les limites, les unités des graduations, l’échelle logarithmique et d’autres propriétés de l’axe en une seule requête.

---

## Conditions préalables

1. **Jeton d’accès JWT** – Obtenez un jeton comme décrit dans le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. Le **classeur cible** doit déjà être uploadé dans le stockage Aspose Cloud (ou dans le stockage par défaut).  
3. Connaître le **nom de la feuille de calcul** et l’**index du graphique (à partir de zéro)** que vous souhaitez modifier.

---

## Point de terminaison

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Remplacez les espaces réservés par vos propres valeurs réelles.*

| Espace réservé | Description |
|----------------|-------------|
| `{name}` | Nom du fichier Excel (par exemple `Book1.xlsx`). |
| `{sheetName}` | Feuille de calcul contenant le graphique (par exemple `Sheet1`). |
| `{chartIndex}` | Index du graphique (à partir de zéro) (par exemple `0`). |

---

## Authentification

L’API utilise une **authentification basée sur un jeton JWT**. Incluez le jeton dans l’en-tête `Authorization` :

```
Authorization: Bearer <jeton JWT>
```

---

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## Paramètres de la requête

| Nom              | Emplacement | Type   | Obligatoire | Description |
|------------------|-------------|--------|-------------|-------------|
| **name**         | Chemin      | string | Oui         | Nom du fichier Excel stocké dans le cloud. |
| **sheetName**    | Chemin      | string | Oui         | Feuille de calcul contenant le graphique. |
| **chartIndex**   | Chemin      | int    | Oui         | Index (à partir de zéro) du graphique à mettre à jour. |
| **axis**         | Corps       | object | Oui         | Paramètres de l’axe (voir *Schéma du corps de requête*). |
| **folder**       | Requête     | string | Non         | Chemin du dossier cloud où réside le fichier. |
| **storageName**  | Requête     | string | Non         | Nom du service de stockage à utiliser. |

---

## Schéma du corps de requête (objet `axis`)

Seules les propriétés que vous souhaitez modifier doivent être présentes.

| Propriété        | Type     | Obligatoire | Description |
|------------------|----------|-------------|-------------|
| `minimum`        | nombre   | Non         | Limite inférieure de l’axe. |
| `maximum`        | nombre   | Non         | Limite supérieure de l’axe. |
| `majorUnit`      | nombre   | Non         | Intervalle entre les graduations majeures. |
| `minorUnit`      | nombre   | Non         | Intervalle entre les graduations mineures. |
| `logBase`        | nombre   | Non         | Base du logarithme lorsque `isLogarithmic` est `true`. |
| `isLogarithmic`  | booléen  | Non         | Indique si l’axe utilise une échelle logarithmique. |
| `displayUnit`    | chaîne   | Non         | Étiquette d’unité affichée sur l’axe (par exemple `"Thousands"`). |
| `tickMark`       | chaîne   | Non         | Style des graduations (`"inside"`, `"outside"`, etc.). |
| `crossAt`        | nombre   | Non         | Position où l’axe croise l’axe perpendiculaire. |

### Exemple de corps de requête

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## Exemples de requêtes

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### Exemples de SDK  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Exemple Node.js
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Exemple Android (Java)
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Réponses

### Succès (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Le type de réponse est `CellsCloudResponse`.

**Codes de statut HTTP**

| Code | Signification               | Description |
|------|-----------------------------|-------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Payload trop volumineux     | Le fichier uploadé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |
---

## Ressources supplémentaires

- **Spécification OpenAPI** – [Voir / télécharger JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **Dépôt SDK** – <https://github.com/aspose-cells-cloud>  
- **Guide d’authentification** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Pour toute question ou retour, veuillez contacter l’équipe de support Aspose.Cells Cloud.*