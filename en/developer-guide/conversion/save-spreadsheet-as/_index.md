---  
title: "Save Spreadsheet as Another Format – Aspose.Cells Cloud API (v4.0)"  
second_title: "Document"  
ArticleTitle: "How to Save a Spreadsheet as Another Format File on Remote Storage: Step‑by‑Step Guide"  
linktitle: "Save Spreadsheet as"  
type: docs  
url: /save-spreadsheet-as/  
keywords: "Aspose Cells, spreadsheet conversion, API, save as, XLSX to PDF, cloud storage"  
description: "Convert an Excel workbook stored in Aspose Cloud to XLSX, PDF, CSV, or any of 20+ formats with a single API call. Learn request syntax, parameters, and sample SDK code."  
weight: 100  
---  

Save a cloud spreadsheet or Excel file as a different format in cloud storage.

## **Save Spreadsheet as API**

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Request Parameters**

| Parameter Name  | Type   | Location | Description                                                                                          |
| :-------------- | :----- | :------- | :--------------------------------------------------------------------------------------------------- |
| name            | String | Path     | **Required.** The name of the workbook file to be converted.                                         |
| format          | String | Query    | **Required.** The desired output format (e.g., `Xlsx`, `PDF`, `CSV`).                               |
| saveOptionsData | Class  | Body     | Optional save‑options data. If omitted, defaults to `null`.                                          |
| folder          | String | Query    | Optional folder path where the source workbook is stored. If omitted, defaults to `null`.           |
| storageName     | String | Query    | Optional name of a custom storage. If omitted, the default storage is used.                         |
| outPath         | String | Query    | Optional output path for the converted file. If omitted, defaults to `null`.                        |
| outStorageName  | String | Query    | Optional storage name for the output file.                                                          |
| fontsLocation   | String | Query    | Optional custom fonts location.                                                                     |
| region          | String | Query    | Optional spreadsheet region setting.                                                                |
| password        | String | Query    | Optional password for opening the spreadsheet file.                                                 |

### **Response**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client ID, or client secret.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.  

## Where should you use the Save Spreadsheet API?

### Enterprise Document Management System

- Automatically save financial reports as PDF archives.  
- Regularly back up sales data in CSV format.  
- Save project plans as read‑only files to prevent accidental changes.

### Data Integration and ETL Processes

- Export CRM system data and save it as a standard Excel template.  
- Convert ERP data to CSV for import into other systems.  
- Save raw data as JSON for API transmission.

### Development and Automation Scenarios

- Backend processing for web applications.  
- Automated report‑generation systems.  
- Cloud collaboration platforms.  
- Approval‑process integration.  
- Data backup and migration.

## Why should you use the Save Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud provides SDKs in multiple languages, enabling rapid development with comprehensive documentation. This reduces the workload compared with building custom conversion solutions.  
- **Reduced Labor Costs** – Eliminates the need for dedicated personnel to handle document consolidation.  
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually make.  
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.  
- **Comprehensive Format Support** – Convert between more than 20 spreadsheet formats.  
- **Preserve Data Fidelity & Formatting** – Maintains original layout, formulas, and styling.

## How to Use the Save Spreadsheet as API with SDKs?

### Save Spreadsheet as API Specification

The [Save Spreadsheet as API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you save a spreadsheet as another format with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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