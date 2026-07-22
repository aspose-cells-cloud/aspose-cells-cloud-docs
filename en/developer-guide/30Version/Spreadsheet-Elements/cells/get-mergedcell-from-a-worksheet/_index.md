---
title: "Get Merged Cells from an Excel Worksheet – Aspose.Cells Cloud API"
type: docs
url: /get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, merged cells, Excel worksheet, REST API, Aspose.Cells SDK, Excel merged cells"
description: "Learn how to retrieve merged‑cell ranges from an Excel worksheet using Aspose.Cells Cloud API (v3.0). Includes authentication steps, full cURL request, response schema, error handling, and SDK examples in C#, Java, Python, and more."
---

This REST API returns information about **merged cells** in an Excel worksheet.

> **Note** – The API object is called **MergedCell** (singular). In the prose we refer to the *concept* of merged cells (plural).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request parameters

| Parameter Name | Type   | Location | Description                         |
|----------------|--------|----------|-------------------------------------|
| **name**       | string | path     | The Excel file name.                |
| **sheetName**  | string | path     | The worksheet name.                 |
| **folder**     | string | query    | Folder that contains the document.  |
| **storageName**| string | query    | Name of the storage to use.         |

## **Response**

Return MergedCellsResponse.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```
**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the GetWorksheetMergedCells API with SDKs

### GetWorksheetMergedCells API Specification


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop against the API. An SDK handles low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}