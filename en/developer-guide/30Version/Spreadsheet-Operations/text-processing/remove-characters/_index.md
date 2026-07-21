---
title: "Remove Characters from Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Document"
linktitle: "Remove Characters"
type: docs
url: /excel-remove-characters/
keywords: "remove characters, Aspose.Cells, Excel API, text processing, cloud"
description: "Learn how to remove characters, character sets, or substrings from Excel worksheets using Aspose.Cells Cloud API. Includes request schema, cURL example, SDK code, and error handling."
weight: 100
ArticleTitle: "Remove Characters from Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Remove Characters from Excel Web API

A comprehensive set of tools for cleaning text content within selected cells. The API removes specific characters, predefined character sets, or substrings, ensuring that worksheet text is standardized and free from unwanted symbols.


```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Function Description

- **Remove custom characters** – Specify any characters you want to delete. Enter each character in the _Remove custom characters_ field; the API will delete every occurrence of those characters in the selected cells.  
- **Remove character sets** – Choose from the predefined sets:  
  - **Non‑printing characters** – Deletes line‑breaks and the first 32 non‑printing ASCII characters (0‑31) plus additional codes (127, 129, 141, 143, 144, 157).  
  - **Text characters** – Removes all letters.  
  - **Numeric characters** – Deletes all digits.  
  - **Symbols** – Removes mathematical, geometric, technical, currency symbols and letter‑like symbols such as “?”, “1”, and “™”.  
  - **Punctuation marks** – Eliminates all punctuation.  
- **Remove a substring** – Deletes any specified substring (e.g., a word) from the selected cells.

### Request Parameters

| Parameter Name          | Type  | Location | Description                                                                    |
| ----------------------- | ----- | -------- | ------------------------------------------------------------------------------ |
| removeCharactersOptions | Class | Body     | Options that define which characters, character sets, or substrings to remove. |

**Schema of `removeCharactersOptions`**

| Property         | Type    | Required | Description                                                                                                    |
| ---------------- | ------- | -------- | -------------------------------------------------------------------------------------------------------------- |
| Range            | string  | Yes      | A‑1 notation or named range that identifies the cells to process (e.g., `"A1:C10"`).                           |
| CustomCharacters | string  | No       | A string containing each custom character to delete (e.g., `"@#$"`).                                           |
| CharacterSet     | string  | No       | Enum value specifying a predefined set (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | string  | No       | The exact substring to remove (e.g., `"USD"`).                                                                 |
| IgnoreCase       | boolean | No       | When `true`, character removal is case‑insensitive.                                                            |

**Example JSON request body**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Sample cURL request**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

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

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the PostRemoveCharacters API with SDKs

### PostRemoveCharacters API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs: