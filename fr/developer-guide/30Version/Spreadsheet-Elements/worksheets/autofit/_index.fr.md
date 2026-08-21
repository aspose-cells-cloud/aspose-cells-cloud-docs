---
---
title: "Travailler avec l’ajustement automatique dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajustement automatique"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "ajustement automatique, colonne, ligne, Aspose.Cells, Cloud, Excel, API, redimensionnement"
description: "Découvrez comment redimensionner automatiquement les lignes et les colonnes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples en cURL, .NET, Java et Python."
weight: 20
ArticleTitle: "Travailler avec l’ajustement automatique dans une feuille de calcul Excel – Aspose.Cells Cloud API"
---

## Travailler avec l’ajustement automatique dans une feuille de calcul Excel

- [Comment ajuster automatiquement une colonne dans une feuille de calcul Excel.](/cells/worksheets/autofit/column/)
- [Comment ajuster automatiquement plusieurs colonnes dans une feuille de calcul Excel.](/cells/worksheets/autofit/columns/)
- [Comment ajuster automatiquement une ligne dans une feuille de calcul Excel.](/cells/worksheets/autofit/row/)
- [Comment ajuster automatiquement plusieurs lignes dans une feuille de calcul Excel.](/cells/worksheets/autofit/rows/)

**Prérequis**  
Avant d’utiliser les opérations d’ajustement automatique, vous devez disposer de :

1. Un compte Aspose.Cells Cloud avec un **Client Id** et un **Client Secret** valides.  
2. Un classeur téléchargé dans le stockage Aspose Cloud (ou accessible via une URL publique).  
3. Le nom de la feuille de calcul que vous souhaitez modifier.

**Référence API**

| Opération | Méthode HTTP | Point de terminaison | Paramètres requis | Corps de la requête | Réponse exemple | Codes de statut |
|-----------|-------------|----------------------|--------------------|------------------|----------------|----------------|
| Ajuster automatiquement une **colonne** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (chemin) <br> `columnIndex` (requête) | *aucun* | `{ "code": 200, "status": "OK", "message": "Colonne ajustée automatiquement." }` | 200, 400, 401, 404, 500 |
| Ajuster automatiquement des **colonnes** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (chemin) <br> `startColumn`, `endColumn` (requête) | *aucun* | `{ "code": 200, "status": "OK", "message": "Colonnes ajustées automatiquement." }` | 200, 400, 401, 404, 500 |
| Ajuster automatiquement une **ligne** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (chemin) <br> `rowIndex` (requête) | *aucun* | `{ "code": 200, "status": "OK", "message": "Ligne ajustée automatiquement." }` | 200, 400, 401, 404, 500 |
| Ajuster automatiquement des **lignes** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (chemin) <br> `startRow`, `endRow` (requête) | *aucun* | `{ "code": 200, "status": "OK", "message": "Lignes ajustées automatiquement." }` | 200, 400, 401, 404, 500 |

**Exemples de code**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Authentification
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Appel de l’ajustement automatique des colonnes
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Ajustement automatique des lignes
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Ajustement automatique d’une seule colonne
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Ces extraits de code illustrent comment :

1. S’authentifier auprès d’Aspose.Cells Cloud à l’aide de votre **Client Id** et **Client Secret**.  
2. Appeler le point de terminaison d’ajustement automatique approprié pour les colonnes ou les lignes.  
3. Traiter la réponse, qui confirme que l’opération a réussi.

**Étapes suivantes**

Une fois l’appel d’ajustement automatique terminé, vous pouvez télécharger le classeur mis à jour :

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

N’hésitez pas à ajuster les paramètres `startColumn`, `endColumn`, `startRow` et `endRow` pour cibler des plages spécifiques.
---