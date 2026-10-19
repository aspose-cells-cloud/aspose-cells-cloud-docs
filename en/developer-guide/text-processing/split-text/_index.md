---
title: "Split Text API – Segment Excel Cells into Columns | Aspose.Cells Cloud"
secondtitle: "Developer Guide"
linktitle: "Split Text"
url: /split-text/
keywords: "Aspose, Cells, Split Text API, Excel, delimiter, text segmentation, cloud API"
description: "Split Excel cell text by delimiter, mask, or line break using Aspose.Cells Cloud REST API. Supports XLSX, ODS, CSV; keep/drop delimiters; output to rows/columns."
summary: "Use the Split Text API to segment Excel cell content by custom delimiters, masks, or line breaks. Ideal for cleaning ERP/CRM imports, legacy data exports, and semi-structured logs."
type: docs
weight: 100
---

Segment Excel cell text into multiple columns or rows using custom segmentation rules. Split content by delimiter, mask, or line break, and output results to a specified range using the Aspose.Cells Cloud Text Processing API.

## Introduction

The Split Text API divides cell contents into multiple cells based on specified delimiters, patterns, or line breaks, and writes the results to a target range. It supports flexible splitting methods, directional output (columns or rows), and configurable delimiter handling—ideal for parsing concatenated data, CSV-style content, or multiline text into structured formats.

### Core Capabilities

- **Split by specific characters** – break down cell content using any character as a separator (e.g., comma, semicolon, space, tab, pipe).
- **Split by string combinations** – separate cells using multi-character delimiters (e.g., `||`, `->`, `; `).
- **Split by pattern mask** – use wildcards to segment text based on structured patterns (e.g., `###-AAA-**`).
- **Split by line break** – parse multiline cell content into separate rows (e.g., addresses, comments, notes).
- **Output direction** – choose between `SplitToColumns` or `SplitToRows`.
- **Delimiter handling** – optionally retain delimiters at the beginning, end, before, or after the split text.

## Prerequisites

