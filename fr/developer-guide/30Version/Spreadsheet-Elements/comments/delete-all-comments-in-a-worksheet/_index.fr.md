---
title: "Supprimer tous les commentaires d'une feuille de calcul"
description: "Supprimer tous les commentaires d'une feuille de calcul dans un fichier Excel à l'aide de l'API Aspose.Cells Cloud. Découvrez le point de terminaison DELETE, les paramètres requis, l'authentification, la requête cURL exemple, le format de réponse, les codes d'erreur et les exemples de SDK."
keywords: "Aspose, Cells, supprimer commentaires, feuille de calcul, API, REST, Excel, cloud"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Supprimer tous les commentaires d'une feuille de calcul

**Version de l'API :** `v3.0`  
**Ressource :** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud fournit un point de terminaison REST robuste permettant de supprimer **tous** les commentaires d'une feuille de calcul spécifiée. Cette opération est irréversible ; une fois exécutée, les commentaires ne peuvent plus être récupérés.

---

## Conditions préalables

| Exigence | Détails |
|----------|---------|
| **Authentification** | Un jeton d'accès JWT valide est requis dans l'en-tête `Authorization` (`Bearer <jeton jwt>`). Obtenez le jeton via le [flux d'authentification OAuth2](https://docs.aspose.cloud/cells/authentication/). |
| **Stockage** | Le fichier doit se trouver dans un espace de stockage accessible à Aspose.Cells Cloud (l'espace de stockage par défaut est utilisé si `storageName` est omis). |
| **Permissions** | Le jeton doit disposer des autorisations de lecture et d'écriture sur le fichier cible. |
| **SDK (facultatif)** | Des SDK sont disponibles pour .NET, Java, PHP, Ruby, Node.js, Python, Perl et Go (voir la section **Exemples de SDK**). |

---

## Requête HTTP

### Point de terminaison

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Paramètres de chemin

| Nom         | Type   | Description |
|-------------|--------|-------------|
| `name`      | string | Nom du fichier Excel (par exemple, `test.xlsx`). |
| `sheetName` | string | Nom de la feuille de calcul (par exemple, `Sheet1`). |

### Paramètres de requête

| Nom            | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `folder`       | string | facultatif  | Chemin vers le dossier contenant le fichier. |
| `storageName`  | string | facultatif  | Nom de l'espace de stockage où se trouve le fichier. |

### En-têtes de requête

| En-tête               | Valeur                              |
|-----------------------|-------------------------------------|
| `Authorization`       | `Bearer <jeton jwt>`                |
| `Accept`              | `application/json`                  |
| `Content-Type`        | `application/json`                  |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

*Remplacez `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` et `<jeton jwt>` par vos propres valeurs réelles.*

---

## Réponse

### Succès (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Le corps de la réponse suit le modèle `CellsCloudResponse`.

### Réponses d’erreur

| Code HTTP | Signification                                  | Exemple de corps |
|-----------|-----------------------------------------------|------------------|
| **400**   | Requête incorrecte – paramètres invalides.   | `{ "Code": 400, "Message": "Requête invalide." }` |
| **401**   | Non autorisé – jeton JWT manquant ou invalide. | `{ "Code": 401, "Message": "Échec de l'authentification." }` |
| **404**   | Introuvable – le fichier ou la feuille de calcul n'existe pas. | `{ "Code": 404, "Message": "Ressource introuvable." }` |
| **500**   | Erreur interne du serveur.                    | `{ "Code": 500, "Message": "Erreur serveur." }` |

---

## Exemples de SDK

Les extraits suivants montrent comment appeler le point de terminaison à l’aide des SDK officiels Aspose.Cells Cloud (version 3.13.0). Remplacez les valeurs de remplacement (`<fileName>`, `<sheet>`, `<jwt token>`, etc.) par vos propres données.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Nom du fichier.
var sheetName = "Sheet1"; // string | Nom de la feuille de calcul.
var folder = "Documents"; // string | Chemin du dossier (facultatif)
var storageName = "MyStorage"; // string | Nom du stockage (facultatif)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l'appel à WorksheetsApi.DeleteWorksheetComments : " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Exception lors de l\'appel à WorksheetsApi->deleteWorksheetComments : ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # facultatif
storage_name = 'MyStorage'    # facultatif

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Exception lors de l'appel à WorksheetsApi->delete_worksheet_comments : #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Erreur : ", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # facultatif
storage_name = "MyStorage"    # facultatif

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Exception lors de l'appel à WorksheetsApi->delete_worksheet_comments :", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Exception lors de l'appel à WorksheetsApi->delete_worksheet_comments : $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Erreur : %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Notes et limites

* Cette opération **supprime tous les commentaires** de la feuille de calcul spécifiée. Utilisez-la avec précaution — il n’existe aucun moyen d’annuler l’opération.
* La requête **n’accepte pas** de corps de requête ; toutes les informations nécessaires sont transmises via l’URL et les en-têtes.
* Si le fichier cible est **protégé** ou si la feuille de calcul est en **lecture seule**, l’API renverra une erreur `400` ou `401`, selon la cause sous-jacente.
* Le point de terminaison fonctionne avec des fichiers stockés dans **Aspose Cloud Storage**, ainsi qu’avec **Amazon S3**, **Azure Blob** ou **Google Cloud Storage**, à condition qu’ils soient correctement référencés via `storageName`.

---

## Ressources associées

* **Spécification OpenAPI** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Guide d’authentification** – [OAuth2 pour Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **Dépôt des SDK** – <https://github.com/aspose-cells-cloud>
* **API générale des feuilles de calcul** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Dernière mise à jour : 2026‑07‑30*