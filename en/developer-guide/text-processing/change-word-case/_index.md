---
title: "Aspose.Cells Cloud Change Word Case API - Convert to Uppercase, Lowercase, Proper Case"
second_title: "Document"
ArticleTitle: "Excel Case Converter - Uppercase, Lowercase, Proper Case & Sentence Case Tool"
linktitle: "Word Case"
type: docs
url: /change-word-case/
keywords: "change Excel text case, convert uppercase lowercase Excel, proper case Excel, capitalize first letter each word, sentence case Excel, Excel case conversion tool, Aspose.Cells case API, text formatting Excel, bulk case change, Excel text transformation"
description: "Change text case in Excel spreadsheets to uppercase, lowercase, proper case (first letter of each word), or sentence case (first letter of sentence) with Aspose.Cells API. Adjust text formatting in bulk according to your needs."
weight: 100
---

Convert Excel text case instantly—switch between uppercase, lowercase, proper case (capitalize each word), or sentence case (capitalize first letter). Use Aspose.Cells Cloud Web API to adjust text formatting in bulk across your spreadsheet.

## Overview

Converts text values in the chosen range to upper, lower, proper or sentence case; formulas, formatting and data-validation remain untouched. String cells only – numbers, booleans, errors and blanks are ignored.

- **UpperCase**  – every character capitalized.
- **LowerCase**  – every character lowercased.
- **ProperCase**  – first letter of each word uppercase, remainder lowercase.
- **SentenceCase**  –  first letter of each sentence uppercase, remainder lowercase.

[](images/result.png)

## **ChangeWordCase API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/content/wordcase
```

### The request parameters of **updateWordCase** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc. |
| wordCaseType | String | Query | Specifies the text case conversion type: `Upper Case` (全部大写), `Lower Case` (全部小写), `Proper Case` (每个单词首字母大写), `Sentence Case` (句子首字母大写). |
| worksheet | String | Query | *(Optional)* The name of the worksheet where case conversion will be applied. If omitted, the operation applies to the first worksheet. |
| range | String | Query | *(Optional)* The cell range where case conversion will be applied (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath | String | Query | *(Optional)* The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output file will be stored. |
| region | String | Query | *(Optional)* Sets the locale for text case conversion rules, particularly relevant for language-specific capitalization (e.g., `"en-US"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If the uploaded spreadsheet is password-protected, provide the password to open and process the file. |

### **Response**

```json
{
File
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the change word case API?

### **Data Cleaning and Standardization**

- **Customer Data Management**: Standardize the capitalization of customer names and address information (e.g., `john doe` → `John Doe`)
- **Product Catalog Processing**: Standardize product titles and description texts (e.g., `IPHONE 15 PRO` → `iPhone 15 Pro`)
- **Financial Report Generation**: Normalize the item names and description fields in financial statements

### Multi-source Data Integration

- **Data Warehouse ETL**: Standardize the text format when loading data from various systems
- **API Data Reception**: Handle data with inconsistent capitalization returned by external APIs
- **Cross-department Data Merging**: Standardize the text format in Excel reports from various departments

### Content Management System

- **Automated News Releases**: Automatically format news headlines and content (capitalization rules for titles)
- **Product Documentation Generation**: Ensure consistency in the formatting of technical documentation terms
- **Knowledge Base Maintenance**: Standardize the text format of FAQs and help documents

### Enterprise Application Integration

- **CRM System Integration**: Automatically format names and company information during the import/export of customer data
- **ERP Data Processing**: Standardize the formats of key fields such as material descriptions and supplier names
- **HR Management System**: Standardize employee information and job titles, etc.

### Batch Document Processing

- **Legal Document Preparation**: Batch processing of clause formats in contracts and agreements
- **Marketing Materials Generation**: Standardizing the text formats of advertising copy and email templates
- **Academic Paper Formatting**: Standardizing the format requirements for references and titles

### Real-time Data Processing

- **User Input Validation**: Real-time formatting of the form data submitted by users
- **Chatbot Responses**: Standardization of the text format for automatically generated responses
- **Instant Report Generation**: Dynamic creation of uniformly formatted business reports

### Internationalization and Localization

- **Multilingual Data Processing**: Handling the differences in capitalization rules for texts in various languages
- **Localization Content Preparation**: Preparing formatted local content for different regions
- **Translation Project Management**: Ensuring consistency in text format before and after translation

## Why should you use the change word case API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Cost-Effective**: You can change word case without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/UpdateWordCase) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Update word case for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
