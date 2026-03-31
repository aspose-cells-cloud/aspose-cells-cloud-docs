---  
title: "Ungroup Columns in an Excel Worksheet – Aspose.Cells Cloud API"  
second_title: "Document"  
linktitle: "Ungroup"  
type: docs  
url: /columns/ungroup/  
aliases:  
  - /ungroup-columns-in-an-excel-worksheet/  
  - /ungroup-columns-in-excel-worksheet/  
keywords: "Aspose.Cells, ungroup columns, Excel API, REST, SDK"  
description: "Learn how to ungroup columns in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, authentication, cURL example, and SDK code snippets for C#, Java, Python, and more."  
weight: 70  
---  

The **Ungroup Columns** REST API removes column grouping in a worksheet.

## Prerequisites  

1. Create an Aspose Cloud account.  
2. Generate a **Client ID** and **Client Secret**.  
3. Obtain an OAuth 2.0 access token (`Authorization: Bearer <access_token>`).  
4. Upload the target workbook to Aspose Cloud storage (or reference an existing file).

## Authentication  

All Aspose.Cells Cloud endpoints require an OAuth 2.0 bearer token.  
Include the following header in every request:

```http
Authorization: Bearer <access_token>
```

You can acquire a token by calling the OAuth 2.0 token endpoint with your client credentials.  
(See the **Authentication** guide in the main documentation for the exact request.)

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

The request parameters are:

| Parameter Name | Type    | Location | Description                                                    |
|----------------|---------|----------|----------------------------------------------------------------|
| name           | string  | path     | The workbook name.                                             |
| sheetName      | string  | path     | The worksheet name.                                            |
| firstIndex     | integer | query    | Zero‑based index of the first column to be ungrouped.          |
| lastIndex      | integer | query    | Zero‑based index of the last column to be ungrouped.           |
| folder         | string  | query    | Path to the folder containing the workbook.                    |
| storageName    | string  | query    | Name of the storage service.                                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** to call the API. The example below includes the required authentication header.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

*On error the service returns a JSON object containing `Code`, `Status`, and `ErrorMessage` fields (e.g., 400 Bad Request, 401 Unauthorized).*

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family  

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details, letting you focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ  

**Q:** *How do I ungroup columns in a worksheet using Aspose.Cells Cloud?*  
**A:** Call the `POST /cells/{name}/worksheets/{sheetName}/cells/columns/ungroup` endpoint, providing the workbook name, worksheet name, and the zero‑based `firstIndex` and `lastIndex` of the columns to ungroup. Include the `Authorization: Bearer <access_token>` header. See the cURL example above.

**Q:** *What response will I receive after a successful ungroup request?*  
**A:** A JSON object containing at least `Code` (200), `Status` (“OK”), and a `Columns` object that echoes the `firstIndex` and `lastIndex` values. Error responses include an `ErrorMessage` field and the appropriate HTTP status code.

**Q:** *Which SDKs can I use to call the Ungroup Columns API?*  
**A:** Aspose.Cells Cloud provides SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go. Each SDK offers a method such as `PostUngroupWorksheetColumns` that abstracts the HTTP call. Sample code for each language is shown in the **Cloud SDK Family** section.  

---  

*Version note: This documentation targets API version **v3.0**. Future releases may introduce breaking changes; consult the “Version History” page for details.*