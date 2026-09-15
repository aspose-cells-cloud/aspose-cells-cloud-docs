---
url: /translate-spreadsheet/
title: "Aspose.Cells Cloud Web API – Translate Spreadsheet to Target Language"
linktitle: "Translate Spreadsheet"
type: docs
description: "Use Aspose.Cells Cloud AI to translate Excel workbooks (XLSX, CSV, etc.) to any language. Preserve formulas, charts, and multi-sheet structure. Includes API spec, SDK examples, and error codes."
keywords: "Aspose.Cells Cloud, translate spreadsheet API, AI translation, spreadsheet translation, multi-sheet translation, cloud spreadsheet processing, targetLanguage, neural translation"
date: 2024-03-15T00:00:00Z
lastmod: 2024-05-22T14:30:00Z
robots: index, follow
canonical: https://docs.aspose.com/cells-cloud/translate-spreadsheet/
weight: 100
---

The **TranslateSpreadsheet** endpoint translates all textual content in an Excel workbook to a specified target language using AI-powered neural translation models. It preserves cell formatting, formulas, charts, pivot tables, conditional formatting, and multi-sheet structure—making it ideal for globalizing financial reports, dashboards, and compliance documents. Supported input formats include XLS, XLSX, XLSM, CSV, and ODS.

> **Note:** This API is available in Aspose.Cells Cloud v4.0+, released in March 2024.

## Prerequisites

Before calling the API, ensure you have:

- A valid Aspose.Cells Cloud account and API credentials (`Client ID` and `Client Secret`)
- A personal access token (JWT) generated using your credentials  
  *(See [Authentication Guide](https://docs.aspose.com/cells-cloud/Authentication/) for setup instructions.)*

## Translate Spreadsheet API

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### Request Parameters

| Parameter Name | Type   | Location | Required | Description |
|:---------------|:-------|:---------|:---------|:------------|
| `Spreadsheet`  | File   | FormData | Yes      | The Excel workbook to translate. Supported formats: `.xls`, `.xlsx`, `.xlsm`, `.csv`, `.ods`. Maximum size: **50 MB**. |
| `targetLanguage` | string | Query | Yes | ISO 639-1 language code for the output language (e.g., `"es"` for Spanish, `"fr"` for French, `"de"` for German). Must be supported by the underlying translation service. |
| `region` | string | Query | No | Locale identifier (e.g., `"US"`, `"EU"`, `"CN"`, `"en-US"`) influencing date/number/currency formatting. If omitted, the original workbook region is retained. |
| `password` | string | Query | No | Password for protected workbooks. Omit if the file is not encrypted. |

### Response

**Successful Response (200 OK)**  
- **Headers**  
  `Content-Type: application/octet-stream` (or `text/csv` for CSV input/output)  
  `Content-Disposition: attachment; filename="translated.xlsx"`  
  `Content-Length: <size_in_bytes>`  
- **Body**  
  Binary stream of the translated spreadsheet file.

**Error Responses (JSON format)**  
Standard Aspose.Cells Cloud error model:
```json
{
  "code": "400",
  "message": "Bad Request",
  "details": ["Invalid targetLanguage parameter"]
}
```

| Status Code | Meaning               | Description |
|:------------|:----------------------|:------------|
| `200`       | OK                    | Translation completed successfully. |
| `400`       | Bad Request           | Invalid or missing parameters (e.g., unsupported file type, invalid language code). |
| `401`       | Unauthorized          | Invalid or expired JWT token. |
| `413`       | Payload Too Large     | Uploaded file exceeds 50 MB limit. |
| `500`       | Internal Server Error | Translation service unavailable or internal processing error. |

## Use Cases

| Industry | Application |
|:---------|:------------|
| **Finance** | Convert quarterly reports into localized versions for regional headquarters while preserving complex formulas and audit trails. |
| **Marketing** | Generate multilingual campaign performance dashboards for global teams with consistent chart layouts. |
| **Education** | Translate gradebooks and assignment sheets into student-native languages without manual reformatting. |
| **Regulatory** | Produce country-specific compliance spreadsheets (e.g., GDPR, SOX) with validated rules and language compliance. |

## Key Features

- **AI-Powered Neural Translation** – Context-aware translation using state-of-the-art models for accuracy and natural phrasing.  
- **Zero Layout Disruption** – Formulas, charts, pivot tables, conditional formatting, and worksheet order remain intact.  
- **Multi-Sheet Automation** – Processes all worksheets in a single request—no per-sheet loops required.  
- **Cloud-Native Integration** – Seamlessly embeds into CI/CD pipelines, serverless functions (e.g., AWS Lambda), or enterprise back-ends via REST or SDK.

## SDK Integration

### Using Aspose.Cells Cloud SDKs

SDKs abstract low-level HTTP details and simplify authentication, file handling, and error parsing. Choose from the following language-specific implementations:

- [.NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/releases/tag/v24.6)  
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/releases/tag/v22.9)  
- [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/releases/tag/v23.3)  
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/releases/tag/v22.10)  
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/releases/tag/v24.2)  
- [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/releases/tag/v22.5)  
- [Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/releases/tag/v22.4)  
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/releases/tag/v24.1)

