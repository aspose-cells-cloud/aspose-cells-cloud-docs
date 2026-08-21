---
title: "Hämta AutoFilter"
description: "Hämta AutoFilter-beskrivningen från ett Excel-ark med Aspose.Cells Cloud REST API."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Hämta AutoFilter-beskrivning från ett ark

**Version:** v3.0  
**Endpoint:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Obs!** Alla exempel på begäranden använder **HTTPS**. Skicka aldrig JWT-token över en osäker anslutning.

---

## Översikt

En **AutoFilter** tillåter användare att filtrera rader i ett kalkylark baserat på kolumnvärden, färger, anpassade kriterier med mera. Detta API returnerar hela AutoFilter-konfigurationen – inklusive filterkolumner, intervall och sorteringsdetaljer – så att du kan inspektera eller återskapa filterinställningarna programmatiskt.

---

## Förutsättningar

| Krav | Beskrivning |
|------|-------------|
| **Autentisering** | En giltig JWT-token krävs. Se [autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Filstplacering** | Arbetsboken måste lagras i Aspose Cloud Storage (eller en ansluten extern lagring). |
| **Format som stöds** | Alla Excel-format som stöds av Aspose.Cells (t.ex. `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (valfritt)** | Om du föredrar att använda ett SDK, installera lämpligt paket (t.ex. `dotnet add package Aspose.Cells-Cloud` för .NET). |

---

## Begäran

### HTTP-begäran

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Parametrar för sökväg

| Parameter | Typ    | Beskrivning |
|-----------|--------|-------------|
| `name`      | string | **Obligatoriskt.** Arbetsbokens filnamn, inklusive filtillägg. |
| `sheetName` | string | **Obligatoriskt.** Namn på kalkylarket där AutoFilter ska hämtas från. |

### Frågeparametrar

| Parameter   | Typ    | Beskrivning |
|-------------|--------|-------------|
| `folder`      | string | Sökväg till mapp i lagringen där arbetsboken finns. |
| `storageName` | string | Namn på den lagring som ska användas. |

### Säkerhet

API:et använder **JWT-tokenbaserad autentisering**. Inkludera token i `Authorization`-headern:

```http
Authorization: Bearer <your_jwt_token>
```

---

## Exempel på begäran (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Svar

Tjänsten returnerar ett JSON-objekt som innesluter `AutoFilter`-modellen.

### Schema för framgångsrikt svar

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### Exempel på svar

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                      |
|-----|---------------------------|--------------------------------------------------|
| 200 | OK                        | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran          | Saknade eller ogiltiga parametrar (t.ex. format som inte stöds). |
| 401 | Autentisering krävs       | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel         | Oväntat serverfel. |
---

## SDK-exempel

Åtgärden finns tillgänglig i alla Aspose.Cells Cloud SDK:n. Nedan finns klara, körbara kodsnuttar.

| Språk | Exempel |
|-------|---------|
| **C#** | <details><summary>Visa kod</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Visa kod</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Visa kod</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Visa kod</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Visa kod</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Visa kod</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Visa kod</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Visa kod</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

För en komplett lista över SDK:n och installationsinstruktioner, besök [Aspose.Cells Cloud GitHub-repositoriet](https://github.com/aspose-cells-cloud).

---

## Se även

- [AutoFilter – OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Lagringsåtgärder](https://docs.aspose.cloud/cells/storage/)  

---