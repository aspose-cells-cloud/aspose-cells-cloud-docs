---
title: "Group rows on an Excel Worksheet"
second_title: "Document"
linktitle: "Group"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "group rows, Excel, Aspose.Cells Cloud, REST API, SDK, worksheet, Excel API"
description: "Group rows in an Excel worksheet using the Aspose.Cells Cloud REST API. Supports multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) for easy integration."
weight: 60
ArticleTitle: "Group Rows in Excel Worksheet using Aspose.Cells Cloud API"
---

This REST API groups rows on an Excel worksheet.

**Prerequisites:**  
- A valid OAuth 2.0 access token (Bearer JWT) must be supplied in the `Authorization` header.  
- The workbook must already exist in the specified `folder` of the chosen `storageName` (or the default storage) before the request is made.

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type    | Location | Description                                                              |
| -------------- | ------- | -------- | ------------------------------------------------------------------------ |
| name           | string  | path     | The name of the workbook file.                                           |
| sheetName      | string  | path     | The name of the worksheet.                                               |
| firstIndex     | integer | query    | Zero‑based index of the first row to be grouped.                         |
| lastIndex      | integer | query    | Zero‑based index of the last row to be grouped.                          |
| hide           | boolean | query    | Indicates whether the grouped rows should be hidden (`true` or `false`). |
| folder         | string  | query    | Path to the folder that contains the workbook.                           |
| storageName    | string  | query    | Name of the storage where the workbook is located.                       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

Typical error responses:

- **400 Bad Request** – check that `firstIndex` and `lastIndex` are valid integers and that `firstIndex` ≤ `lastIndex`.  
- **401 Unauthorized** – verify that the `Authorization` header contains a current JWT token.  
- **404 Not Found** – ensure the workbook (`name`) and worksheet (`sheetName`) exist in the specified `folder`/`storageName`.

{{< /tab >}}

{{< /tabs >}}

**See also:** [Ungroup rows on an Excel worksheet](../rows/ungroup/ "Ungroup rows on an Excel worksheet"), [Hide rows on an Excel worksheet](../rows/hide/ "Hide rows on an Excel worksheet"), [Unhide rows on an Excel worksheet](../rows/unhide/ "Unhide rows on an Excel worksheet").

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}