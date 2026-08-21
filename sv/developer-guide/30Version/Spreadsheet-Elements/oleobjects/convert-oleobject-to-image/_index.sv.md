---
title: "Konvertera OLE-objekt till bild – Aspose.Cells Cloud REST API"
description: "Hämta ett inbäddat OLE-objekt från ett Excel-ark och konvertera det till PNG, JPEG, TIFF, GIF, EMF eller BMP med Aspose.Cells Cloud REST API."
keywords:
  - "konvertera OLE-objekt till bild"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "bildkonvertering"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Konvertera OLE-objekt till bild

Hämta ett inbäddat OLE-objekt från ett ark och returnera det i det begärda bildformatet.

---

## Förutsättningar

Innan du anropar detta slutställe måste du ha:

1. **Aspose.Cells Cloud-konto** – registrera dig på [Aspose Clouds portal](https://dashboard.aspose.cloud/).  
2. **Arbetsbok uppladdad till molnlagring** – använd API:et **Upload File** eller Aspose Clouds användargränssnitt.  
3. **JWT-åtkomsttoken** – skaffa en token enligt [autentiseringsguiden](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Säkerhet och autentisering

Alla Aspose.Cells Cloud-API:er kräver **JWT-tokenbaserad autentisering**. Inkludera token i `Authorization`-headern:

```http
Authorization: Bearer <jwt-token>
```

Endast HTTPS-slutställen stöds; använd aldrig `http://`.

---

## Begäran

### HTTP-metod
`GET`

### Slutställe
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Sökvägsparametrar

| Namn          | Typ    | Krävs | Beskrivning                              |
|---------------|--------|-------|------------------------------------------|
| `name`        | sträng | ✅    | Namn på arbetsboksfilen (t.ex. `Book1.xlsx`). |
| `sheetName`   | sträng | ✅    | Ark som innehåller OLE-objektet. |
| `objectNumber`| heltal| ✅    | Nollbaserat index för OLE-objektet.      |

### Frågeparametrar

| Namn        | Typ    | Krävs | Beskrivning |
|-------------|--------|-------|-------------|
| `format`    | sträng | ❌    | Önskat bildformat (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Om utelämnas är standardvärdet `png`. |
| `folder`    | sträng | ❌    | Sökväg till mappen där arbetsboken finns. |
| `storageName`| sträng| ❌    | Namn på lagringstjänsten (t.ex. `MyCloud`). |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Ersätt `<jwt-token>` med en giltig JWT-token.*

---

## Svar

| Status | Content‑Type            | Beskrivning |
|--------|-------------------------|-------------|
| `200`  | `image/png` (eller begärt format) | Binära bilddata som representerar OLE-objektet. |
| `400`  | `application/json`      | Ogiltiga begärningsparametrar. |
| `401`  | `application/json`      | Autentisering misslyckades ( saknad/ogiltig JWT). |
| `404`  | `application/json`      | Den angivna arbetsboken, arket eller OLE-objektet hittades inte. |
| `500`  | `application/json`      | Serverfel. |

### Hantering av binärt innehåll

API:et returnerar råa bildbytes. Du kan:

* **Spara direkt till en fil** (Linux/macOS-exempel):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Koda till Base64** för felsökning eller inbäddning i JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Exempel (delvis) Base64-utdata:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Fel-svar

| HTTP-status | Kod                    | Meddelande |
|-------------|------------------------|------------|
| `400`       | `InvalidParameter`     | En eller flera begärningsparametrar är ogiltiga. |
| `401`       | `AuthenticationFailed`| Saknad eller ogiltig JWT-token. |
| `404`       | `PropertyNotFound`     | Den begärda arbetsboken, arket eller OLE-objektet finns inte. |
| `500`       | `InternalError`        | Ett oväntat fel inträffade på servern. |

---

## SDK-exempel

Följande kodfragment visar hur du anropar åtgärden med de officiella SDK:erna. Ersätt `YOUR_JWT_TOKEN` och andra platshållare med dina egna värden.

| Språk | Exempel |
|-------|---------|
| **C#** | <details><summary>Visa kod</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Visa kod</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Visa kod</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Visa kod</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Visa kod</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Visa kod</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Visa kod</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Visa kod</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(Den fullständiga listan över SDK:er finns i [GitHub-förrådet](https://github.com/aspose-cells-cloud).)*

---

## Relaterade åtgärder

- **Lägg till OLE-objekt** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Uppdatera OLE-objekt** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Ta bort OLE-objekt** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Hämta lista över OLE-objekt** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Se motsvarande API-referenssidor för mer information.

---

## Ytterligare resurser

- **OpenAPI-specifikation** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Autentiseringsguide** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK-förråd** – <https://github.com/aspose-cells-cloud>
- **Prestanda och tillgänglighet** – Kör Lighthouse- och axe‑core-granskningar för att säkerställa optimala laddningstider och WCAG 2.1 AA-kompatibilitet.

---
---