---  
title: "Sort Data of Range on an Excel Worksheet"  
second_title: "Document"  
linktitle: "Sort"  
type: docs  
url: /worksheets/sort-data/  
aliases: [/sort-worksheet-data/]  
keywords: "Aspose.Cells Cloud, Excel sort API, worksheet range sorting, REST API, dataSorter"  
description: "Sort a specific range in an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint, required parameters, authentication steps, error handling, and SDK examples."  
weight: 20  
---  

The REST API sorts data within a specified range on an Excel worksheet.

## REST API  

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

**Authentication** – The request must include a valid Bearer token obtained through the Aspose Cloud OAuth 2.0 flow. Add the token to the `Authorization` header:

```
Authorization: Bearer <jwt token>
```

**Security** – Always use HTTPS; the example URLs have been updated accordingly.

### Request parameters  

| Parameter Name | Type   | Location | Required | Description |
|----------------|--------|----------|----------|-------------|
| name           | string | path     | Yes      | The workbook name. |
| sheetName      | string | path     | Yes      | The worksheet name. |
| cellArea       | string | query    | Yes      | The cell range to be sorted (e.g., `A5:A10`). |
| dataSorter     | object | body     | Yes      | JSON object that defines the sorting settings (see schema below). |
| folder         | string | query    | No       | The folder that contains the workbook. |
| storageName    | string | query    | No       | The name of the storage where the workbook is located. |

**`dataSorter` object schema** – The body must contain a JSON object with the following properties:

- `CaseSensitive` *(boolean, required)* – Determines whether the sort is case‑sensitive.  
- `HasHeaders` *(boolean, required)* – Indicates whether the range includes a header row.  
- `KeyList` *(array, required)* – A collection of sorting keys. Each key object includes:  
  - `Key` *(integer)* – Zero‑based column index.  
  - `SortOrder` *(string)* – `"ascending"` or `"descending"`.  
- `SortLeftToRight` *(boolean, required)* – If `true`, sorting proceeds left‑to‑right; otherwise top‑to‑bottom.  
- *(Optional)* `CaseOrder`, `SortLeftToRight`, etc., may also be supplied according to the OpenAPI specification.

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

| HTTP Status | Code | Message                              |
|-------------|------|--------------------------------------|
| 400         | 400  | Bad request – missing or invalid parameters. |
| 401         | 401  | Unauthorized – invalid or absent JWT token. |
| 404         | 404  | Not found – workbook or worksheet does not exist. |
| 500         | 500  | Internal server error. |

The response body follows the pattern `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` for error cases.

## Cloud SDK Family  

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}