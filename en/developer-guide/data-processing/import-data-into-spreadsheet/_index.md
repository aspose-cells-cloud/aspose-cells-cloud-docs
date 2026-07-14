---
title: "Aspose.Cells Cloud Data Import API – A cloud solution for automatically importing CSV, JSON, and XML data into Excel spreadsheets."
second_title: "Document"
ArticleTitle: "Multi‑Source Data Integration Excel Platform – Aspose.Cells Cloud Automated Data Import and Transformation API."
linktitle: "Import Data into Spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, data import API, CSV to Excel, JSON to Excel, XML to Excel, cloud spreadsheet, REST API"
description: "Import CSV, JSON, or XML data into Excel spreadsheets with Aspose.Cells Cloud REST API. Learn request format, parameters, sample SDK code, and error handling."
weight: 100
---

## Core Features

### Multi-Format Data Support

- **[CSV](https://docs.fileformat.com/spreadsheet/csv/) Data Import**: Supports various delimiters and automatically detects encoding.
- **[JSON](https://docs.fileformat.com/web/json/) Data Handling**: Flattens complex JSON structures into Excel tables.
- **[XML](https://docs.fileformat.com/web/xml/) File Conversion**: Maps node data to Excel row and column structure.

## **Import Data into Spreadsheet API Description**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name     | Type   | Location         | Description                                                              |
| ------------------ | ------ | ---------------- | ------------------------------------------------------------------------ |
| datafile           | File   | FormData         | The data file (CSV, JSON, or XML) to be imported.                        |
| spreadsheet        | File   | FormData         | The target workbook that will receive the imported data.                 |
| worksheet          | string | Query            | Name of the worksheet where data will be placed.                         |
| startCell          | string | Query            | Top‑left cell (e.g., `A1`) that marks the start position for the import. |
| insert             | bool   | Query            | `true` to insert rows; `false` to overwrite existing data.               |
| convertNumericData | bool   | Query            | `true` to convert numeric strings to numbers during import.              |
| splitter           | string | Query            | Single‑character CSV delimiter (default is `,`).                         |
| outPath            | string | Query (optional) | Folder path where the updated workbook will be stored.                   |
| outStorageName     | string | Query (optional) | Name of the storage location for the output file.                        |
| fontsLocation      | string | Query (optional) | Path to a custom fonts folder, if required.                              |
| region             | string | Query (optional) | Spreadsheet region configuration (e.g., `en-US`).                        |
| password           | string | Query (optional) | Password for opening a protected workbook.                               |

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Error Codes

| Code | Message               | When It Occurs                                      |
| ---- | --------------------- | --------------------------------------------------- |
| 400  | Bad Request           | Invalid API URI or malformed request parameters.    |
| 401  | Unauthorized          | Missing/invalid access token or client credentials. |
| 404  | Not Found             | The specified spreadsheet cannot be accessed.       |
| 500  | Internal Server Error | An unexpected server‑side problem while processing. |

## Why You Should Use This API

- **Efficient data loading** – Enables bulk import of large datasets directly into a workbook without creating intermediate files.  
- **Broad SDK support** – Provides client libraries for .NET, Java, PHP, Ruby, Node.js, Python, Go, and Perl, simplifying integration.  
- **In‑memory processing** – Performs transformations in memory, which reduces temporary storage requirements.  

## How to Use the Import Data into Spreadsheet API with SDKs

**Prerequisites:** To use this API you must have a valid Aspose Cloud account, the latest version of the Aspose.Cells Cloud SDK (v4.0 or newer), and an OAuth2 access token with the `Cells.ReadWrite` scope. The data files must not exceed the service‑specific size limits (typically 100 MB per file).

**Notes / Limitations:** The API supports up to 1 000 000 rows per import. Only comma is the default CSV delimiter; other single‑character delimiters can be specified via the `splitter` parameter. Large XML files may increase processing time.

For related operations such as exporting data or converting workbook formats, see the **Export Data** and **Convert Workbook** documentation.

### Import Data into Spreadsheet API Specification

The [Import Data into Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp

```

{{</tab>}}
{{<tab tabNum="2" >}}

```java

```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}

