---
title: "Ta bort alla pivotdiagram i ett Excel-ark"
description: "Tar bort alla pivotdiagram från ett angivet ark med hjälp av Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, Pivotdiagram, Ta bort, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Ta bort alla pivotdiagram i ett Excel-ark

## Översikt
Denna åtgärd tar bort **alla** pivotdiagram från ett givet ark i en Excel-fil. Det är användbart när du behöver återställa ett arks analysfunktioner eller städa upp oanvända pivotdiagram med ett enda anrop.

## Förutsättningar
Innan du anropar API:t, se till att du har slutfört följande steg:

1. **Aspose Cloud-konto** – Skapa ett Aspose Cloud-konto om du inte redan har ett.  
2. **JWT-token** – Skapa en JSON Web Token (JWT) för autentisering. Se [Autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) för mer information.  
3. **Lagringsinställning** – Ladda upp mål-Excel-filen till Aspose Cloud-lagring eller till en ansluten extern lagring. Notera **mappen** och **lagringsnamnet** (om tillämpligt) där filen finns.

## Autentisering
Aspose.Cells Cloud API:er kräver **JWT-tokenbaserad autentisering**. Inkludera token i `Authorization`-huvudet i varje begäran:

```
Authorization: Bearer <jwt token>
```

## HTTP-begäran

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Parametrar för sökväg
| Namn | Typ | Krävs | Beskrivning |
|------|-----|-------|-------------|
| `name` | sträng | Ja | Filnamnet för Excel-filen (t.ex. `Sample.xlsx`). |
| `sheetName` | sträng | Ja | Namnet på arket från vilket alla pivotdiagram kommer att tas bort (t.ex. `Sheet1`). |

### Frågeparametrar
| Namn | Typ | Krävs | Beskrivning |
|------|-----|-------|-------------|
| `folder` | sträng | Nej | Mappen som innehåller filen. |
| `storageName` | sträng | Nej | Lagringsnamnet som ska användas (om filen inte finns i standardlagringen). |

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Lyckat svar
Tjänsten returnerar ett standardobjekt `CellsCloudResponse` som anger åtgärdens status.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Felhantering

| HTTP-status | Betydelse | Exempel på nyttolast |
|-------------|-----------|----------------------|
| **400** | Felaktig begäran – saknade eller ogiltiga parametrar | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | Auktoriseringsfel – ogiltig eller utgången JWT | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | Ej hittad – filen eller arket finns inte | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | Internt serverfel – oväntat misslyckande | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## SDK-exempel

Följande kodfragment visar hur du anropar åtgärden med flera Aspose.Cells Cloud SDK:n.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initiera API-klienten
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Konfigurera begäransparametrar
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
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
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
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

# Konfigurera API-klienten
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
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
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
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*Ytterligare SDK:n (Go, PHP, Ruby, Swift, Perl, Android) finns i [Aspose.Cells Cloud SDK-repositoriet](https://github.com/aspose-cells-cloud).*

## Se även
- [Ta bort ett specifikt pivotdiagram](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Hämta alla pivotdiagram i ett ark](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Översikt över autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI-specifikation för DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Dokumentet senast uppdaterat 2026-07-30. Allt innehåll är UTF-8-kodat.*