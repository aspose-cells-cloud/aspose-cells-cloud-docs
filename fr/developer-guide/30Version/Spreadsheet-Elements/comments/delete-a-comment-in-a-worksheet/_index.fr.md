---
title: "API de suppression de commentaire de feuille de calcul – Aspose.Cells Cloud"
description: "Supprimez un commentaire cellulaire spécifique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint, les paramètres, des exemples de requête/réponse, des extraits de code SDK et la gestion des erreurs."
keywords: "Aspose.Cells, supprimer le commentaire, API Excel, REST, commentaire de feuille de calcul"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API de suppression de commentaire de feuille de calcul – Aspose.Cells Cloud

> **Dernière mise à jour de la page :** 30 juillet 2026  

## Vue d’ensemble
Un **commentaire** est une note textuelle attachée à une cellule spécifique dans une feuille de calcul Excel.  
L’opération **Supprimer le commentaire de feuille de calcul** supprime un commentaire à partir de la cellule spécifiée.

![Aspose.Cells Cloud – Illustration de la suppression de commentaire de feuille de calcul](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API de suppression de commentaire de feuille de calcul")

## Authentification
Tous les endpoints d’Aspose.Cells Cloud exigent une **authentification basée sur un jeton JWT**.  
Incluez le jeton dans l’en-tête `Authorization` :

```
Authorization: Bearer <jeton jwt>
```

Pour plus de détails sur l’obtention d’un jeton JWT, consultez le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Conditions préalables
- Un jeton d’accès JWT valide.  
- Le classeur cible (`{name}`) doit exister à l’emplacement de stockage spécifié.  
- Facultatif : l’un des SDK Aspose.Cells Cloud installés pour votre langage préféré.

## Requête HTTP

### Endpoint
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Paramètres de chemin
| Paramètre   | Type   | Obligatoire | Description |
|-------------|--------|-------------|-------------|
| `name`      | string | ✅ | Le nom du classeur Excel (par exemple, `test.xlsx`). |
| `sheetName` | string | ✅ | Le nom de la feuille de calcul contenant le commentaire. |
| `cellName`  | string | ✅ | L’adresse de la cellule dont le commentaire sera supprimé (par exemple, `A1`). |

### Paramètres de requête
| Paramètre     | Type   | Obligatoire | Description |
|---------------|--------|-------------|-------------|
| `folder`      | string | ❌ | Le chemin du dossier où le classeur est stocké. Si omis, le dossier racine est utilisé. |
| `storageName` | string | ❌ | Le nom du service de stockage (par exemple, `MyCloud`). Si omis, le stockage par défaut est utilisé. |

## Exemple de requête

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

## Réponse

### Succès (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description |
|------|-----------------------------|-------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur     | Erreur inattendue du serveur. |

### Réponses d’erreur

| Code HTTP | Description | Exemple |
|-----------|-------------|---------|
| 400 | Requête incorrecte – paramètres manquants ou mal formés. | `{ "Code": 400, "Message": "Paramètres non valides." }` |
| 401 | Non autorisé – jeton invalide ou manquant. | `{ "Code": 401, "Message": "Authentification requise." }` |
| 404 | Non trouvé – le fichier, la feuille de calcul ou le commentaire n’existe pas. | `{ "Code": 404, "Message": "Ressource introuvable." }` |
| 500 | Erreur interne du serveur – condition inattendue sur le serveur. | `{ "Code": 500, "Message": "Erreur serveur." }` |

## Exemples de SDK
Ci-dessous figurent des extraits prêts à l’emploi pour les langages les plus populaires. Remplacez `<jeton jwt>`, `test.xlsx`, `Sheet1` et `A1` par vos propres valeurs.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configuration du client API
var config = new Configuration
{
    AccessToken = "<jeton jwt>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Commentaire supprimé. Statut : " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l'appel à WorksheetsApi.DeleteWorksheetComment : " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jeton jwt>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Commentaire supprimé, statut : " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception lors de l'appel à WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jeton jwt>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Commentaire supprimé. Statut : " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception lors de l’appel à WorksheetsApi->deleteWorksheetComment : ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jeton jwt>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Commentaire supprimé – statut : #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception lors de l’appel à WorksheetsApi->delete_worksheet_comment : #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jeton jwt>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Commentaire supprimé. Statut :", response.status);
    })
    .catch((error) => {
        console.error("Erreur lors de la suppression du commentaire :", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jeton jwt>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Commentaire supprimé. Statut :", response.status)
except Exception as e:
    print("Exception lors de l’appel à WorksheetsApi->delete_worksheet_comment :", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jeton jwt>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Commentaire supprimé. Statut : " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception lors de l’appel à WorksheetsApi->delete_worksheet_comment : $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jeton jwt>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // dossier (facultatif)
        "MyStorage",   // storageName (facultatif)
    )
    if err != nil {
        fmt.Printf("Erreur lors de l’appel à DeleteWorksheetComment : %v\n", err)
        return
    }
    fmt.Printf("Commentaire supprimé. Statut : %s\n", result.Status)
}
```

## Opérations connexes
- [Ajouter un commentaire de feuille de calcul](/comments/add/)  
- [Mettre à jour un commentaire de feuille de calcul](/comments/update/)  

## Limitation de débit
Aspose.Cells Cloud applique une **limite de débit par défaut de 100 requêtes par minute par compte**. Dépasser cette limite renvoie HTTP 429 Too Many Requests. Mettez en œuvre une backoff exponentielle ou respectez l’en-tête `Retry-After` pour éviter la limitation.

## Voir aussi
- **Spécification OpenAPI :** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Guide d’authentification :** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Dépôt SDK :** <https://github.com/aspose-cells-cloud>  

---