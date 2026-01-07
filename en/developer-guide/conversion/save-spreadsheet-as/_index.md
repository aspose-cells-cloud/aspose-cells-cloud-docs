---
title: "Aspose.Cells Cloud Web API - Save the spreadsheet as another format file on remote storage - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to save the spreadsheet as another format file on remote storage: Step-by-Step Guide"
linktitle: "Save Spreadsheet as"
type: docs
url: /save-spreadsheet-as/
keywords: "spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, REST"
description: "Effortlessly convert spreadsheets stored in the cloud to various formats, including XLSX, PDF, and CSV, using our robust API."
weight: 100
---

Save a cloud spreadsheet/Excel file as a format file to cloud storage.

## **Save Spreadsheet as API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| name | String | Path | (Required) The name of the workbook file to be converted. |
| format | String | Query | (Required) The desired output format (e.g., "Xlsx", "PDF", "CSV"). |
| saveOptionsData | Class | Body | (Optional) Save options data. The default is null. |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should you use the Save Spread API?

### Enterprise Document Management System

- Automatically save financial reports as PDF archives
- Regularly backup sales data in CSV format
- Save project plans as read-only to prevent accidental changes

### Data Integration and ETL Processes

- Export CRM system data and save as a standard Excel template
- Convert ERP data to CSV for import into other systems
- Save raw data as JSON for API transmission

### Development and Automation Scenarios

- Backend processing for web applications
- Automated report generation system
- Cloud collaboration platform
- Approval process integration
- Data backup and migration

## Why should you use the Save Spread API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Comprehensive Format Support**: Convert between 20+ spreadsheet formats.
- **Preserve Data Fidelity & Formatting**

## How to Use the Convert Table to JSON API with SDKs?

### Save Spreadsheet as API Specification

The [Save Spreadsheet as API Specification](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to save a spreadsheet as a format file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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
