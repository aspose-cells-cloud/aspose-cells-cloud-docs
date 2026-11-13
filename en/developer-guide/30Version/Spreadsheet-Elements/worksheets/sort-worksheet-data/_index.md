---
title: "Sort Data of Range on an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Sort"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, Excel sort API, worksheet range sorting, REST API, dataSorter"
description: "Sort Excel worksheet range data using Aspose.Cells Cloud REST API with specified cell area and dataSorter configuration."
weight: 100
ArticleTitle: "Sort Excel Worksheet Range Data with Aspose.Cells Cloud REST API"
---
The **PostWorksheetRangeSort** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort`) enables sorting data within a specified range on an Excel worksheet using Aspose.Cells Cloud. It requires the file name, worksheet name, cell area to sort, and a DataSorter object in the request body, with optional folder and storage parameters. This operation supports complex sorting scenarios such as multi-column, case-sensitive, and custom list sorting, making it suitable for programmatic data organization in cloud-based Excel workflows.

## The Post Worksheet Range Sort Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| cellArea | String | Query | The area needed to sort. |
| dataSorter | class:datasorter | HTTPBody | DataSorter with sorting settings. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**`dataSorter` object schema** – The body must contain a JSON object with the following properties:

- `CaseSensitive` _(boolean, required)_ – Determines whether the sort is case‑sensitive.
- `HasHeaders` _(boolean, required)_ – Indicates whether the range includes a header row.
- `KeyList` _(array, required)_ – A collection of sorting keys. Each key object includes:
  - `Key` _(integer)_ – Zero‑based column index.
  - `SortOrder` _(string)_ – `"ascending"` or `"descending"`.
- `SortLeftToRight` _(boolean, required)_ – If `true`, sorting proceeds left‑to‑right; otherwise top‑to‑bottom.
- _(Optional)_ `CaseOrder`, `SortLeftToRight`, etc., may also be supplied according to the OpenAPI specification.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Error handling** – The API can return standard HTTP error codes. Typical responses include:

| HTTP Status | Code | Message                                           |
| ----------- | ---- | ------------------------------------------------- |
| 400         | 400  | Bad request – missing or invalid parameters.      |
| 401         | 401  | Unauthorized – invalid or absent JWT token.       |
| 404         | 404  | Not found – workbook or worksheet does not exist. |
| 500         | 500  | Internal server error.                            |

The response body follows the pattern `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` for error cases.

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
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

## How to Use the Post Worksheet Range Sort API with SDKs?

### Post Worksheet Range Sort API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort" rel="noopener noreferrer">Post Worksheet Range Sort API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetRangeSort.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetRangeSort.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetRangeSort.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetRangeSort.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetRangeSort.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetRangeSort.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetRangeSort.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetRangeSort.go" >}}
{{</tab>}}
{{< /tabs >}}
