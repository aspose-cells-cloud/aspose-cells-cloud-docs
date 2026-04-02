---
title: "Excel to SQL"
second_title: "Document"
linktitle: "Excel to SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Excel to SQL, Aspose.Cells Cloud, REST API, spreadsheet conversion, SQL file, data migration, API integration"
description: "Use Aspose.Cells Cloud REST API to convert Excel spreadsheets into SQL files. Supports multiple SDKs and programming languages for seamless integration into your applications."
weight: 100
---

This REST API converts a spreadsheet file to an SQL format file.

**Query Parameter**

| Parameter Name          | Type   | Description                                                                                 |
|-------------------------|--------|---------------------------------------------------------------------------------------------|
| password                | string | Password required to open the Excel file.                                                   |
| storageName             | string | Name of the storage where the file is stored.                                                |
| checkExcelRestriction   | bool   | Indicates whether to check Excel file restrictions when modifying cell‑related objects.   |

**Request Body Parameter**

| Parameter Name | Type      | Description                                                                      |
|----------------|-----------|----------------------------------------------------------------------------------|
| datafile       | data file | The spreadsheet file to be converted, included as the first part of the request. |

**Response**

[FileInfo](/cells/file-info/)

## REST API Specification

| **API**                | **Type** | **Description**                         | **Swagger Link**                                                                 |
|------------------------|----------|-----------------------------------------|-----------------------------------------------------------------------------------|
| /cells/convert/sql     | POST     | Convert a spreadsheet to an SQL file.   | [PostConvertWorkbookToSQL](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.json",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs Implementing This Function

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Saves a workbook in a different format and stores the result in the specified storage.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converts a workbook to another format with optional settings and returns the result in the response.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Retrieves a workbook with optional conversion settings.