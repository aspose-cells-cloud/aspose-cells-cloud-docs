---
title: "Export Excel Range to PDF, PNG, CSV – Aspose.Cells Cloud API"
second_title: "Document"
ArticleTitle: "How to Export a Remote Spreadsheet Range to Other Formats: Step‑by‑Step Guide"
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose.Cells, Export Range, Cloud API, Excel to PDF, Excel to CSV, Spreadsheet conversion"
description: "Convert a specific Excel range stored in Aspose Cloud to PDF, PNG, CSV or other formats. Learn the endpoint, parameters, sample code, and error handling."
weight: 100
---

![Aspose.Cells Cloud v4.0](https://img.shields.io/badge/Aspose.Cells%20Cloud-v4.0-blue)

Export a cloud spreadsheet/Excel range to a format file. The format file can be saved in the cloud or exported to local storage.

## Export Range as Format API

### Prerequisites

To call this API you must obtain an OAuth 2.0 access token.

1. **Request a token** – Send a `POST` request to  
   `https://api.aspose.cloud/connect/token` with your **client_id** and **client_secret**.  
2. **Include the token** – Add the header `Authorization: Bearer <access_token>` to every request.  
3. **Set the storage (optional)** – If you use a custom storage, specify `storageName` or `outStorageName` in the query string.

### API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### Full Request Example

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyBook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf&outPath=output/MyRange.pdf" \
     -H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type   | Location | Description |
| :------------- | :----- | :------- | :---------- |
| **name** | String | Path | (Required) The name of the workbook file to be retrieved. |
| **worksheet** | String | Path | The worksheet name of the spreadsheet. |
| **range** | String | Path | The range to be converted (e.g., `A1:C12`). |
| **format** | String | Query | (Required) Desired output format (e.g., `pdf`, `png`, `svg`). |
| **folder** | String | Query | (Optional) Folder path where the workbook is stored. |
| **storageName** | String | Query | (Optional) Name of the storage if using a custom cloud storage. |
| **outPath** | String | Query | (Optional) Path for the output file in cloud storage. |
| **outStorageName** | String | Query | (Optional) Storage name for the output file. |
| **fontsLocation** | String | Query | (Optional) Custom fonts location. |
| **region** | String | Query | (Optional) Region setting of the spreadsheet. |
| **password** | String | Query | (Optional) Password required to open the spreadsheet file. |

### Response Details

The API returns a binary stream containing the exported file.  
- **Content‑Type** – Corresponds to the requested format (e.g., `application/pdf`).  
- **Response body** – The file data can be saved directly to disk or streamed to another service.  

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

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client ID, or client secret.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should you use the Export Range to another format API?

### Data Export & Migration Scenarios

- **Database Integration** – Export specific Excel ranges directly to database systems.  
- **Application Integration** – Feed selected spreadsheet data into SaaS applications.  
- **System Migration** – Transfer specific data ranges between legacy and modern systems.  
- **Cross‑Platform Sharing** – Share focused data subsets across different platforms.

### Reporting & Analytics

- **Targeted Reporting** – Export specific report sections to other formats for focused analysis.  
- **Dashboard Data Feeds** – Supply specific data ranges to BI dashboard tools.  
- **Performance Metrics** – Extract KPI ranges for performance‑tracking systems.  
- **Financial Reporting** – Export financial statement sections for external auditing.

### Development & Testing

- **Test Data Management** – Export specific data ranges for testing purposes.  
- **Development Environments** – Share sample data ranges with development teams.  
- **API Testing** – Generate CSV test data from specific spreadsheet sections.  
- **Prototype Development** – Provide focused data sets for application prototypes.

### Business Operations

- **Selective Data Sharing** – Share specific data ranges with external partners.  
- **Partial Data Backup** – Backup critical data ranges in a chosen format.  
- **Departmental Data Transfer** – Share specific data between departments.  
- **Compliance Reporting** – Export regulatory data ranges for compliance submissions.

### Automation Workflows

- **Scheduled Range Exports** – Automatically export specific ranges on a schedule.  
- **Trigger‑Based Extraction** – Export ranges based on business events or triggers.  
- **Workflow Integration** – Integrate range exports into business process workflows.  
- **Batch Range Processing** – Process multiple specific ranges in batch operations.

## Why should you use the Export Range to another format API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development with comprehensive documentation. Compared to building custom chart‑rendering solutions, this significantly reduces development workload.  
- **Reduced Labor Costs** – Less need for personnel dedicated to document consolidation.  
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility issues.  
- **Preserves Complex Excel Formatting** – Output files retain the original spreadsheet’s formatting.

## How to Use the Export Spreadsheet Range as Format API with SDKs?

### Export Range as Format API Specification

The [Export Range as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to export a spreadsheet range to a format file with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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