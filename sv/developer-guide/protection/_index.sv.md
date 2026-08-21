---
title: "Aspose.Cells Cloud Web API – Ställ in / Ändra öppningslösenord för Excel-filer"
second_title: "Komplett utvecklarguide"
ArticleTitle: "Kalkylbladsskydd – Ställ in öppnings- och ändringslösenord"
linktitle: "Skydd"
type: docs
url: /sv/protection/
keywords: "Aspose.Cells, moln, API, kalkylblad, skydd, öppningslösenord, läs-skriv-lösenord, Excel"
description: "Lär dig hur du skyddar en Excel-arbetsbok med ett öppnings- eller läs-skriv-lösenord med Aspose.Cells Cloud REST API. Innehåller begärsyntax, kodexempel och felhantering."
weight: 60
---

I den här guiden lär du dig hur du ställer in, ändrar och tar bort både **öppningslösenordet** och **läs-skriv-lösenordet** för kalkylblad med Aspose.Cells Cloud Web API. Dessa funktioner hjälper dig att skydda känslig data i dina Excel-arbetsböcker.

**Förutsättningar**  
- Ett aktivt Aspose.Cells Cloud-konto med ett giltigt API-nyckel och SID.  
- Arbetsboken du vill skydda måste vara uppladdad till Aspose Cloud-lagring eller tillgänglig via en offentlig URL.  

**API-referens**  

| **HTTP-metod** | **Endpoint** | **Fråga / Sökvägsparametrar** | **Beskrivning** |
|----------------|--------------|-------------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (sökväg) – namn på arbetsboken<br>`openPassword` (fråga, valfritt) – lösenord som krävs för att öppna filen<br>`readWritePassword` (fråga, valfritt) – lösenord som krävs för att ändra filen | Ställer in eller uppdaterar öppnings- och/eller läs-skriv-lösenord för den angivna arbetsboken. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (sökväg) – namn på arbetsboken | Tar bort alla lösenord som skyddar arbetsboken. |

**Exempel på begäran (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**Exempel på svar (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Skydd för arbetsboken har uppdaterats."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas        | Ogiltigt eller saknat JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

**Kodexempel**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**Felhantering**  
När ett fel uppstår returnerar API:et en JSON-nyttolast som innehåller `Code`, `Message` och eventuellt `Description`. Kontrollera statuskoden och hantera den enligt behov i din programmlogik.

**Relaterade ämnen**  

- **[Hur du skyddar ett kalkylblad med ett lösenord med Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Hur du avskyddar ett kalkylblad med ett lösenord med Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---