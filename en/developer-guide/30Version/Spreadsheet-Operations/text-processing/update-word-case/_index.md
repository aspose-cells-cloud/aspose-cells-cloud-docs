---
title: "Aspose.Cells – Update Word Case API"
second_title: "Document"
linktitle: "Word Case"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, Update Word Case API, text case conversion, Excel, CSV, Google Sheets, REST API"
description: "Convert text case in Excel, CSV, or Google Sheets files with Aspose.Cells Cloud’s Update Word Case API. Supports upper‑/lower‑case, title case, and first‑letter capitalization."
weight: 100
---

# **Aspose.Cells – Update Word Case API**

Managing inconsistent text case in spreadsheets (Excel, Google Sheets, CSV) can be frustrating, especially with large datasets. The **PostUpdateWordCase web API** automates text‑case conversions, ensuring clean and standardized data with minimal effort.

## **Interface Details**

### **Endpoint**

```
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

**Authentication** – Include an OAuth 2.0 bearer token in the request header:

```
Authorization: Bearer <access_token>
```

### **Function Description**

The PostUpdateWordCase web API addresses the common issue of inconsistent text case in spreadsheets, which can significantly impact data analysis and processing. This API automates case conversion, ensuring that your data is clean, standardized, and ready for further manipulation or analysis.

- **Automated Text‑Case Conversion**  
  - **Uppercase to Lowercase** – Convert all uppercase letters to lowercase.  
  - **Lowercase to Uppercase** – Convert all lowercase letters to uppercase.  
  - **Capitalize First Letter** – Capitalize the first letter of each word.  
  - **Title Case** – Convert text to title case, where the first letter of each major word is capitalized.

- **Support for Multiple Formats** – The API works with a wide range of spreadsheet formats, including Excel, OpenOffice, JSON, CSV, and others. This versatility makes it suitable for various data‑processing needs.

### Request Parameters of **postUpdateWordCase** API

| Parameter Name   | Type   | Location      | Description |
|------------------|--------|---------------|-------------|
| `wordCaseOptions`| object | Request body  | Options that define the desired case transformation, such as the source range, target case type, and additional settings. |

**`wordCaseOptions` schema**

```json
{
  "Range": "A1:B10",          // Excel‑style range to process (required)
  "CaseType": "Upper",        // Enum: Upper, Lower, Capitalize, Title (required)
  "IgnoreBlank": true         // Boolean, optional – when true, blank cells are left unchanged
}
```

- **Range** – The cell range to which the case conversion will be applied (e.g., `A1:C5`).  
- **CaseType** – The type of case conversion. Allowed values are `Upper`, `Lower`, `Capitalize`, and `Title`.  
- **IgnoreBlank** – If `true`, blank cells are ignored; default is `false`.

### **Response Description**

```json
{
  "Filename": "Result.xlsx",
  "FileSize": 25432,
  "FileContent": "base64_encoded_string"
}
```

- **Filename** – Name of the processed file.  
- **FileSize** – Size of the file in bytes.  
- **FileContent** – Base‑64 encoded content of the transformed file.

### **Prerequisites**

- A valid Aspose Cloud **client‑id** and **client‑secret**.  
- An OAuth 2.0 access token obtained from the Aspose Cloud authentication service.  
- The latest Aspose.Cells Cloud SDK version **≥ 23.9** (or a direct HTTP call).  
- The source spreadsheet must already be uploaded to Aspose Cloud storage.

### **Error Handling**

| HTTP Status | Meaning                              | Sample Error Payload |
|-------------|--------------------------------------|----------------------|
| **200**     | Success – the file is returned.      | N/A |
| **400**     | Bad request – missing or invalid parameters. | `{ "error": "Invalid wordCaseOptions supplied." }` |
| **401**     | Unauthorized – missing or invalid OAuth token. | `{ "error": "Authentication failed." }` |
| **415**     | Unsupported Media Type – file format not supported. | `{ "error": "File format not supported." }` |
| **500**     | Internal server error.               | `{ "error": "An unexpected error occurred." }` |

### **Version / Last Updated**

**API version:** 3.0 – **Last updated:** 2024‑11‑01  

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
 {{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
 {{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
 {{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
 {{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
 {{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
 {{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
 {{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
 {{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}

### Frequently Asked Questions

| Question | Answer |
|----------|--------|
| **What does the Update Word Case API do?** | It converts the text case of cells in an Excel, CSV, or Google Sheets file. You can change uppercase to lowercase, lowercase to uppercase, capitalize the first letter of each word, or apply title case across a specified range. |
| **How do I authenticate a request to the Update Word Case endpoint?** | Include an OAuth 2.0 bearer token in the `Authorization` header: `Authorization: Bearer <access_token>`. The token is obtained from the Aspose Cloud authentication service using your client‑id and client‑secret. |
| **What is the required JSON structure for `wordCaseOptions`?** | ```json { "Range": "A1:B10", "CaseType": "Upper", "IgnoreBlank": true }``` – `Range` (string) specifies the Excel‑style cell range, `CaseType` (enum) is one of `Upper`, `Lower`, `Capitalize`, `Title`, and `IgnoreBlank` (bool, optional) tells the API whether to skip blank cells. |

---