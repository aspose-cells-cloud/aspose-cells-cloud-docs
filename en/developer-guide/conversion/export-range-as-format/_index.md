---
title: "Export Excel Range to PDF, PNG, CSV – Aspose.Cells Cloud API"
second_title: "Document"
ArticleTitle: "How to Export a Remote Spreadsheet Range to Other Formats: Step‑by‑Step Guide"
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells, Export Excel Range, PDF, PNG, CSV, Cloud API, Spreadsheet Conversion"
description: "Learn how to convert a specific Excel range stored in Aspose Cells Cloud to PDF, PNG, CSV or other formats. Includes endpoint details, parameters, sample requests, response handling, and error information."
weight: 100
---

Export a cloud spreadsheet/Excel range to a format file. The format file can be saved in the cloud or exported to local storage.

**Prerequisites:** To use this API you must have a valid Aspose Cloud account, obtain a client ID and client secret, generate a JWT access token, and ensure the workbook you want to convert is uploaded to your chosen storage.

## Export Range as Format API

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name     | Type   | Location | Description                                                                                                                                        |
| :----------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path     | (Required) The name of the workbook file to be retrieved.                                                                                          |
| **worksheet**      | String | Path     | The worksheet name of the spreadsheet.                                                                                                             |
| **range**          | String | Path     | The range to be converted (e.g., `A1:C12`).                                                                                                        |
| **format**         | String | Query    | (Required) Desired output format (e.g., `pdf`, `png`, `svg`).                                                                                      |
| **folder**         | String | Query    | (Optional) Folder path where the workbook is stored.                                                                                               |
| **storageName**    | String | Query    | (Optional) Name of the storage if using a custom cloud storage.                                                                                    |
| **outPath**        | String | Query    | (Optional) Path for the output file in cloud storage.                                                                                              |
| **outStorageName** | String | Query    | (Optional) Storage name for the output file.                                                                                                       |
| **fontsLocation**  | String | Query    | (Optional) Custom fonts location.                                                                                                                  |
| **region**         | String | Query    | (Optional) Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| **password**       | String | Query    | (Optional) Password required to open the spreadsheet file.                                                                                         |

#### Sample cURL Request

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

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

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client ID, or client secret.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

**HTTP Status‑Code Summary**

| Status | Description                                   |
| ------ | --------------------------------------------- |
| 200    | Successful export; binary file returned.      |
| 400    | Bad request – malformed URI or parameters.    |
| 401    | Unauthorized – authentication failure.        |
| 404    | Not found – workbook or worksheet missing.    |
| 500    | Internal server error – processing failure.   |

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
- **No Server Maintenance** – No servers to maintain, no software updates, and no compatibility issues.
- **Preserves Complex Excel Formatting** – Output files retain the original spreadsheet’s formatting.

## How to Use the Export Spreadsheet Range as Format API with SDKs?

### Export Range as Format API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Export Range as Format API Specification</a> provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to export a spreadsheet range to a format file with concise code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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

### See Also

- **Export Worksheet as Format** – Convert an entire worksheet to PDF, PNG, CSV, etc.  
- **Convert Workbook to PDF** – Transform a whole workbook into a PDF document.  
- **Export Range to Image** – Generate image files (PNG, JPEG) from a specific range.  

These related endpoints can help you handle broader conversion scenarios.