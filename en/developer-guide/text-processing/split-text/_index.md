---
title: "Split Text API – Segment Excel Cells into Columns | Aspose.Cells Cloud"
secondtitle: "Developer Guide"
linktitle: "Split Text"
url: /split-text/
keywords: "Aspose, Cells, Split Text API, Excel, delimiter, text segmentation, cloud API"
description: "Split Excel cell text by delimiter, mask, or line break into columns or rows using Aspose.Cells Cloud REST API."
summary: "Use the Split Text API to segment Excel cell content by custom delimiters, masks, or line breaks. Ideal for cleaning ERP/CRM imports, legacy data exports, and semi-structured logs."
type: docs
weight: 100
ArticleTitle: "Split Excel Text by Delimiter, Mask, or Line Break | Aspose.Cells Cloud API"
---
The **SplitText** API (`PUT https://api.aspose.cloud/v4.0/cells/content/split/text`) in Aspose.Cells Cloud enables precise text segmentation within Excel workbooks by splitting cell content using custom delimiters, line breaks, or pattern masks, then outputting results to a specified range in columns or rows; for example, users can split a cell’s comma-separated values into adjacent columns while optionally retaining or removing the delimiters.

## Overview

The Split Text API divides cell contents into multiple cells based on specified delimiters, patterns, or line breaks, and writes the results to a target range. It supports flexible splitting methods, directional output (columns or rows), and configurable delimiter handling—ideal for parsing concatenated data, CSV-style content, or multiline text into structured formats.

### Core Capabilities

- **Split by specific characters** – break down cell content using any character as a separator (e.g., comma, semicolon, space, tab, pipe).
- **Split by string combinations** – separate cells using multi-character delimiters (e.g., `||`, `->`, `; `).
- **Split by pattern mask** – use wildcards to segment text based on structured patterns (e.g., `###-AAA-**`).
- **Split by line break** – parse multiline cell content into separate rows (e.g., addresses, comments, notes).
- **Output direction** – choose between `SplitToColumns` or `SplitToRows`.
- **Delimiter handling** – optionally retain delimiters at the beginning, end, before, or after the split text.

## The Split Text Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/split/text
```

### Authentication

Include your JWT token in the `Authorization` header:

```bash
-H "Authorization: Bearer {access_token}"
```

> **Note**: All requests must use HTTPS. The authentication endpoint enforces TLS 1.2+.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| delimiters | String | Query | Indicates the custom delimiter. |
| keepDelimitersInResultingCells | Boolean | Query | Indicates keep delimiters in resulting cells. |
| keepDelimitersPosition | String | Query | Indicates keep delimiters position. |
| HowToSplit | String | Query | Indicates |
| outPositionRange | String | Query | Indicates split delimiters type. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

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
