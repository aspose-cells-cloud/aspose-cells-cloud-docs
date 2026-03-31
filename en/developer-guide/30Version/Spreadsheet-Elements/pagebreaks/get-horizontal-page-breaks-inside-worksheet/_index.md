---  
title: "Get Horizontal Page Breaks"  
second_title: "Document"  
linktitle: "Get Horizontal Page Breaks"  
type: docs  
url: /page-breaks/get-horizontal-page-breaks/  
aliases: [/get-horizontal-page-breaks-inside-worksheet/]  
keywords: "horizontal page breaks, Aspose.Cells Cloud, REST API, Excel worksheet, SDK"  
description: "Retrieve horizontal page breaks from an Excel worksheet via Aspose.Cells Cloud API. Includes endpoint, parameters, cURL example, response format, and SDK snippets for C#, Java, Python, and more."  
weight: 10  
---  

**Horizontal page break** – a row‑based break that forces the worksheet to start a new printed page after the specified row. This REST API retrieves those horizontal page breaks.

## Prerequisites  

Before calling the endpoint you must:

* **Obtain a JWT token** – see the **Authentication** guide for details on generating a token with the required scopes. Include the token in the `Authorization: Bearer <jwt token>` header.  
* **Configure storage** – ensure the Excel file is stored in Aspose Cloud storage (default or a custom storage name).  

## REST API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```  

The request parameters are:

| Parameter Name | Type   | Location | Description                                                                 |
|----------------|--------|----------|-----------------------------------------------------------------------------|
| name           | string | path     | The name of the Excel file.                                                |
| sheetName      | string | path     | The name of the worksheet.                                                |
| folder         | string | query    | The folder path in storage where the file is located. *(optional)*        |
| storageName    | string | query    | The name of the storage. *(optional)*                                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Error Handling  

| HTTP Status | Description                              | Example JSON |
|-------------|------------------------------------------|--------------|
| 400         | Bad request – missing or invalid parameters. | `{ "Code": 400, "Message": "Invalid parameter." }` |
| 401         | Unauthorized – JWT token is missing or invalid. | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | Not found – the specified file or worksheet does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500         | Internal server error – unexpected condition on the server. | `{ "Code": 500, "Message": "Server error." }` |

## Frequently Asked Questions  

**Q:** How do I retrieve horizontal page breaks from a worksheet using Aspose.Cells Cloud?  
**A:** Send a `GET` request to `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/horizontalpagebreaks` with a valid JWT token. The response returns a JSON object containing a `HorizontalPageBreakList` with row numbers and column ranges.

**Q:** What parameters are required for the Get Horizontal Page Breaks API?  
**A:**  
* `name` (path) – Excel file name (required).  
* `sheetName` (path) – Worksheet name (required).  
* `folder` (query) – Storage folder path (optional).  
* `storageName` (query) – Storage name (optional).

**Q:** Which SDKs can I use to call the Get Horizontal Page Breaks API?  
**A:** Aspose.Cells Cloud SDKs are available for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go. Sample code for each language is provided on the page.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}