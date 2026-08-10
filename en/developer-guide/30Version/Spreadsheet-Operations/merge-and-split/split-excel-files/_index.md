---
title: "Split an Excel workbook into multiple files"
ArticleTitle: "How to Split an Excel Workbook into Multiple Files using Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Split an Excel file"
type: docs
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, REST API, split workbook, multiple files, JPEG, PNG, PDF, CSV, JSON"
description: "The Aspose.Cells Cloud REST API enables splitting an Excel workbook into multiple files in various formats. This documentation provides request parameters, a cURL example, and SDK code samples for languages such as C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."
weight: 130
---

This REST API splits an Excel **workbook** into multiple files in different formats.

> **Prerequisites** – To use this API you must obtain a valid JWT token, ensure you are using a supported SDK version, and verify that your workbook is stored in a supported storage location. The API also enforces file‑size limits that are documented in the platform guidelines.

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name       | Type    | Location | Description                                                                                     | Required |
| -------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------- | -------- |
| files[]              | file    | formData | One or more Excel workbooks to be **split**. Use `file1`, `file2`, … in the request.          | Yes      |
| format               | string  | Query    | Desired output format for the split files.                                                     | No       |
| from                 | integer | Query    | Starting worksheet index.                                                                       | No       |
| to                   | integer | Query    | Ending worksheet index.                                                                         | No       |
| horizontalResolution | integer | Query    | Image horizontal resolution.                                                                    | No       |
| verticalResolution   | integer | Query    | Image vertical resolution.                                                                      | No       |
| outFolder            | string  | Query    | Output folder for the split files.                                                              | No       |
| splitNameRule        | string  | Query    | Naming rule applied to split files.                                                             | No       |
| folder               | string  | Query    | Folder containing the original workbook.                                                        | No       |
| storageName          | string  | Query    | Name of the storage to use.                                                                     | No       |

### **Response**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[file1 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file2 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file3 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      }
    ]
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
## How to Use the PostWorkbookSplit API with SDKs

### PostWorkbookSplit API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}