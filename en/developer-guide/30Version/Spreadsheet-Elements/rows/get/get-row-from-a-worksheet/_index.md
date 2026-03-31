---  
title: "Get Row Description from an Excel Worksheet"  
second_title: "Document"  
linktitle: "Row"  
type: docs  
url: /rows/get/row/  
aliases: [/get-row-from-a-worksheet/]  
keywords: "Aspose.Cells Cloud, Excel row API, Get Worksheet Row, REST API, .NET SDK, Java SDK, Python SDK"  
description: "Retrieve detailed information (height, style, hidden state, etc.) for a specific row in an Excel worksheet using Aspose.Cells Cloud REST API. Includes curl example, SDK snippets, and error handling."  
weight: 10  
---  

This REST API retrieves row data by its index on an Excel worksheet.

## REST API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```  

The request parameters are:

| Parameter Name | Type    | Location | Description                                    |
|----------------|---------|----------|------------------------------------------------|
| name           | string  | path     | The name of the workbook file.                 |
| sheetName      | string  | path     | The name of the worksheet within the workbook. |
| rowIndex       | integer | path     | Zero‑based index of the row to retrieve.       |
| folder         | string  | query    | The folder that contains the workbook.         |
| storageName    | string  | query    | The name of the storage where the workbook resides. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL. Include the `Authorization: Bearer <jwt token>` header to authenticate the request.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family  

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}