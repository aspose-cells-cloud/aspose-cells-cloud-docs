---
title: "Merge Multiple Excel Files into a Single Workbook"
second_title: "Document"
linktitle: "Merge Multiple Excel Files"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, merge multiple Excel files, REST API, spreadsheet merge, cloud SDK"
description: "Learn how to merge multiple Excel workbooks into one file using the Aspose.Cells Cloud REST API (v3.0). Includes HTTPS endpoint, cURL command, SDK samples, required parameters, and error‑handling details."
weight: 32
---

## REST API

This REST API merges multiple Excel files into a single Excel workbook.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


### Request parameters

| Parameter Name  | Type    | Location | Description                                                                       | Required |
| --------------- | ------- | -------- | --------------------------------------------------------------------------------- | -------- |
| files[]         | file    | formData | One or more Excel workbooks to be merged. Use `file1`, `file2`, … in the request. | Yes      |
| format          | string  | query    | Desired output format (e.g., `xlsx`).                                             | Yes      |
| mergeToOneSheet | boolean | query    | Set to `true` to combine all worksheets into a single sheet; default is `false`.  | No       |

### **Response**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[merged filename]",
    "Filesize" : [file size],
    "FileContent" : "[Base64String]"
}
```

**Response Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the PostMerge API with SDKs

### PostMerge API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}
