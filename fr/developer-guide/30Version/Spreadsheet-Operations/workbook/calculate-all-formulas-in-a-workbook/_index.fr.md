---
title: "Calculer toutes les formules d’un classeur Excel"
second_title: "Document"
linktitle: "Calculer"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, calculer les formules, API Excel, SDK cloud"
description: "Calculez toutes les formules d’un classeur Excel via l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, les paramètres de requête, le schéma de réponse, les prérequis et des extraits de code SDK pour plusieurs langages."
weight: 140
ArticleTitle: "Calculer toutes les formules d’un classeur Excel"
---

Cet API REST calcule **toutes les formules** d’un classeur Excel.

**Prérequis :** Avant d’appeler ce point de terminaison, assurez-vous d’avoir :
- Un jeton d’authentification JWT valide. (Voir le [Guide d’authentification](/authentication/).)  
- Votre identifiant client et votre secret Aspose.Cells Cloud.  
- Le classeur cible uploadé vers l’emplacement de stockage désigné. (Voir la [Configuration du stockage](/storage/).)

## API PostWorkbookCalculateFormula

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

Les paramètres de la requête sont listés ci-dessous :

| Nom du paramètre | Type               | Emplacement | Description                                                                                     |
| ------------------ | ------------------ | ----------- | ----------------------------------------------------------------------------------------------- |
| **name**           | string             | path        | Nom du fichier du classeur.                                                                     |
| **options**        | CalculationOptions | body        | Objet JSON spécifiant les paramètres de calcul (par ex. `CalcStackSize`, `IgnoreError`).       |
| **ignoreError**    | boolean            | query       | Si `true`, les erreurs rencontrées pendant le calcul sont ignorées.                            |
| **folder**         | string             | query       | Chemin du dossier contenant le classeur.                                                        |
| **storageName**    | string             | query       | Nom du service de stockage où le classeur est stocké.                                          |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Détails de la réponse

| Champ              | Type   | Description                                                           |
| ------------------ | ------ | --------------------------------------------------------------------- |
| **Code**           | int    | Code d’état similaire à HTTP (200 indique le succès).                |
| **Status**         | string | Brève description textuelle du résultat (par ex. `OK`).               |
| **WorkbookUrl**    | string | URL directe permettant de télécharger le classeur mis à jour.        |
| **ErrorMessage**   | string | Informations détaillées sur l’erreur en cas d’échec de la requête ; `null` en cas de succès. |

#### Prochaines étapes / Erreurs courantes

- **Gérer les erreurs de calcul** – définissez `ignoreError=false` pour recevoir une réponse d’erreur lorsqu’une formule ne peut pas être évaluée.
- **Respecter les limites de débit** – vérifiez l’en‑tête `X-RateLimit-Remaining` ; s’il atteint `0`, attendez avant de réessayer.
- **Guidage des codes d’état HTTP** :
  - `400` – Paramètres de requête invalides.
  - `401` – Échec d’authentification (jeton JWT invalide ou expiré).
  - `404` – Classeur introuvable.
  - `500` – Erreur côté serveur ; contactez le support Aspose si elle persiste.

| Code | Signification         | Quand il est renvoyé                                      |
|------|-----------------------|-----------------------------------------------------------|
| 400  | Mauvaise requête      | Paramètres de requête invalides ou JSON mal formé.       |
| 401  | Non autorisé          | Jeton JWT manquant, invalide ou expiré.                  |
| 404  | Introuvable           | Le classeur spécifié n’existe pas dans le stockage.      |
| 500  | Erreur interne serveur| Échec inattendu côté serveur ; contactez le support Aspose. |

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}