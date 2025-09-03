---
title: "Import Data into Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Import Data into Spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Import data, Excel API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cells"
description: "Efficiently import data into a spreadsheet from supported formats like CSV, JSON, and XML using the Excel API."
weight: 100
kwords: "Excel API, Import Data, Office Cloud, REST API, Spreadsheet, CSV, JSON, XML, Data Integration, Error Handling"
---

# **Excel API: Import Data Into Spreadsheet**

## **Overview**

Efficiently import data into a spreadsheet from supported file formats such as CSV, JSON, and XML.

## **Function Description**

This API enables the importation of data into a spreadsheet from supported data file formats (CSV, JSON, XML).
It requires two primary inputs: the target spreadsheet and the data file.
The data file must be accessible and in one of the supported formats (CSV, JSON, XML).
The API ensures that the import process is handled efficiently, accurately parsing and inserting data into the specified spreadsheet.
In cases where the data file is inaccessible, the format is unsupported, or errors occur during the import process, appropriate exceptions are thrown.
Users are advised to ensure that their data files are properly formatted and that the target spreadsheet is accessible to avoid errors.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

## The request parameters of **importDataIntoSpreadsheet** API are

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

## **Response Structure**

```json
{
File
}
```

## **Error Handling**

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication failed, or credentials were not provided.
- **404 Not Found**: Source file is not accessible.
- **500 Server Error**: An anomaly occurred during data retrieval from the spreadsheet.

## **Usage Scenarios and Key Features**

- **Multiple Data Formats**: Import data seamlessly from CSV, JSON, and XML file formats.
- **Direct Spreadsheet Integration**: Easily import data directly into the specified spreadsheet.
- **Efficient Data Handling**: Ensure accurate parsing and efficient handling of data during import.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.

## **Excel API SDK**

Utilizing an SDK is the optimal approach to expedite development. An SDK manages low-level details, allowing you to concentrate on your project tasks. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

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
