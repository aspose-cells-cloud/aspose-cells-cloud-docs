---
title: "Excel to CSV"
second_title: "Document"
linktitle: "Excel to CSV"
type: docs
url: convert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel to CSV, Aspose.Cells Cloud, REST API, spreadsheet conversion, CSV file, file conversion"
description: "Convert Excel spreadsheets to CSV using the Aspose.Cells Cloud REST API. Supports multiple SDKs and programming languages for easy integration."
weight: 90
---

This REST API converts a spreadsheet file to a CSV‑format file.

### Query Parameters

| Parameter Name          | Type   | Description                                                                                         |
|-------------------------|--------|-----------------------------------------------------------------------------------------------------|
| `password`              | string | The password required to open the Excel file.                                                       |
| `storageName`           | string | The name of the storage where the file is located.                                                  |
| `checkExcelRestriction`| bool   | Whether to check Excel file restrictions when the user modifies cell‑related objects.             |

### Request Body Parameter

| Parameter Name | Type      | Description                                                               |
|----------------|-----------|---------------------------------------------------------------------------|
| `datafile`     | data file | The data file included in the first part of the multipart request body. |

### Response

[FileInfo](/cells/file-info/)

## REST API Specification

| API                         | Type | Description                         | Swagger Link |
|-----------------------------|------|-------------------------------------|--------------|
| `/cells/convert/csv`        | POST | Convert a spreadsheet to a CSV file.| [PostConvertWorkbookToCSV](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs Implementing This Function

- **POST** `/cells/{name}/saveAs` – Save an Excel file as a CSV file with additional settings and store the result in a storage location.  
  [API reference](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)

- **PUT** `/cells/convert` – Convert an Excel file to CSV with extra options and return the result directly in the response.  
  [API reference](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)

- **GET** `/cells/{name}` – Retrieve an Excel workbook and convert it to CSV with optional settings.  
  [API reference](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)