> **Tip:** Always link to a specific SDK version (e.g., `v24.6`) to avoid breaking changes.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<highlight csharp>}}
// Example: C# SDK v24.6
var cellsApi = new CellsApi(clientId, clientSecret);
var response = cellsApi.TranslateSpreadsheet("input.xlsx", targetLanguage: "es", region: "US");
File.WriteAllBytes("translated.xlsx", response);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<highlight java>}}
// Example: Java SDK v22.9
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File response = cellsApi.cellsAiTranslateSpreadsheet("input.xlsx", "es", "US", null);
Files.write(Paths.get("translated.xlsx"), response);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<highlight php>}}
// Example: PHP SDK v23.3
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->cellsAiTranslateSpreadsheet("input.xlsx", "es", "US");
file_put_contents("translated.xlsx", $response);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<highlight ruby>}}
# Example: Ruby SDK v22.5
cells_api = AsposeCellsCloud::API::CellsApi.new(client_id, client_secret)
response = cells_api.cells_ai_translate_spreadsheet("input.xlsx", target_language: "es", region: "US")
File.write("translated.xlsx", response)
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<highlight typescript>}}
// Example: Node.js SDK v24.2
const { CellsApi } = require("@aspose/cells-cloud");
const cellsApi = new CellsApi(process.env.CLIENT_ID, process.env.CLIENT_SECRET);
const response = await cellsApi.cellsAiTranslateSpreadsheet("input.xlsx", "es", "US");
await fs.promises.writeFile("translated.xlsx", response);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<highlight python>}}
# Example: Python SDK v22.10
from asposecellscloud.api import CellsApi
cells_api = CellsApi(client_id, client_secret)
response = cells_api.cells_ai_translate_spreadsheet("input.xlsx", target_language="es", region="US")
with open("translated.xlsx", "wb") as f:
    f.write(response)
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<highlight perl>}}
# Example: Perl SDK v22.4
my $api = AsposeCellsCloud::API::CellsApi->new(
    -client_id => $client_id,
    -client_secret => $client_secret
);
my $response = $api->cells_ai_translate_spreadsheet("input.xlsx", "es", "US");
open my $fh, '>', "translated.xlsx";
print $fh $$response;
close $fh;
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<highlight go>}}
// Example: Go SDK v24.1
api := cells.NewCellsApi(os.Getenv("CLIENT_ID"), os.Getenv("CLIENT_SECRET"))
response, _, err := api.CellsAiTranslateSpreadsheet(context.Background(), "input.xlsx", "es", "US", nil)
os.WriteFile("translated.xlsx", response, 0644)
{{</highlight>}}  
{{</tab>}}  
{{< /tabs >}}

## API Specification & Testing

- **Interactive Swagger UI**: Test the API directly in your browser using the [Translate Spreadsheet OpenAPI spec](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet).  
- **Postman Collection**: Import the [Aspose.Cells Cloud Postman collection](https://github.com/aspose-cells-cloud/aspose-cells-cloud-postman) for reusable request templates.

## Related Documentation

- [How to Save Excel to PDF](/save-as/)  
- [Merge Multiple Spreadsheets](/merge-spreadsheets/)  
- [Compare Two Excel Files](/compare/)  
- [Cloud Authentication Guide](https://docs.aspose.com/cells-cloud/Authentication/)

## Troubleshooting

| Issue | Resolution |
|:------|:-----------|
| `400 Bad Request` with "Invalid targetLanguage" | Verify language code against [supported languages](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/language-support). |
| `401 Unauthorized` | Regenerate JWT token using valid `Client ID`/`Secret` and ensure it hasn’t expired (typically 24h). |
| `500 Internal Server Error` | Check [Service Health Dashboard](https://status.aspose.cloud/) for translation service outages. |
| Formatted numbers/dates misaligned | Specify `region` parameter (e.g., `"US"` or `"EU"`) to enforce locale-aware formatting. |