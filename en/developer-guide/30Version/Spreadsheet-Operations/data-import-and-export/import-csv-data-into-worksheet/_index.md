---
title: "Import CSV Data into Excel Worksheet"
second_title: "Document"
linktitle: "Import CSV data"
type: docs
url: /import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "Import CSV data, Excel, Aspose.Cells Cloud, REST API, Spreadsheet, CSV import"
description: "Aspose.Cells Cloud REST API enables importing CSV data into Excel worksheets. Supported SDKs include Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 19
---

This REST API **imports CSV data** into an Excel worksheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the `ImportCSVDataOption` data and the second part contains the CSV file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the tables below.

### ImportCSVDataOption

| Parameter Name      | Type                                 | Description                                                                 |
|---------------------|--------------------------------------|-----------------------------------------------------------------------------|
| SeparatorString     | string                               | Character used to separate fields in the CSV file (e.g., `,` or `;`).      |
| ConvertNumericData  | string (`true`/`false`)              | Indicates whether numeric strings should be converted to numeric values. |
| FirstRow            | int                                  | 1‑based index of the first row where the data will be placed.              |
| FirstColumn         | int                                  | 1‑based index of the first column where the data will be placed.           |
| SourceFile          | string                               | Name of the source CSV file to be imported.                                 |
| CustomParsers       | List\<CustomParserConfig\>           | Collection of custom parser configurations for specific columns.          |

### CustomParserConfig

| Parameter Name | Type   | Description                                                             |
|----------------|--------|-------------------------------------------------------------------------|
| ColumnIndex    | int    | Zero‑based index of the column to which the custom parser applies.     |
| ParseMethod    | string | Parsing method for the column (e.g., `ToString`, `ToDate`, `ToNumber`).|
| CustomStyle    | string | Custom style (e.g., number format) applied to the parsed cells.        |

**Example**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```

## Cloud SDK Family

Using an SDK is the best way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call the Aspose.Cells web service using the PHP SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}