---
title: "Apply Rich Text Formatting to a Cell"
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, rich text, cell formatting, REST API, Aspose.Cells Cloud"
description: "Learn how to apply rich text formatting to a specific Excel cell using the Aspose.Cells Cloud REST API. Includes request syntax, parameter details, cURL example, and SDK snippets."
ArticleTitle: "Apply Rich Text Formatting to a Cell using Aspose.Cells Cloud API"
---

## REST API

This REST API applies **rich text formatting** to a cell in an Excel file.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type   | Location                     | Description                                                                 |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| name           | string | path                         | The name of the Excel file (e.g., `Book1.xlsx`).                           |
| sheetName      | string | path                         | The worksheet that contains the target cell.                               |
| cellName       | string | path                         | The address of the cell to format (e.g., `A1`).                            |
| options        | object | body                         | JSON object that defines the rich‑text formatting settings for the cell. |
| folder         | string | query                        | The folder in storage where the Excel file is located.                     |
| storageName    | string | query                        | The name of the storage service (if a custom storage is used).            |

### **Response**

```json
{
    "Status":"OK",
    "Code":200
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


## How to Use the PostCellCharacters API with SDKs

### PostCellCharacters API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*C# SDK example*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Java SDK example*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*PHP SDK example*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ruby SDK example*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Node.js SDK example*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Python SDK example*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Perl SDK example*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Go SDK example*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
