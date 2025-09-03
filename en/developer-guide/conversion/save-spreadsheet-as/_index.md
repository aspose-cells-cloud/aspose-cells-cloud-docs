---
title: "Save Spreadsheet as - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Save Spreadsheet as"
type: docs
url: /save-spreadsheet-as/
keywords: "spreadsheet conversion, cloud storage API, Excel to PDF, Excel to CSV, REST API, Aspose.Cells"
description: "Effortlessly convert spreadsheets stored in the cloud to various formats, including XLSX, PDF, and CSV, using our robust API."
weight: 100
kwords: "Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, convert Excel files, save spreadsheet as, API functionality, cloud-based conversion"
---

# **Excel API: SaveSpreadsheetAs**

## **Overview**

This API allows users to convert a spreadsheet stored in cloud storage into a specified format seamlessly.

## **Function Description**

The `SaveSpreadsheetAs` method directly accesses a spreadsheet file from cloud storage, converting it into the desired output format (e.g., XLSX, PDF, CSV) while ensuring that no local downloads are necessary.
It is crucial to have the cloud storage configuration (including access credentials and file path) correctly set up.
The conversion is performed entirely within the cloud environment, minimizing data transfer and enhancing security by keeping sensitive information within the cloud infrastructure.
Should the specified source file be unavailable or if an error occurs during the conversion, an appropriate exception will be thrown.
Supported output formats are contingent on the capabilities of the underlying conversion service.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

## The request parameters of **saveSpreadsheetAs** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| name | String | Path | (Required) The name of the workbook file to be converted. |
| format | String | Query | (Required) The desired output format (e.g., "Xlsx", "Pdf", "Csv"). |
| saveOptionsData | Class | Body | (Optional) Save options data. The default is null. |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

## **Response Structure**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication failed or no credentials provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Based Conversion**: Access and convert spreadsheet files in cloud storage to desired formats (e.g., XLSX, PDF, CSV) without local downloads.
- **Efficient Data Handling**: The API minimizes data transfer by performing conversions remotely and enhances security by keeping sensitive data within the cloud infrastructure.
- **Convenience**: Simplifies the conversion process by managing everything in the cloud.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to expedite your development process. SDKs handle low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples showcase how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}
