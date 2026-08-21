---
title: "Supprimer tous les tableaux croisés dynamiques d'une feuille Excel"
description: "Supprime tous les tableaux croisés dynamiques d'une feuille spécifiée à l'aide de l'API REST Aspose.Cells Cloud."
keywords: "Aspose.Cells, Tableau croisé dynamique, Supprimer, API REST, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Supprimer tous les tableaux croisés dynamiques d'une feuille Excel

## Vue d'ensemble
Cette opération supprime **tous** les tableaux croisés dynamiques d'une feuille donnée dans un fichier Excel. Elle est utile lorsque vous devez réinitialiser l'analyse d'une feuille ou nettoyer les tableaux croisés dynamiques inutilisés en une seule appel.

## Conditions préalables
Avant d'appeler l'API, assurez-vous d'avoir effectué les étapes suivantes :

1. **Compte Aspose Cloud** – Créez un compte Aspose Cloud si vous n'en avez pas encore.  
2. **Jeton JWT** – Générez un jeton Web JSON (JWT) pour l'authentification. Consultez le [guide d'authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) pour plus de détails.  
3. **Configuration du stockage** – Téléversez le fichier Excel cible vers le stockage Aspose Cloud ou vers un stockage externe connecté. Notez le **dossier** et le **nom du stockage** (le cas échéant) où se trouve le fichier.

## Authentification
Les API Aspose.Cells Cloud exigent une **authentification basée sur un jeton JWT**. Incluez le jeton dans l'en-tête `Authorization` de chaque requête :

```
Authorization: Bearer <jeton JWT>
```

## Requête HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Paramètres de chemin
| Nom | Type   | Obligatoire | Description |
|-----|--------|-------------|-------------|
| `name` | chaîne de caractères | Oui | Le nom du fichier Excel (par exemple, `Exemple.xlsx`). |
| `sheetName` | chaîne de caractères | Oui | Le nom de la feuille à partir de laquelle tous les tableaux croisés dynamiques seront supprimés (par exemple, `Feuil1`). |

### Paramètres de requête
| Nom | Type   | Obligatoire | Description |
|-----|--------|-------------|-------------|
| `folder` | chaîne de caractères | Non | Le dossier contenant le fichier. |
| `storageName` | chaîne de caractères | Non | Le nom du stockage à utiliser (si le fichier n’est pas dans le stockage par défaut). |

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

## Réponse réussie
Le service renvoie un objet standard `CellsCloudResponse` indiquant l’état de l’opération.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Gestion des erreurs

| Statut HTTP | Signification | Exemple de charge utile |
|-------------|---------------|-------------------------|
| **400** | Requête incorrecte – paramètres manquants ou non valides | `{ "Code": 400, "Message": "Paramètre requis manquant 'name'." }` |
| **401** | Non autorisé – jeton JWT invalide ou expiré | `{ "Code": 401, "Message": "Jeton d'authentification invalide." }` |
| **404** | Non trouvé – fichier ou feuille inexistante | `{ "Code": 404, "Message": "Feuille non trouvée." }` |
| **500** | Erreur interne du serveur – échec inattendu | `{ "Code": 500, "Message": "Une erreur inattendue s'est produite." }` |

## Exemples de SDK

Les extraits suivants montrent comment appeler l’opération à l’aide de plusieurs SDK Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialiser le client API
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configurer les paramètres de la requête
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Code de réponse : {response.Code}, statut : {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l’appel à CellsApi.DeleteWorksheetPivotTables : " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code : " + result.getCode() + ", Statut : " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Configurer le client API
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code : {response.code}, Statut : {response.status}')
except ApiException as e:
    print("Exception lors de l’appel à CellsApi->delete_worksheet_pivot_tables : %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code : ${result.code}, Statut : ${result.status}`);
    })
    .catch(err => {
        console.error('Erreur :', err);
    });
```

*D’autres SDK (Go, PHP, Ruby, Swift, Perl, Android) sont disponibles dans le [dépôt GitHub des SDK Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

## Voir aussi
- [Supprimer un tableau croisé dynamique spécifique](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Obtenir tous les tableaux croisés dynamiques d’une feuille](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Vue d’ensemble de l’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [Spécification OpenAPI pour DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Dernière mise à jour du document le 2026-07-30. Tout le contenu est encodé en UTF-8.*