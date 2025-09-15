---
title: "Aspose.Cells Cloud Web API - Import Csv, JSON, or XML Data into a Spreadsheet file."
second_title: "Document"
ArticleTitle: "Import Csv, JSON, or XML Data into a Spreadsheet file."
linktitle: "Import Data into Spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cells"
description: "Efficiently import data into a spreadsheet from supported formats like CSV, JSON, and XML using the Aspose.Cells Cloud Web API."
weight: 100
kwords: "Aspose.Cells Cloud Web API, Import Data, Office Cloud, REST, Spreadsheet, CSV, JSON, XML"
---

Import data into a spreadsheet worksheet. The supported format of the imported data file is [Xml](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) or [CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Import Data into Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| datafile | File | FormData | Upload the data file to be imported. |
| Spreadsheet | File | FormData | Upload the target spreadsheet file. |
| worksheet | String | Query | Specify the worksheet for importing data. |
| startcell | String | Query | Specify the starting position for importing data. |
| insert | Boolean | Query | Indicates whether to insert or overwrite the specified import data. |
| convertNumericData | Boolean | Query | Specify whether to convert numerical data during import. |
| splitter | String | Query | Specify the delimiter for CSV format. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Specify the output file storage name. |
| fontsLocation | String | Query | Define custom fonts to be used. |
| regoin | String | Query | Set the spreadsheet region configuration. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response**

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

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Import Data into Spreadsheet API?

- Importing large amounts of data into spreadsheet worksheet.
- The imported data file format is [Xml](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) and [CSV](https://docs.fileformat.com/spreadsheet/csv/).

## Why should you use the Import Data into Spreadsheet API?

- Importing large amounts of data into spreadsheets.
- Development can be quickly completed through the existing SDK.

## How to Use the Import Data into Spreadsheet API with SDKs

### Import Data into Spreadsheet API Specification

The [Import Data into Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to import data into  a spreadsheet worksheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
