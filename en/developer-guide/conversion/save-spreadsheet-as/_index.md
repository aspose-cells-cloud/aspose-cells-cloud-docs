---
title: "Save Spreadsheet as Another Format – Aspose.Cells Cloud API (v4.0)"
second_title: "Document"
ArticleTitle: "How to Save a Spreadsheet as Another Format File on Remote Storage: Step‑by‑Step Guide"
linktitle: "Save Spreadsheet as"
type: docs
url: /save-spreadsheet-as/
keywords: "Aspose Cells, spreadsheet conversion, save as, API, XLSX to PDF, cloud storage, Excel to PDF, CSV export, cloud conversion"
description: "Learn how to save a spreadsheet stored in Aspose Cloud as another format (XLSX, PDF, CSV, etc.) using the Aspose.Cells Cloud Save Spreadsheet API. Includes request syntax, parameters, curl example, and SDK code."
weight: 100
---

Save a cloud spreadsheet or Excel file as a different format in cloud storage.

## **Save Spreadsheet as API**

The API requires a valid OAuth 2.0 access token. Obtain the token by registering an application in the Aspose Cloud dashboard, then request a token using your client ID and client secret. Include the token in the `Authorization: Bearer {access_token}` header for every request.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

**Example with request body and curl**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name  | Type   | Location | Description                                                                               |
| :-------------- | :----- | :------- | :---------------------------------------------------------------------------------------- |
| name            | String | Path     | **Required.** The name of the workbook file to be converted.                              |
| format          | String | Query    | **Required.** The desired output format (e.g., `Xlsx`, `PDF`, `CSV`).                     |
| saveOptionsData | Class  | Body     | Optional save‑options data. If omitted, defaults to `null`.                               |
| folder          | String | Query    | Optional folder path where the source workbook is stored. If omitted, defaults to `null`. |
| storageName     | String | Query    | Optional name of a custom storage. If omitted, the default storage is used.               |
| outPath         | String | Query    | Optional output path for the converted file. If omitted, defaults to `null`.              |
| outStorageName  | String | Query    | Optional storage name for the output file.                                                |
| fontsLocation   | String | Query    | Optional custom fonts location.                                                           |
| region          | String | Query    | Optional spreadsheet region setting.                                                      |
| password        | String | Query    | Optional password for opening the spreadsheet file.                                       |

**Supported output formats**

| Format | Extension |
| :----- | :-------- |
| Xlsx   | .xlsx |
| Pdf    | .pdf |
| Csv    | .csv |
| Html   | .html |
| Ods    | .ods |
| Xls    | .xls |
| Txt    | .txt |
| Mhtml  | .mhtml |
| Tiff   | .tiff |
| Pptx   | .pptx |
| … (more) | See API spec for the full list (over 20 formats) |

### **Response**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Sample error response (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Invalid request parameters."
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
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

- **Developer‑Friendly** – Provides SDKs for multiple languages with detailed documentation, simplifying integration.  
- **Labor‑Efficient** – Handles conversion on the server, reducing the need for custom conversion code.  
- **Usage‑Based Pricing** – Charges only for the API calls performed, without upfront licensing fees.  
- **No Server Maintenance** – The service runs in the cloud, removing the need to manage conversion infrastructure.  
- **Extensive Format Support** – Supports conversion among more than 20 spreadsheet formats.  
- **Data Fidelity** – Preserves layout, formulas, and styling during conversion.

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

### Related Topics

Explore other conversion APIs that may complement your workflow:

- **Convert Spreadsheet to PDF** – Quickly turn Excel files into PDF documents.  
- **Export Table as CSV** – Extract tabular data for analytics pipelines.  
- **Convert Spreadsheet to HTML** – Render workbooks directly in web pages.

These links help developers discover additional functionality within the Aspose.Cells Cloud suite.