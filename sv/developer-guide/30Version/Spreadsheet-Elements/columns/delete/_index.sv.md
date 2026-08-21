---
title: "Ta bort kolumn från ett Excel-ark med Aspose.Cells Cloud API"
description: "Lär dig hur du tar bort en eller flera kolumner från ett Excel-ark via Aspose.Cells Cloud REST API. Innehåller autentisering, begäran syntax, parametrar, svar, felhantering och SDK-exempel."
keywords: ["Aspose.Cells", "Ta bort kolumn", "Excel API", "REST", "Cloud", "Ark", "Kolumner"]
date: 2026-07-30
api_version: "v3.0"
---

# Ta bort kolumn från Excel-ark

**Endpoint**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

Åtgärden tar bort en enskild kolumn eller ett intervall av kolumner från ett ark. Cellreferenser (inklusive formler) kan automatiskt uppdateras efter borttagning.

---

## Innehållsförteckning
1. [Förutsättningar](#prerequisites)  
2. [Autentisering](#authentication)  
3. [Begäran-URL och HTTP-metod](#request-url--http-method)  
4. [Parametrar](#parameters)  
   - [Sökvägsparametrar](#path-parameters)  
   - [Frågeparametrar](#query-parameters)  
5. [cURL-exempel](#curl-example)  
6. [Svar](#responses)  
7. [Felkoder](#error-codes)  
8. [SDK-exempel](#sdk-samples)  
9. [Ytterligare anteckningar](#additional-notes)  

---

## Förutsättningar
- En giltig **JWT-åtkomsttoken** som erhållits via Aspose Cloud:s autentiseringsflöde.  
- Arbetsboken (`{name}`) måste redan vara uppladdad till Aspose Cloud-lagring (eller tillgänglig via frågeparametrarna `folder`/`storageName`).  

---

## Autentisering
Alla Aspose.Cells Cloud-begäranden kräver **Bearer token**-autentisering.

```http
Authorization: Bearer <access_token>
```

Se [autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) för detaljer om hur du erhåller en JWT-token.

---

## Begäran-URL och HTTP-metod
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – arbetsbokens filnamn (t.ex. `test.xlsx`).  
- **`{sheetName}`** – arkets namn (t.ex. `Sheet1`).  
- **`{columnIndex}`** – nollbaserat index för den första kolumn som ska tas bort.

---

## Parametrar

| Namn              | Plats  | Typ     | Obligatorisk | Beskrivning |
|-------------------|--------|---------|--------------|-------------|
| **name**          | path   | string  | ✅ Ja        | Arbetsbokens filnamn. |
| **sheetName**     | path   | string  | ✅ Ja        | Arkets namn. |
| **columnIndex**   | path   | integer | ✅ Ja        | Nollbaserat index för den första kolumn som ska tas bort. |
| **startColumn**   | query  | integer | ❌ Nej       | Nollbaserat index där borttagningen börjar. Standardvärde är `columnIndex` om utelämnat. |
| **totalColumns**  | query  | integer | ❌ Nej       | Antal kolumner att ta bort. Om utelämnas tas endast den kolumn som anges med `columnIndex` bort. |
| **updateReference** | query | boolean | ❌ Nej     | När `true` uppdateras cellreferenser (inklusive formler) i hela arbetsboken efter borttagning. |
| **folder**        | query  | string  | ❌ Nej       | Sökvägen till mappen som innehåller arbetsboken. |
| **storageName**   | query  | string  | ❌ Nej       | Namn på Aspose Cloud-lagringstjänsten. |

> **Obs** – Parametern `columns` som visas i API-specifikationen på lågnivå har ersatts av de mer uttrycksfulla frågeparametrarna `startColumn` och `totalColumns`. Båda metoderna stöds för bakåtkompatibilitet.

---

## cURL-exempel

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Förklaring
- Tar bort kolumn **B** (`columnIndex = 1`) från `Sheet1` i `test.xlsx`.  
- `startColumn=1` och `totalColumns=1` anger en borttagning av en enskild kolumn.  
- `updateReference=true` säkerställer att formler och andra referenser automatiskt justeras.

---

## Svar

| HTTP-kod | Beskrivning | Exempel |
|----------|-------------|---------|
| **200**  | Lyckades – kolumn(er) togs bort. | `{ "Code": 200, "Status": "OK" }` |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401**  | Oauktorisering – saknad eller ogiltig JWT-token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | Ej hittad – arbetsboken eller arket finns inte. | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500**  | Internt serverfel – oväntat tillstånd på servern. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

Svarsbrödtexten följer den generella modellen **`CellsCloudResponse`**.

---

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktorisering              | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
---

## SDK-exempel

Här är klara att köra kodsnuttar för de mest populära SDK:erna. Ersätt platshållarvärden (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` etc.) med dina egna uppgifter.

| Språk | Exempel |
|-------|--------|
| **C#** | <details><summary>Visa kod</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Visa kod</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Visa kod</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Visa kod</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Visa kod</summary> <br>```go\npackage main\n\nimport (\n    "context"\n    "fmt"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_ACCESS_TOKEN>"\n    cfg.BasePath = "https://api.aspose.cloud"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), "test.xlsx", "Sheet1", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println("Error:", err)\n        return\n    }\n    fmt.Println("Status:", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Visa kod</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts "Status: #{resp.status}"\nrescue AsposeCellsCloud::ApiError => e\n  puts "Exception: #{e}"\nend\n```</details> |
| **PHP** | <details><summary>Visa kod</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo "Status: " . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Visa kod</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint "Status: ", $response->{Status}, "\n";\n```</details> |

*Alla SDK lägger automatiskt till den nödvändiga `Authorization`-headers when `access_token` konfigurerats.*

---

## Ytterligare anteckningar

### Säkerhetsheaders (rekommenderas för produktion)
När dokumentations sidan visas, inkludera följande HTTP-svarsheaders för att förbättra säkerheten:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Prestandatips
- Ladda tredjeparts analysskript (`gtag.js`, `containerize.js`) med attributet `async` eller skjut upp dem tills sidan har renderats.  
- Minifiera eventuella anpassade JavaScript/CSS-buntar.  
- Förhandsladda små SVG-ikoner om de blockerar rendering:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO-förbättringar (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Ta bort kolumn från Excel-ark med Aspose.Cells Cloud API",
  "description": "Lär dig hur du tar bort en eller flera kolumner från ett Excel-ark via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Ta bort kolumn", "Excel", "REST API"]
}
```

Placera kodsnutten i ett `<script type="application/ld+json">`-block i HTML-headern.

### Tillgänglighet
- Alla dekorativa bilder använder `alt=""` eller döljs med `aria-hidden="true"`.  
- Open Graph-bilden inkluderas nu med ett `alt`-attribut i metataggen för kompletthet.  

---

## Se även
- [OpenAPI-specifikation för DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Översikt över autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Aspose.Cells Cloud SDK:er på GitHub](https://github.com/aspose-cells-cloud)  

---