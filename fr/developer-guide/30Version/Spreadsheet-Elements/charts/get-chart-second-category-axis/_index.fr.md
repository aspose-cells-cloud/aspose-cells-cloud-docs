---
title: "Obtenir l’axe de deuxième catégorie d’un graphique"
type: docs
url: /fr/charts/second-category-axis/get/
weight: 60
keywords: "Obtenir l’axe de deuxième catégorie d’un graphique, API Aspose.Cells Cloud, axe de graphique Excel, API REST, axe de deuxième catégorie, Aspose.Cells"
description: "Récupérer l’axe de deuxième catégorie d’un graphique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le format de la requête, les paramètres, un exemple cURL, le schéma de réponse, les codes de statut et des notes d’utilisation."
ArticleTitle: "Obtenir l’axe de deuxième catégorie d’un graphique – Aspose.Cells Cloud API"
---

Cet API REST permet de récupérer **l’axe de deuxième catégorie** d’un graphique.

## API GetChartSecondCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement du paramètre (chemin/requête) | Description                                              |
| ---------------- | ------- | ------------------------------------------ | -------------------------------------------------------- |
| name             | string  | path                                       | Nom du fichier Excel stocké dans le cloud.              |
| sheetName        | string  | path                                       | Nom de la feuille de calcul contenant le graphique.     |
| chartIndex       | integer | path                                       | Index à base zéro du graphique dont l’axe est demandé.  |
| folder           | string  | query                                      | Chemin du dossier dans le stockage où le fichier est situé. |
| storageName      | string  | query                                      | Nom du stockage Aspose Cloud à utiliser (facultatif).   |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Axe de deuxième catégorie",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                      |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT invalide ou manquant.                                  |
| 413  | Payload Too Large           | Le fichier téléchargé dépasse la taille limite.                |
| 500  | Internal Server Error       | Erreur interne inattendue du serveur.                            |

## Comment utiliser l’API GetChartSecondCategoryAxis avec les SDK

### Spécification de l’API GetChartSecondCategoryAxis

L’opération **GetChartSecondCategoryAxis** est définie dans la [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) et permet des interactions REST directes depuis un navigateur web ou tout client HTTP.

Vous pouvez utiliser l’outil en ligne de commande `cURL` pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API avec `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Axe de deuxième catégorie",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour intégrer cette API dans votre projet. Les SDK gèrent les détails de bas niveau tels que l’authentification, la construction des requêtes et l’analyse des réponses, vous permettant de vous concentrer sur la logique métier. Consultez la liste complète des SDK Aspose.Cells Cloud dans le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment appeler l’opération **Get Chart Second Category Axis** à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configurer le client API
var config = new Configuration
{
    ClientId = "<votre-client-id>",
    ClientSecret = "<votre-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Construire la requête
var request = new GetChartSecondCategoryAxisRequest(
    name: "Échantillon.xlsx",
    sheetName: "Feuil1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Exécuter
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Nom de l’axe : {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // Configurer le client API
        Configuration config = new Configuration();
        config.setClientId("<votre-client-id>");
        config.setClientSecret("<votre-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Construire la requête
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Échantillon.xlsx", "Feuil1", 0, "Documents", null);

        // Exécuter
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Nom de l’axe : " + response.getAxis().getName());
    }
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
use Aspose\Cells\Cloud\Sdk\Api\ChartsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;
use Aspose\Cells\Cloud\Sdk\Model\Requests\GetChartSecondCategoryAxisRequest;

// Configurer
$config = new Configuration();
$config->setClientId('<votre-client-id>');
$config->setClientSecret('<votre-client-secret>');

$apiInstance = new ChartsApi($config);

$request = new GetChartSecondCategoryAxisRequest(
    'Échantillon.xlsx',  // name
    'Feuil1',            // sheetName
    0,                   // chartIndex
    'Documents',         // folder
    null                 // storageName
);

try {
    $result = $apiInstance->getChartSecondCategoryAxis($request);
    echo "Nom de l’axe : " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Exception lors de l’appel à ChartsApi->getChartSecondCategoryAxis : ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# Configurer le SDK
config = AsposeCellsCloud::Configuration.new
config.client_id = '<votre-client-id>'
config.client_secret = '<votre-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Échantillon.xlsx',
    sheet_name: 'Feuil1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Nom de l’axe : #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception lors de l’appel à ChartsApi->get_chart_second_category_axis : #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# Configurer le client API
config = asposecellscloud.Configuration()
config.client_id = '<votre-client-id>'
config.client_secret = '<votre-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Échantillon.xlsx',
    sheet_name='Feuil1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Nom de l’axe :', response.axis.name)
except ApiException as e:
    print('Exception lors de l’appel à ChartsApi->get_chart_second_category_axis :', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Exemple Node.js utilisant le SDK Aspose.Cells Cloud
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<votre-client-id>',
    clientSecret: '<votre-client-secret>'
});
const api = new ChartsApi(config);

(async () => {
    try {
        const response = await api.getChartSecondCategoryAxis({
            name: 'Échantillon.xlsx',
            sheetName: 'Feuil1',
            chartIndex: 0,
            folder: 'Documents'
        });
        console.log('Nom de l’axe :', response.axis.name);
    } catch (error) {
        console.error('Erreur :', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Exemple Android (Java) utilisant le SDK Aspose.Cells Cloud pour Android
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<votre-client-id>");
        config.setClientSecret("<votre-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Échantillon.xlsx", "Feuil1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Nom de l’axe : " + response.getAxis().getName());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(clientId: "<votre-client-id>", clientSecret: "<votre-client-secret>")
let api = ChartsApi(configuration: config)

let request = GetChartSecondCategoryAxisRequest(
    name: "Échantillon.xlsx",
    sheetName: "Feuil1",
    chartIndex: 0,
    folder: "Documents",
    storageName: nil
)

api.getChartSecondCategoryAxis(request: request) { result, error in
    if let axis = result?.axis {
        print("Nom de l’axe : \(axis.name ?? "")")
    } else if let err = error {
        print("Erreur : \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<votre-client-id>',
    client_secret => '<votre-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Échantillon.xlsx',
    sheet_name  => 'Feuil1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Nom de l’axe : " . $response->axis->name . "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "<votre-client-id>"
    cfg.ClientSecret = "<votre-client-secret>"

    apiInstance := api.NewChartsApi(cfg)

    request := asposecellscloud.GetChartSecondCategoryAxisRequest{
        Name:      "Échantillon.xlsx",
        SheetName: "Feuil1",
        ChartIndex: 0,
        Folder:    "Documents",
        StorageName: nil,
    }

    result, _, err := apiInstance.GetChartSecondCategoryAxis(request)
    if err != nil {
        fmt.Println("Erreur : ", err)
        return
    }
    fmt.Println("Nom de l’axe : ", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}
---