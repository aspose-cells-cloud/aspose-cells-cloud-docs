---
title: "Aspose.Cells Cloud Web API - Export Remote Excel Range to other formats - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Export the Remote Spreadsheet Range to other formats: Step-by-Step Guide"
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel worksheet"
description: "Convert a specified range of a spreadsheet in cloud storage to various formats such as PDF, CSV, or image formats without downloading the file."
weight: 100
---

Export a cloud spreadsheet/Excel range to a format file. The format file can be saved in the cloud or exported to the local storage.

## **Export Range as Format API**

### API Endpoint

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|(Required) The name of the workbook file to be retrieved.|
|worksheet|String|Path|The The worksheet name of Spreadsheet/Excel|
|range|String|Path|The range to be converted (e.g., A1:C12).|
|format|String|Query|(Required) The desired output format (e.g., "png", "pdf", "svg").|
|folder|String|Query|(Optional) The folder path where the workbook is stored. Defaults to null.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Defaults to default storage if omitted.|
|outPath|String|Query|(Optional) The folder path for the output file. Defaults to null.|
|outStorageName|String|Query|The name of the output file storage.|
|fontsLocation|String|Query|Custom fonts location.|
|region|String|Query|The region setting of the spreadsheet.|
|password|String|Query|The password required to open the spreadsheet file.|

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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should you use the Export Range to another format API?

### **Data Export & Migration Scenarios**

- **Database Integration**: Export specific Excel ranges directly to database systems
- **Application Integration**: Feed selected spreadsheet data into SaaS applications
- **System Migration**: Transfer specific data ranges between legacy and modern systems
- **Cross-Platform Sharing**: Share focused data subsets across different platforms

### **Reporting & Analytics**

- **Targeted Reporting**: Export specific report sections to other format for focused analysis
- **Dashboard Data Feeds**: Supply specific data ranges to BI dashboard tools
- **Performance Metrics**: Extract KPI ranges for performance tracking systems
- **Financial Reporting**: Export financial statement sections for external auditing

### **Development & Testing**

- **Test Data Management**: Export specific data ranges for testing purposes
- **Development Environments**: Share sample data ranges with development teams
- **API Testing**: Generate CSV test data from specific spreadsheet sections
- **Prototype Development**: Provide focused data sets for application prototypes

### **Business Operations**

- **Selective Data Sharing**: Share specific data ranges with external partners
- **Partial Data Backup**: Backup critical data ranges in data format
- **Departmental Data Transfer**: Share specific data between departments
- **Compliance Reporting**: Export regulatory data ranges for compliance submissions

### **Automation Workflows**

- **Scheduled Range Exports**: Automatically export specific ranges on schedule
- **Trigger-Based Extraction**: Export ranges based on business events or triggers
- **Workflow Integration**: Integrate range exports into business process workflows
- **Batch Range Processing**: Process multiple specific ranges in batch operations

## Why should you use the Export Range to another format API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Cost-Effective**: You can convert charts without first uploading the workbook, which saves storage space and reduces costs.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Export Spreadsheet Range as Format API with SDKs?

### Export Range as Format API Specification

The [Export Range as Format API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to export a spreadsheet data of range  to a format file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
