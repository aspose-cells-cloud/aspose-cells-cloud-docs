---
title: "Kopiera rader på ett Excel-arbetsblad"
description: "Kopiera data och format från specifika hela rader i ett Excel-arbetsblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar autentisering, begäran/svarsdetaljer, felhantering och SDK-exempel."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Kopiera rader på ett Excel-arbetsblad <span style="float:right;">v3.0</span>

Kopiera data och format från specifika hela rader i ett arbetsblad.

---

## Förutsättningar

| # | Krav |
|---|------|
| 1 | En giltig **JWT**-token. Se [autentiseringshandboken](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | Arbetsboken (`{name}`) måste redan finnas i den valda **mappen** / **lagringen**. |
| 3 | Målarbetsbladet (`{sheetName}`) måste finnas i arbetsboken. |
| 4 | (Valfritt) Känna till **mappen** och **storageName** om filen inte finns på standardplatsen. |

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Alla sökvägsparametrar skiftlägeskänsliga.*

### Sökvägsparametrar

| Parameter | Typ    | Obligatorisk | Beskrivning |
|-----------|--------|--------------|-------------|
| `name`    | sträng | ✅ | Namnet på arbetsboksfilen (t.ex. `test.xlsx`). |
| `sheetName` | sträng | ✅ | Namnet på arbetsbladet (t.ex. `Sheet1`). |

### Frågeparametrar

| Parameter            | Typ     | Obligatorisk | Beskrivning |
|----------------------|---------|--------------|-------------|
| `sourceRowIndex`     | heltal  | ✅ | Nollbaserat index för källraden. |
| `destinationRowIndex`| heltal  | ✅ | Nollbaserat index där raderna ska placeras. |
| `rowNumber`          | heltal  | ✅ | Antal rader att kopiera. |
| `worksheet`          | sträng  | ❌ | Arbetsbladsidentifierare; vanligtvis samma som **sheetName**. |
| `folder`             | sträng  | ❌ | Sökväg till mappen som innehåller arbetsboken. |
| `storageName`        | sträng  | ❌ | Namn på lagringstjänsten. |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Obs**  
> Ersätt `<jwt token>` med en giltig JWT-token som erhållits från autentiseringstjänsten.

---

## Lyckad svarskod

| Kod | Beskrivning |
|-----|-------------|
| **200** | Rader kopierade utan fel. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Svarsbrödet är en instans av `CellsCloudResponse`.

---

## Felhantering

| HTTP-kod | Betydelse                              | Exempel på svar |
|----------|----------------------------------------|-----------------|
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**  | Otillåten – ogiltig eller saknad JWT-token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | Hittades inte – arbetsbok eller arbetsblad existerar inte. | `{ "Code": 404, "Message": "File not found." }` |
| **500**  | Internt serverfel – oväntat tillstånd på servern. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Riktlinjer för felhantering**

* **400** – Kontrollera att alla obligatoriska frågeparametrar finns och är korrekt formaterade.  
* **401** – Generera eller uppdatera JWT-token igen.  
* **404** – Bekräfta namnen på arbetsboken och arbetsbladet, samt att filen finns i den angivna mappen/lagringen.  
* **500** – Försök igen efter en kort fördröjning; om problemet kvarstår, kontakta Aspose-support.

---

## SDK-exempel

Följande kodavsnitt visar hur man anropar **Copy Rows**-operationen med de officiella Aspose.Cells Cloud SDK:n.

| Språk | Exempel |
|-------|---------|
| **C#**   | <details><summary>Visa kod</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi(\"clientId\", \"clientSecret\");\nawait api.PostCopyWorksheetRowsAsync(name: \"test.xlsx\", sheetName: \"Sheet1\", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Visa kod</summary>```java\nCellsApi api = new CellsApi(\"clientId\", \"clientSecret\");\napi.postCopyWorksheetRows(\"test.xlsx\", \"Sheet1\", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Visa kod</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Visa kod</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Visa kod</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Visa kod</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Visa kod</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Visa kod</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Fullständiga källkodsfiler finns i [Aspose‑Cells‑Cloud GitHub-förrådet](https://github.com/aspose-cells-cloud).*

---

## Se även

- [Lägg till rad på ett Excel-arbetsblad](/rows/add/)  
- [Ta bort rad på ett Excel-arbetsblad](/rows/delete/)  
- [Uppdatera rad på ett Excel-arbetsblad](/rows/update/)  

--- 

*Sidan genererad den **{{DATE}}**. För den senaste versionen av denna API, se [OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*