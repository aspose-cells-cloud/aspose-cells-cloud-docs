---
title: "Aspose.Cells Cloud – Change Word Case (Upper, Lower, Proper, Sentence)"
ArticleTitle: "Excel Case Converter – Uppercase, Lowercase, Proper Case & Sentence Case"
linktitle: "Word Case"
type: docs
url: /change-word-case/
keywords: "change word case API, Aspose.Cells, Excel case conversion, uppercase, lowercase, proper case, sentence case, text formatting"
description: "Convert Excel text case using Aspose.Cells Cloud API: uppercase, lowercase, proper case, and sentence case"
weight: 100
---
The **UpdateWordCase** API (`PUT https://api.aspose.cloud/v4.0/cells/content/wordcase`) in Aspose.Cells Cloud enables instant text case conversion in spreadsheets—supporting Upper Case, Lower Case, Proper Case, and Sentence Case—by processing only string cells while preserving formulas, formatting, and data validation; users upload a spreadsheet and specify the desired case type via query parameter, optionally targeting a specific worksheet or range.

## The Update Word Case Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| wordCaseType | String | Query | Specify text case: Upper Case, Lower Case, Proper Case, Sentence Case. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

On success the service returns **200 OK** (or **202 Accepted**) with a JSON payload containing the binary stream of the processed workbook.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token or incorrect client credentials.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – The spreadsheet encountered an internal processing anomaly.

Use the Aspose.Cells Cloud Web API to instantly convert text case in your spreadsheet—switch between uppercase, lowercase, proper case (capitalize each word), or sentence case (capitalize the first letter of each sentence) across a selected range. Only string cells are affected; numbers, booleans, errors, and blanks are ignored. Formulas, formatting, and data validation remain untouched.

- **UpperCase** – every character capitalized.
- **LowerCase** – every character lower‑cased.
- **ProperCase** – first letter of each word upper‑cased, the remainder lower‑cased.
- **SentenceCase** – first letter of each sentence upper‑cased, the remainder lower‑cased.

<img src="images/result.png" alt="Before/After case conversion screenshot" width="800" height="450" />

## Where should we use the change word case API?

### Data Cleaning and Standardization

- **Customer Data Management** – Standardize the capitalization of customer names and address information (e.g., `john doe` → `John Doe`).
- **Product Catalog Processing** – Standardize product titles and description texts (e.g., `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Financial Report Generation** – Normalize item names and description fields in financial statements.

### Multi‑source Data Integration

- **Data Warehouse ETL** – Standardize text format when loading data from various systems.
- **API Data Reception** – Handle data with inconsistent capitalization returned by external APIs.
- **Cross‑department Data Merging** – Standardize text format in Excel reports from different departments.

### Content Management System

- **Automated News Releases** – Automatically format news headlines and content (capitalization rules for titles).
- **Product Documentation Generation** – Ensure consistency in the formatting of technical documentation terms.
- **Knowledge Base Maintenance** – Standardize the text format of FAQs and help documents.

### Enterprise Application Integration

- **CRM System Integration** – Automatically format names and company information during import/export of customer data.
- **ERP Data Processing** – Standardize key fields such as material descriptions and supplier names.
- **HR Management System** – Standardize employee information and job titles.

### Batch Document Processing

- **Legal Document Preparation** – Batch processing of clause formats in contracts and agreements.
- **Marketing Materials Generation** – Standardize text formats of advertising copy and email templates.
- **Academic Paper Formatting** – Standardize format requirements for references and titles.

### Real‑time Data Processing

- **User Input Validation** – Real‑time formatting of form data submitted by users.
- **Chatbot Responses** – Standardization of text format for automatically generated responses.
- **Instant Report Generation** – Dynamic creation of uniformly formatted business reports.

### Internationalization and Localization

- **Multilingual Data Processing** – Handle differences in capitalization rules for texts in various languages.
- **Localization Content Preparation** – Prepare formatted local content for different regions.
- **Translation Project Management** – Ensure consistency in text format before and after translation.

## Why should you use the change word case API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comprehensive documentation. Compared to building custom solutions, this significantly reduces development workload.
- **Cost‑Effective** – You can change word case without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## How to Use the Update Word Case API with SDKs?

### Update Word Case API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase" rel="noopener noreferrer">Update Word Case API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement **UpdateWordCase** for cells with minimal code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
