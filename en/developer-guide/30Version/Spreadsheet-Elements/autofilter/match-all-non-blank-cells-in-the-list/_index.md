---
title: "Match all non‑blank cells in an Excel worksheet"
second_title: "Document"
linktitle: "Match all non‑blank cells"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, match non‑blank cells, AutoFilter, Excel API"
description: "Learn how to use Aspose.Cells Cloud REST API to match all non‑blank cells in an AutoFilter list on an Excel worksheet. Includes endpoint, parameters, authentication, response schema, error codes, and SDK examples."
ArticleTitle: "Match all non‑blank cells in an Excel worksheet using Aspose.Cells Cloud API"
weight: 100
---

**Overview**  
The *Match all non‑blank cells* operation applies an AutoFilter to a worksheet and returns only the rows where the specified column contains data, ignoring empty cells. This is useful for cleaning data sets, generating reports, or preparing data for further analysis.

**Prerequisites**  
- A valid JWT token for Aspose.Cells Cloud authentication.  
- The workbook must be uploaded to Aspose Cloud storage.  
- You need the file name, worksheet name, and the zero‑based column index (`fieldIndex`) you wish to filter.

This REST API matches all non‑blank cells in the AutoFilter list on an Excel worksheet.

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Location | Description                                                    |
| -------------- | ------- | -------- | -------------------------------------------------------------- |
| name           | string  | path     | The name of the Excel file.                                    |
| sheetName      | string  | path     | The name of the worksheet that contains the AutoFilter.        |
| fieldIndex     | integer | query    | Zero‑based index of the column to which the filter is applied. |
| folder         | string  | query    | _(Optional)_ Folder path where the file is stored.             |
| storageName    | string  | query    | _(Optional)_ Name of the storage service to use.               |

### **Response**

```json
{
    "Status":"OK",
    "Code":200
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

*Example error response (400)*  

```json
{
  "Code": 400,
  "Message": "Invalid parameter: fieldIndex must be a non‑negative integer."
}
```

## How to Use the PostWorksheetMatchNonBlanks API with SDKs

### PostWorksheetMatchNonBlanks API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}