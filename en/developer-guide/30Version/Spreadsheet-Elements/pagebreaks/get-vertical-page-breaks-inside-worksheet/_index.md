---  
title: "Get Vertical Page Breaks"  
second_title: "Document"  
linktitle: "Get Vertical Page Breaks"  
type: docs  
url: /page-breaks/get-vertical-page-breaks/  
aliases: [/get-vertical-page-breaks-inside-worksheet/]  
keywords: "Aspose.Cells, vertical page breaks, Excel API, cloud spreadsheet, REST API"  
description: "Retrieve vertical page breaks from an Excel worksheet using the Aspose.Cells Cloud REST API (v3.0). Includes HTTPS endpoint, required parameters, cURL example, response details, error handling, and SDK samples."  
weight: 20  
---  

This REST API retrieves **vertical** page breaks from a worksheet.

## Rest Api  

### Prerequisites  

1. **Authentication** – Obtain a JWT token via the Aspose Cloud OAuth endpoint (`/connect/token`).  
2. **Storage configuration** – Ensure the workbook is stored in Aspose Cloud storage (default is the root folder).  
3. **API version** – This documentation applies to API version **v3.0**.  

### Quick‑Start  

1. Get a JWT token.  
2. Upload the Excel file to the desired storage folder (if it is not already there).  
3. Call the endpoint shown below.  
4. Parse the JSON response to read the `VerticalPageBreakList`.  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

The request parameters for this endpoint are:

| Parameter Name | Type   | Location | Description                                           | Required |
|----------------|--------|----------|-------------------------------------------------------|----------|
| `name`         | string | path     | The name of the Excel file.                           | Yes |
| `sheetName`    | string | path     | The name of the worksheet from which to read breaks. | Yes |
| `folder`       | string | query    | The folder in storage that contains the file.         | No |
| `storageName`  | string | query    | The name of the Aspose Cloud storage to use.          | No |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Details  

| Field                     | Type   | Description                                                                    |
|---------------------------|--------|--------------------------------------------------------------------------------|
| `VerticalPageBreakList`   | array  | A collection of vertical page‑break objects.                                   |
| `Column`                  | int    | The column index (zero‑based) where the break occurs.                          |
| `StartRow`                | int    | The first row of the break range (zero‑based).                                 |
| `EndRow`                  | int    | The last row of the break range (zero‑based, typically `1048575` for the last row). |
| `link.Href`               | string | Self‑referencing URL for the resource (HTTPS).                                 |
| `Code`                    | int    | HTTP status code returned by the service.                                      |
| `Status`                  | string | Textual description of the HTTP status.                                        |

### Error Handling  

| HTTP Code | Meaning                           | Typical Cause                                 |
|-----------|-----------------------------------|----------------------------------------------|
| 401       | Unauthorized                      | Missing or invalid JWT token.               |
| 404       | Not Found                         | Specified file or worksheet does not exist. |
| 400       | Bad Request                       | Invalid or malformed query parameters.      |
| 500       | Internal Server Error             | Unexpected server‑side condition.           |

Check the `Code` and `Status` fields in the JSON response for additional details.

### Version / Change Log  

This page documents **v3.0** of the Aspose.Cells Cloud API. For newer versions and change‑log details, see the [API changelog](/cells/changelog).

## Cloud SDK Family  

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details so you can focus on your business logic. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}