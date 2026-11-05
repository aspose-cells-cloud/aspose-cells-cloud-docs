---
title: "Convert Excel Range to PDF using Aspose.Cells Cloud API v4.0"
ArticleTitle: "How to Convert Local Spreadsheet Range Data to a PDF File: Step‑By‑Step Guide"
linktitle: "Convert Range to PDF"
type: docs
url: /convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, Excel to PDF, range to PDF, cloud API, REST conversion"
description: "Convert Excel range to PDF using Aspose.Cells Cloud REST API with cURL or SDKs—secure, format-preserving conversion."
weight: 100
date: 2024-03-15
lastmod: 2024-03-15
---
The **ConvertRangeToPdf** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf`) in Aspose.Cells Cloud enables direct conversion of a specified cell range—defined by worksheet name and range address (e.g., "Sheet1!A1:C10")—from a locally uploaded Excel file into a PDF document, leveraging cloud-native processing without requiring prior file upload to storage.

## The Convert Range to PDF Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| range | String | Query | cell area. e.g. A1:C10 |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

_Typical response is a binary PDF stream returned as a file download._

## **Where Should You Use the Convert Range to PDF API?**

- **Financial Statements**: Convert balance sheets, income statements (specific ranges) to PDF for audit‑ready documentation.
- **Sales Reports**: Transform sales dashboards or commission calculations to distributable PDFs.
- **Operational Metrics**: Export KPI tables and performance metrics as formal PDF reports.
- **Contractual Data**: Export pricing tables and service‑level agreements from spreadsheets to PDF attachments.
- **Audit Trails**: Preserve financial data ranges as uneditable PDF evidence.
- **Portfolio Summaries**: Export investment performance ranges as client‑ready PDF statements.
- **Quality Control Reports**: Export inspection data ranges to PDF for compliance records.
- **Inventory Summaries**: Transform stock‑level tables to PDF for management review.

## Why Should You Use the Convert Range to PDF API?

- **Developer‑Friendly**: Aspose.Cells Cloud SDKs reduce API integration to fewer than 10 lines of code (e.g., 7 lines in Python), significantly accelerating development compared with custom rendering solutions.
- **Cost‑Effective**: You can convert range data without first uploading the entire workbook, saving storage space and reducing costs.
- **Preserves Complex Excel Formatting** in a universally accessible PDF format.

## How to Use the Convert Range to PDF API with SDKs?

### Convert Range to PDF API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf" rel="noopener noreferrer">Convert Range to PDF API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="2" tabID="1" tabName1="PHP" tabName2="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}
