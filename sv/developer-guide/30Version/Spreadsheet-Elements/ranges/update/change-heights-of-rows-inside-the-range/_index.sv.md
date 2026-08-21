---
title: "Ställ in radhöjd för ett intervall i Excel – Aspose.Cells Cloud API (v3.0)"
description: "Ändra radhöjden för rader inom ett visst intervall i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller slutpunkt, parametrar, cURL-exempel, exempelsvar och SDK-utdrag för flera språk."
keywords: "Aspose.Cells, radhöjd, intervall, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Ställ in radhöjd för ett intervall i Excel

Denna åtgärd uppdaterar radhöjden för ett angivet intervall på ett ark som lagras i Aspose Cloud-lagring.

## Förutsättningar / Autentisering

Du måste hämta ett JWT-åtkomsttoken från Aspose Cloud OAuth-tjänsten med scope **Cells.ReadWrite**.

Inkludera token i `Authorization`-headern i varje begäran:

```http
Authorization: Bearer <jwt token>
```

Om du inte har en token, följ **Aspose Cloud:s autentiseringsguide** för att begära en.

## HTTP-begäran

| Metod | URI |
|-------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Path-parametrar

| Namn | Typ | Beskrivning |
|------|-----|-------------|
| `name` | `string` | **Obligatoriskt.** Namnet på Excel-filen som är lagrad i molnet. |
| `sheetName` | `string` | **Obligatoriskt.** Det ark som innehåller målintervallen. |

### Query-parametrar

| Namn | Typ | Obligatoriskt | Beskrivning |
|------|-----|---------------|-------------|
| `value` | `number` | **Ja** | Önskad radhöjd (i punkter) som ska tillämpas på intervallet. |
| `folder` | `string` | Nej | Mappväg i lagringen där filen finns. |
| `storageName` | `string` | Nej | Namn på lagringstjänsten (om flera lagringar är konfigurerade). |

### Begärandetext (JSON)

Texten måste innehålla ett **Range**-objekt som definierar vilka rader som påverkas.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### JSON-schema för Range

| Egenskap | Typ | Obligatoriskt | Beskrivning |
|----------|-----|---------------|-------------|
| `FirstRow` | heltal | **Ja** | Nollbaserat index för den första raden i intervallet. |
| `RowCount` | heltal | **Ja** | Antal rader som höjden ska tillämpas på. |
| `FirstColumn` | heltal | Nej | Nollbaserat index för den första kolumnen (valfritt vid radhöjd endast). |
| `ColumnCount` | heltal | Nej | Antal kolumner som intervallet täcker (valfritt). |

Endast egenskaperna ovan används för radhöjdsåtgärden; överskottsfält ignoreras.

## Exempel på begäran

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Exempelsvar (lyckad begäran)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                | Beskrivning                                           |
|-----|--------------------------|-------------------------------------------------------|
| 200 | OK                       | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsinformation. |
| 400 | Felaktig begäran         | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad          | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast       | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel        | Oväntat serverfel. |

Alla svar innehåller en numerisk `Code` och en läsbar `Status` (eller `Message` vid fel). Ytterligare `ErrorDetails` kan anges vid fel.

## SDK-exempel

Följande kodsnuttar visar hur man anropar **Ställ in radhöjd för ett intervall** med de officiella Aspose.Cells Cloud SDK:erna.

| Språk | Exempel |
|-------|---------|
| **C#** | <details><summary>Visa kod</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Visa kod</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Visa kod</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Visa kod</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Radhöjd inställd'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Visa kod</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Visa kod</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Visa kod</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Visa kod</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Obs:** Alla SDK:er lägger automatiskt till nödvändig `Authorization: Bearer`-header när åtkomsttoken är konfigurerad.

## Se även

- **OpenAPI-specifikation** – Detaljerad specifikation för denna åtgärd: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK-lagringsplats** – Källkod och ytterligare språkbindningar: <https://github.com/aspose-cells-cloud>
- **Autentiseringsguide** – Hur du hämtar en JWT-token: <https://docs.aspose.cloud/cells/authentication/>

---