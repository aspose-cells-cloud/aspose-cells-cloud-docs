---
title: "Add an empty row on an Excel worksheet"
ArticleTitle: "Add an empty row to an Excel worksheet using Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, add empty row, worksheet, REST API, insert row, cloud spreadsheet"
description: "Use Aspose.Cells Cloud REST API to insert an empty row into an Excel worksheet. Supports multiple SDKs (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) for rapid development."
weight: 20
---

This REST API adds a new row to an Excel worksheet. It inserts an empty row at the specified zero‑based index.

**Prerequisites:**  
- A valid Aspose Cloud access token (Bearer JWT) must be included in the `Authorization` header.  
- The target workbook must be uploaded to your Aspose Cloud storage, and the `folder` and `storageName` parameters should point to its location.

**Notes:**  
- The `rowIndex` is zero‑based; inserting at index 0 adds a row at the top of the worksheet.  
- Excel worksheets have a maximum of 1,048,576 rows; attempting to insert beyond this limit will result

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type    | Location | Description                                              |
| -------------- | ------- | -------- | -------------------------------------------------------- |
| name           | string  | path     | The workbook file name.                                  |
| sheetName      | string  | path     | The worksheet name.                                      |
| rowIndex       | integer | path     | The zero‑based index where the new row will be inserted. |
| folder         | string  | query    | The folder path in storage that contains the workbook.   |
| storageName    | string  | query    | The name of the Aspose Cloud storage to use.             |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Note:** All Aspose.Cells Cloud endpoints require HTTPS. Use the secure `https://` scheme for production calls.

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

*Example of an error response (e.g., when the row index exceeds the worksheet limit):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Row index out of range. Maximum rows allowed: 1048576."
}
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}