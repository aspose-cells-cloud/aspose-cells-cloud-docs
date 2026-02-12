---
title: "Aspose.Cells Cloud Web API – Translate Spreadsheet to Target Language"
second_title: "Document"
ArticleTitle: "How to Translate an Entire Spreadsheet Using Aspose.Cells Cloud AI Translation API"
linktitle: "Translate Spreadsheet"
type: docs
url: /translate-spreadsheet/
keywords: "Aspose.Cells Cloud, spreadsheet translation API, AI translation, translate spreadsheet, target language, multi-sheet translation, cloud spreadsheet processing"
description: "Learn how to use the Aspose.Cells Cloud TranslateSpreadsheet API to automatically translate all text in an Excel workbook to a target language while preserving formatting and formulas. Includes request parameters, response details, and real‑world use cases."
weight: 100
---

The **TranslateSpreadsheet** endpoint reads every text element in a workbook, sends the content to an AI‑powered translation service, and returns a new spreadsheet file where all textual data is rendered in the specified target language. The operation keeps the original layout, cell styles, formulas, and multi‑sheet structure intact, making it ideal for globalizing reports, dashboards, and data‑driven documents. Supported file formats include XLS, XLSX, XLSM, CSV, and ODS. Errors are returned for invalid language codes, authentication failures, or translation service outages.

## **Translate Spreadsheet API**

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type   | Location | Required/Optional | Description                                                                                                                                                                                                 |
| :------------- | :----- | :------- | :---------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | Required | FormData          | The Excel workbook to be translated. Acceptable extensions: .xls, .xlsx, .xlsm, .csv, .ods. Maximum file size: 50 MB. Example: `budget.xlsx`.                                                               |
| targetLanguage | string | Required | Query             | ISO 639‑1 language code for the desired output language (e.g., "es" for Spanish, "fr" for French, "de" for German). Must be a language supported by the underlying AI service.                              |
| region         | string | Optional | Query             | Spreadsheet region identifier that influences locale‑specific formatting such as dates, numbers, and currency. Common values: "US", "EU", "CN". If omitted, the workbook’s original region setting is used. |
| password       | string | Optional | Query             | Password for opening a protected workbook. Leave blank when the file is not password‑protected.                                                                                                             |

### **Response**

Successful response (200 OK)
Headers:
Content-Type: application/octet-stream // or text/csv when CSV output is requested
Content-Disposition: attachment; filename="translated.xlsx"
Content-Length: <size in bytes>
Body:
<binary stream containing the translated spreadsheet file>

Error responses follow the standard Aspose.Cells Cloud error model (application/json) with fields `code`, `message`, and optional `details`.

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Translate Spreadsheet API?

- **International Financial Reporting** – Convert quarterly Excel reports into multiple languages for regional offices while preserving formulas and chart layouts.
- **Multi‑language Marketing Dashboards** – Automatically generate localized versions of sales performance dashboards for global teams.
- **Educational Content Distribution** – Translate grade‑books, assignment sheets, or curriculum spreadsheets for students in different countries without manual copy‑pasting.
- **Regulatory Compliance** – Produce language‑specific compliance spreadsheets that retain validation rules and data‑validation lists.

## Why should you use the Translate Spreadsheet API?

- **AI‑driven accuracy** – Leverages state‑of‑the‑art neural translation models for context‑aware, high‑quality language conversion.
- **Zero layout disruption** – Keeps cell formulas, conditional formatting, charts, and worksheet ordering exactly as in the source file.
- **Single‑call multi‑sheet processing** – Translates every worksheet in one request, eliminating the need for per‑sheet loops.
- **Seamless cloud integration** – Works with Aspose.Cells Cloud authentication, enabling automated pipelines in CI/CD, serverless functions, or enterprise back‑ends.

## How to Use the Translate Spreadsheet API with SDKs

### Translate Spreadsheet API Specification

The [Translate Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge a spreadsheet into another spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
