---
title: "Merge Multiple Excel Files into One Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
ArticleTitle: "Combine Multiple Excel Files into One – Batch Merge Spreadsheets to 30+ Formats"
linktitle: "Merge Spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, merge spreadsheets, Excel API, cloud spreadsheet, batch merge, PDF conversion, CSV merge, ODS merge, API reference, SDK"
description: "Combine several local Excel, CSV, or ODS files into a single workbook and convert the result to 30+ formats (PDF, HTML, etc.) using Aspose.Cells Cloud. Includes endpoint, parameters, authentication guide, and SDK examples."
weight: 100
---

Merge multiple local Excel, CSV, or ODS files into a single workbook and convert it to 30+ output formats with Aspose.Cells Cloud API.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name  | Type    | Location         | Description                                                                                      |
| --------------- | ------- | ---------------- | ------------------------------------------------------------------------------------------------ |
| Spreadsheet     | File    | FormData         | The local spreadsheet file to upload. Supports XLSX, XLS, CSV, ODS, etc.                         |
| outFormat       | String  | Query            | Desired output format (e.g., `XLSX`, `PDF`, `CSV`, `HTML`). Supports 30+ formats.                |
| mergeInOneSheet | Boolean | Query            | `true` → all data merged into a single worksheet; `false` → each original sheet is preserved.    |
| outPath         | String  | Query (optional) | Cloud folder path where the merged file will be saved. If omitted, the default location is used. |
| outStorageName  | String  | Query            | Name of the cloud storage to use (default or custom).                                            |
| fontsLocation   | String  | Query (optional) | Cloud folder containing custom fonts for correct PDF/image rendering.                            |
| region          | String  | Query (optional) | Locale for number, date, and currency formatting (e.g., `en-US`, `zh-CN`).                       |
| password        | String  | Query (optional) | Password for opening a protected spreadsheet.                                                    |

### **Response**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

The file can be downloaded directly from or saved to the location specified by `outPath`.

**Success response details**

| Status Code | Content‑Type               | Description                                |
| ----------- | -------------------------- | ------------------------------------------ |
| 200 OK      | `application/octet-stream` | Binary stream of the merged workbook file. |

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## Where should we use the Merge Spreadsheet API?

### **Education and Academic Applications**

- **Student Assignment Grading** – Merge multiple student assignment files for unified comments and grading.
- **Research Data Collection** – Consolidate data spreadsheets from different experimental groups.
- **Teaching Material Creation** – Combine exercises from multiple chapters into a single question‑bank workbook.

### **Data Processing and Analysis**

- **Small Data Set Integration** – Merge CSV or Excel files exported from disparate sources.
- **Data Analysis Pre‑processing** – Combine relevant data files before performing analysis.
- **Template Data Filling** – Populate pre‑set report templates with merged data.

### **Development and Technical Support**

- **Test Data Preparation** – Merge several test case files for automated testing.
- **Log File Analysis** – Consolidate Excel reports of system logs from different periods.
- **Configuration Management** – Merge multiple configuration spreadsheets into a unified configuration file.

## Why should you use the Merge Spreadsheet API?

- **Developer‑Friendly** – SDK libraries are available for many languages, reducing development effort compared with building a custom solution.
- **Reduced Labor Costs** – Eliminates the need for dedicated staff to perform manual document consolidation.
- **Pay‑per‑Use** – Only pay for the API calls you actually make; no upfront investment.
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Merge Spreadsheet API with SDKs

### OpenAPI Specification

The <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI Specification</a> provides a machine‑readable description of the API, enabling direct REST interactions.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}