- A valid [Aspose Cloud access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for JWT-based authentication.
- A spreadsheet file uploaded to Aspose Cloud storage or sent directly in the request body.
- Supported formats: XLSX, XLS, ODS, CSV.

## REST API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/split/text
```

### Authentication

Include your JWT token in the `Authorization` header:

```bash
-H "Authorization: Bearer {access_token}"
```

> **Note**: All requests must use HTTPS. The authentication endpoint enforces TLS 1.2+.

## Request Parameters

| Parameter Name                   | Type    | Location | Required | Default          | Description                                                                                                    |
| -------------------------------- | ------- | -------- | -------- | ---------------- | -------------------------------------------------------------------------------------------------------------- | ------------------- |
| `spreadsheet`                    | File    | FormData | Yes      | —                | The spreadsheet file to process (XLSX, XLS, ODS, CSV).                                                         |
| `delimiters`                     | String  | Query    | Yes      | —                | One or more delimiter characters (e.g., `","`, `";"`, `"                                                       | "`, `" "`, `"\n"`). |
| `keepDelimitersInResultingCells` | Boolean | Query    | No       | `false`          | When `true`, delimiters are retained in the resulting cells.                                                   |
| `keepDelimitersPosition`         | String  | Query    | No       | `None`           | Where to retain delimiters if enabled: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`.        |
| `howToSplit`                     | String  | Query    | No       | `SplitToColumns` | Direction of output: `None`, `SplitToColumns`, `SplitToRows`.                                                  |
| `outPositionRange`               | String  | Query    | Yes      | —                | Target range for output (e.g., `` `"D1:F10"` ``).                                                              |
| `worksheet`                      | String  | Query    | No       | First sheet      | Worksheet name where splitting is applied.                                                                     |
| `range`                          | String  | Query    | No       | Used range       | Source cell range to split (e.g., `` `"A1:A10"` ``).                                                           |
| `outPath`                        | String  | Query    | No       | Source folder    | Cloud storage path to save the output workbook.                                                                |
| `outStorageName`                 | String  | Query    | No       | Default          | Name of the cloud storage for output.                                                                          |
| `region`                         | String  | Query    | No       | `en-US`          | Locale setting (e.g., `"en-US"`, `"de-DE"`, `"ja-JP"`). Affects delimiter interpretation and formatting rules. |
| `password`                       | String  | Query    | No       | —                | Password for password-protected workbooks.                                                                     |

### Notes on Key Parameters

- **`delimiters`**: Accepts single characters or strings (e.g., `"|"`, `"::"`, `"\r\n"`). Multiple delimiters are supported as a concatenated string (e.g., `",;"` splits on both comma and semicolon).
- **`region`**: Influences locale-specific behavior (e.g., in `de-DE`, semicolon is often used as a list separator instead of comma). Example: `"fr-FR"` treats comma as decimal separator and space as thousands separator.
- **`outPositionRange`**: Must be a valid Excel range (e.g., `` `"B2:E100"` ``). The API writes results starting at the top-left cell and expands right (columns) or down (rows) as needed.

## Example Request

### cURL Example

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/content/split/text?delimiters=%2C&howToSplit=SplitToColumns&outPositionRange=D1%3AF10&worksheet=Sheet1&range=A1%3AA5' \
  -H 'Authorization: Bearer <your_access_token>' \
  -H 'Content-Type: multipart/form-data' \
  -F 'spreadsheet=@input.xlsx' \
  -o output.xlsx
```

### SDK Examples (Selected)

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<highlight csharp>}}
// C# example: Split text in column A by comma into columns D–F
var cellsApi = new CellsApi(clientId, clientSecret);
cellsApi.SplitText(
"input.xlsx",
delimiters: ",",
howToSplit: "SplitToColumns",
outPositionRange: "D1:F10",
worksheet: "Sheet1",
range: "A1:A5"
);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<highlight java>}}
// Java example: Split multiline text in A1:A10 into rows starting at B1
SplitTextRequest request = new SplitTextRequest();
request.setDelimiters("\n");
request.setHowToSplit("SplitToRows");
request.setOutPositionRange("B1");
request.setWorksheet("Sheet1");
request.setRange("A1:A10");
cellsApi.splitText(request, "input.xlsx", null, null);
{{</highlight>}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<highlight python>}}

# Python example: Split by pipe delimiter, retain at end, write to rows

api = CellsApi(os.getenv('ASPOSE_CLOUD_CLIENT_ID'), os.getenv('ASPOSE_CLOUD_CLIENT_SECRET'))
api.split_text(
file='input.xlsx',
delimiters='|',
how_to_split='SplitToRows',
out_position_range='C1:E10',
worksheet='Data',
range='A1:A8',
keep_delimiters_in_resulting_cells=True,
keep_delimiters_position='AtTheEnd'
)
{{</highlight>}}  
{{</tab>}}  
{{</tabs>}}

> **Tip**: Use [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud) for battle-tested, language-native integration.

## Response

The API returns the modified workbook as a binary stream (file download):

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="output.xlsx"
```

### Error Codes

| Code                         | Description                                                                |
| ---------------------------- | -------------------------------------------------------------------------- |
| `400 Bad Request`            | Invalid parameter format (e.g., malformed range, missing required fields). |
| `401 Unauthorized`           | Missing, expired, or invalid JWT token.                                    |
| `403 Forbidden`              | Insufficient permissions or quota exceeded.                                |
| `404 Not Found`              | Spreadsheet file not found in storage or invalid path.                     |
| `415 Unsupported Media Type` | File format not supported (e.g., .xlsx required).                          |
| `500 Internal Server Error`  | Unexpected server-side failure during processing.                          |

## OpenAPI Specification

The full API contract is documented in the [Aspose.Cells Cloud OpenAPI spec](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText).
