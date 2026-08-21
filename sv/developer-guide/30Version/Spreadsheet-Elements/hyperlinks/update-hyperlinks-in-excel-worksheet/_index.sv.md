---
title: "Uppdatera en hyperlänk i ett Excel-arbetsblad – Aspose.Cells Cloud API-guide"
description: "Lär dig hur du uppdaterar en hyperlänk i ett Excel-arbetsblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, schemat för begäran, cURL-exempel, SDK-utdrag, felhantering, gränssnitt för frekvensbegränsning och förutsättningar."
keywords:
  - "Aspose.Cells"
  - "uppdatering av hyperlänk"
  - "Excel API"
  - "REST API"
  - "molnarkalkylblad"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Uppdatera en hyperlänk i ett Excel-arbetsblad  

**API-version:** v3.0  

Operationen **PostWorksheetHyperlink** uppdaterar en befintlig hyperlänk i ett arbetsblad som identifieras med dess nollbaserade index.

---

## Innehållsförteckning
1. [Förutsättningar](#prerequisites)  
2. [Frekvensbegränsning](#rate-limiting)  
3. [Slutpunkt](#endpoint)  
4. [Parametrar](#parameters)  
   - [Sökvägsparametrar](#path-parameters)  
   - [Frågeparametrar](#query-parameters)  
   - [Schemat för begärandetexten](#request-body-schema)  
5. [Svar](#responses)  
   - [Framgångsrikt svar](#success-response)  
   - [Felsvar](#error-responses)  
6. [cURL-exempel](#curl-example)  
7. [SDK-kodutdrag](#sdk-code-samples)  
8. [Se även](#see-also)  

---

## Förutsättningar <a name="prerequisites"></a>

| Krav | Beskrivning |
|------|-------------|
| **Autentisering** | JWT-tokenbaserad autentisering. Skaffa en token enligt beskrivningen i [Autentiseringsguiden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Lagring** | Arbetsboken måste lagras i ett stödsamt Aspose Cloud-lagringssystem (standard är **Default**). |
| **Rättigheter** | JWT-token måste ha rättighet att läsa och skriva målarbetsboken. |
| **Headers** | `Content-Type: application/json` och `Accept: application/json` krävs för alla begäranden. |

---

## Frekvensbegränsning <a name="rate-limiting"></a>

Aspose.Cells Cloud tillämpar en **högsta gräns på 60 begäranden per minut per åtkomsttoken**. Överskridning av denna gräns returnerar HTTP **429 Too Many Requests**. Implementera exponentiell backoff eller respektera `Retry-After`-headern när throttling uppstår.

---

## Slutpunkt <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Uppdaterar hyperlänken identifierad med `hyperlinkIndex` i arbetsbladet `sheetName` i filen `name`.*

---

## Parametrar <a name="parameters"></a>

### Sökvägsparametrar <a name="path-parameters"></a>

| Namn              | Typ    | Krävs | Beskrivning |
|-------------------|--------|-------|-------------|
| `name`            | string | ✅ | Namn på Excel-filen (inklusive filtillägg). |
| `sheetName`       | string | ✅ | Namn på arbetsbladet som innehåller hyperlänken. |
| `hyperlinkIndex`  | integer| ✅ | Nollbaserat index för hyperlänken som ska uppdateras. |

### Frågeparametrar <a name="query-parameters"></a>

| Namn          | Typ    | Krävs | Beskrivning |
|---------------|--------|-------|-------------|
| `folder`      | string | ❌ | Sökväg till mapp i lagringen där arbetsboken finns. |
| `storageName` | string | ❌ | Namn på lagringstjänsten (t.ex. `Default`). |

### Schemat för begärandetexten <a name="request-body-schema"></a>

Begärandetexten måste innehålla ett **`hyperlink`**-objekt. Endast de fält du vill ändra behöver anges; utelämnade valfria fält behåller sina befintliga värden.

| Fält              | Typ    | Krävs | Beskrivning |
|-------------------|--------|-------|-------------|
| `Address`         | string | ✅ | Mål-URL för hyperlänken. |
| `Area`            | object | ✅ | Cellomfång där hyperlänken placeras. Måste innehålla `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (alla heltal, nollbaserade). |
| `ScreenTip`       | string | ❌ | Verktygstips som visas vid muspekning. |
| `TextToDisplay`   | string | ❌ | Text som visas i cellen. |
| `link`            | object| ❌ | Hypermedia-länkar (`Href`, `Rel`, `Title`, `Type`). Vanligtvis utelämnas i begärandepayloads. |

**Definition av `Area`-objektet**

| Delfält        | Typ    | Krävs | Beskrivning |
|----------------|--------|-------|-------------|
| `StartRow`     | integer| ✅ | Nollbaserat startradindex. |
| `StartColumn`  | integer| ✅ | Nollbaserat startkolumnindex. |
| `EndRow`       | integer| ✅ | Nollbaserat slutradindex. |
| `EndColumn`    | integer| ✅ | Nollbaserat slutkolumnindex. |

---

## Svar <a name="responses"></a>

### Framgångsrikt svar <a name="success-response"></a>

| Fält | Typ    | Beskrivning |
|------|--------|-------------|
| `Code`| integer| HTTP-statuskod (200 för framgång). |
| `Status`| string| Textuellt statusvärde (`OK`). |
| `Hyperlink`| object (valfritt) | Det uppdaterade hyperlänkobjektet, returneras när `link`-delobjektet begärs. |

**Exempel på JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Felsvar <a name="error-responses"></a>

| HTTP-kod | Anledning | Exempel på kropp |
|----------|-----------|----------------|
| **400** | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Oautentiserad – saknad eller ogiltig JWT-token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Inte hittad – arbetsbok, arbetsblad eller hyperlänk finns inte. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | För många begäranden – frekvensbegränsning överskriden. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Internt serverfel – oväntat serverfel. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURL-exempel <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC-hemsida",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Svar**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Tips:* Spara JSON-payloaden i en fil (t.ex. `payload.json`) och referera till den med `--data @payload.json` för tydligare kopiering och klistra in.

---

## SDK-kodutdrag <a name="sdk-code-samples"></a>

Följande utdrag visar hur man anropar **PostWorksheetHyperlink** med de officiella Aspose.Cells Cloud SDK:erna. Ersätt plats hållare (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` etc.) med riktiga värden.

| Språk | Exempel |
|-------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = "https://www.msnbc.com/",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = "MSNBC-hemsida",\n    TextToDisplay = "MSNBC"\n};\nvar response = api.PostWorksheetHyperlink("test.xlsx", "Sheet1", 1, hyperlink, folder: "samples");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress("https://www.msnbc.com/");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip("MSNBC-hemsida");\nhyperlink.setTextToDisplay("MSNBC");\nCellsCloudResponse resp = api.postWorksheetHyperlink("test.xlsx", "Sheet1", 1, hyperlink, "samples", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address="https://www.msnbc.com/",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip="MSNBC-hemsida",\n    text_to_display="MSNBC"\n)\nresponse = api.post_worksheet_hyperlink("test.xlsx", "Sheet1", 1, hyperlink, folder="samples")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC-hemsida',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: "https://www.msnbc.com/", Area: &area, ScreenTip: "MSNBC-hemsida", TextToDisplay: "MSNBC"}\nresp, _ := client.PostWorksheetHyperlink("test.xlsx", "Sheet1", 1, hyperlink, "samples", "")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC-hemsida');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC-hemsida',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC-hemsida', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, " ", $resp->{Status}, "\n";\n``` |

*Alla SDK:er är öppen källkod och kan hittas i [Aspose.Cells Cloud GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud).*

---

## Se även <a name="see-also"></a>

- **Autentisering** – [Kom igång med JWT-tokens](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Lagringsoperationer** – [Ladda upp en fil](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Andra hyperlänksoperationer** – [Lägg till en hyperlänk](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Ta bort en hyperlänk](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI-specifikation** – Fullständig definition av slutpunkten: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Dokumentet uppdaterades senast: 2026-07-30*