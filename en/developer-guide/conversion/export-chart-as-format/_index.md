---
title: "Export Excel Chart – Aspose.Cells Cloud API"
second_title: "Document"
description: "Convert a chart from a cloud‑stored Excel workbook to PDF, PNG, SVG or other formats with a single REST call."
ArticleTitle: "How to Convert a Local Spreadsheet Worksheet to a PDF File: Step‑by‑Step Guide"
linktitle: "Convert Worksheet to PDF"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, Export Chart, API, PDF, PNG, SVG, Excel, REST, Cloud Conversion"
weight: 100
---

Convert a chart that resides in a workbook stored in Aspose Cloud Storage to a different file format (PDF, PNG, SVG, …) without downloading the source file.

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### 📦 Request Parameters

| Name               | Type    | Location | Required | Description                                               |
| ------------------ | ------- | -------- | -------- | --------------------------------------------------------- |
| **name**           | string  | Path     | Yes      | Workbook file name.                                       |
| **worksheet**      | string  | Path     | Yes      | Worksheet name that contains the chart.                   |
| **chartIndex**     | integer | Path     | Yes      | Zero‑based index of the chart to export.                  |
| **format**         | string  | Query    | Yes      | Desired output format (e.g., `png`, `pdf`, `svg`).        |
| **folder**         | string  | Query    | No       | Folder path where the workbook is stored (default: root). |
| **storageName**    | string  | Query    | No       | Custom storage name; omit to use the default storage.     |
| **outPath**        | string  | Query    | No       | Folder path where the converted file will be saved.       |
| **outStorageName** | string  | Query    | No       | Storage name for the output file.                         |
| **fontsLocation**  | string  | Query    | No       | Path to a folder that contains custom fonts.              |
| **region**         | string  | Query    | No       | Locale setting (e.g., `en-US`, `fr-FR`).                  |
| **password**       | string  | Query    | No       | Password for opening a protected workbook.                |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## How to Use the Export Chart as Format API with SDKs?

### Export Chart as Format API Specification

The [Export Chart as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) provides a publicly accessible programming interface and enables REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert spreadsheet table data to a PDF file with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:
