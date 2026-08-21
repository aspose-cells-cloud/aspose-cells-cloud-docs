---
title: Vertikalen Seitenumbruch löschen – Aspose.Cells Cloud REST API
description: Entfernen Sie einen vertikalen Seitenumbruch aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Anforderungssyntax, Parameter, Beispiele, Antwortcodes und SDK-Snippets.
keywords: vertikalen Seitenumbruch löschen, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# Vertikalen Seitenumbruch löschen

Löschen Sie einen vertikalen Seitenumbruch aus einem Arbeitsblatt in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API.

---

## Voraussetzungen

* Ein **JWT-Authentifizierungstoken** muss im Header `Authorization` übermittelt werden.  
* Die Arbeitsmappe (`{name}`) muss im angegebenen **Ordner** oder **Speicher** gespeichert sein und für den API-Client zugänglich sein.

---

## HTTP-Anforderung

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parameter | Typ   | Ort   | Erforderlich | Beschreibung |
|-----------|--------|----------|----------|-------------|
| **name**      | string | path   | Ja | Der Name der Excel-Datei. |
| **sheetName** | string | path   | Ja | Der Name des Arbeitsblatts, das den Seitenumbruch enthält. |
| **index**     | integer| path   | Ja | Nullbasierter Index des zu löschenden vertikalen Seitenumbruchs. |
| **folder**    | string | query  | Nein | Pfad zum Ordner, in dem die Datei gespeichert ist. |
| **storageName**| string| query  | Nein | Name des Speicherdienstes. |

---

## Beispiel für eine Anforderung

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Erfolgsantwort

| Code | Beschreibung |
|------|-------------|
| **200** | Der vertikale Seitenumbruch wurde erfolgreich gelöscht. |

**Beispiel für Nutzdaten**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Fehlerantworten

| HTTP-Code | Beschreibung |
|-----------|-------------|
| **401** | Nicht autorisiert – fehlendes oder ungültiges Token. |
| **404** | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder der Seitenumbruchindex existiert nicht. |
| **400** | Ungültige Anforderung – fehlerhafte Anforderungssyntax oder ungültige Parameter. |
| **500** | Interner Serverfehler – unerwarteter Zustand aufgetreten. |

**Beispielhafte Fehlernutzdaten**

*401 – Nicht autorisiert*

```json
{
  "Code": 401,
  "Message": "Ungültiges Authentifizierungstoken."
}
```

*404 – Nicht gefunden*

```json
{
  "Code": 404,
  "Message": "Die angegebene Datei, das Arbeitsblatt oder der Seitenumbruchindex wurde nicht gefunden."
}
```

*400 – Ungültige Anforderung*

```json
{
  "Code": 400,
  "Message": "Die Anforderungsparameter sind ungültig oder fehlerhaft."
}
```

*500 – Interner Serverfehler*

```json
{
  "Code": 500,
  "Message": "Ein unerwarteter Serverfehler ist aufgetreten."
}
```

---

## SDK-Codebeispiele

Die folgenden Beispiele zeigen, wie der Vorgang **DeleteVerticalPageBreak** mithilfe verschiedener Aspose.Cells Cloud SDKs aufgerufen wird.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(SDK-Snippets für PHP, Ruby, Perl und andere Sprachen folgen dem gleichen Muster und sind im offiziellen GitHub-Repository verfügbar.)*

---

## Verwandte Ressourcen

* **OpenAPI-Spezifikation** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>  
* **Authentifizierungsanleitung** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Dokument zuletzt aktualisiert am: 2026‑07‑30*