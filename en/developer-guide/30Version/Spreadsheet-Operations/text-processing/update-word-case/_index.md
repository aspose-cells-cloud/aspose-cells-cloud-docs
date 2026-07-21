---
title: "Aspose.Cells – Update Word Case API"
second_title: "Document"
linktitle: "Word Case"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, Update Word Case API, text case conversion, Excel, CSV, Google Sheets, REST API"
description: "Convert text case in Excel, CSV, or Google Sheets files with Aspose.Cells Cloud’s Update Word Case API. Supports upper‑/lower‑case, title case, and first‑letter capitalization."
weight: 100
ArticleTitle: "Aspose.Cells – Update Word Case API Documentation"
---

**API version:** 3.0

Managing inconsistent text case in spreadsheets (Excel, Google Sheets, CSV) can be frustrating, especially with large datasets. The **PostUpdateWordCase web API** automates text‑case conversions, ensuring clean and standardized data with minimal effort.


## **Excel Web API – Update Word Case API**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### **Function Description**

The PostUpdateWordCase web API addresses the common issue of inconsistent text case in spreadsheets, which can significantly impact data analysis and processing. This API automates case conversion, ensuring that your data is clean, standardized, and ready for further manipulation or analysis.

- **Automated Text‑Case Conversion**
  - **Uppercase to Lowercase** – Convert all uppercase letters to lowercase.
  - **Lowercase to Uppercase** – Convert all lowercase letters to uppercase.
  - **Capitalize First Letter** – Capitalize the first letter of each word.
  - **Title Case** – Convert text to title case, where the first letter of each major word is capitalized.

- **Support for Multiple Formats** – The API works with a wide range of spreadsheet formats, including Excel, OpenOffice, JSON, CSV, and others. This versatility makes it suitable for various data‑processing needs.

### **Request Parameters**

| Parameter Name    | Type   | Location     | Description                                                                                                               |
| ----------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | object | Request body | Options that define the desired case transformation, such as the source range, target case type, and additional settings. |

**`wordCaseOptions` schema**

```json
{
  "Range": "A1:B10", // Excel‑style range to process (required)
  "CaseType": "Upper", // Enum: Upper, Lower, Capitalize, Title (required)
  "IgnoreBlank": true // Boolean, optional – when true, blank cells are left unchanged
}
```

- **Range** – The cell range to which the case conversion will be applied (e.g., `A1:C5`).
- **CaseType** – The type of case conversion. Allowed values are `Upper`, `Lower`, `Capitalize`, and `Title`.
- **IgnoreBlank** – If `true`, blank cells are ignored; default is `false`.

### **Response**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[merged filename]",
    "Filesize" : [file size],
    "FileContent" : "[Base64String]"
}
```

- **Filename** – Name of the processed file.
- **FileSize** – Size of the file in bytes.
- **FileContent** – Base‑64 encoded content of the transformed file.

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the PostUpdateWordCase API with SDKs

### PostUpdateWordCase API Specification

The <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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