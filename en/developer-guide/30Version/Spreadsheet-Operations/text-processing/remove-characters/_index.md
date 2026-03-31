---
title: "Remove Characters from Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Document"
linktitle: "Remove Characters"
type: docs
url: /excel-remove-characters/
keywords: "remove characters, Excel, Aspose.Cells Cloud, API, POST, text cleaning, data sanitization"
description: "Learn how to use Aspose.Cells Cloud API to delete custom characters, character sets, or substrings from Excel worksheets. Includes request schema, sample cURL, SDK code, and error handling."
weight: 100
---

# Remove Characters from Excel (PostRemoveCharacters) – Aspose.Cells Cloud API

A comprehensive set of tools for cleaning text content within selected cells. The API removes specific characters, predefined character sets, or substrings, ensuring that worksheet text is standardized and free from unwanted symbols.

## Interface Details

### Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

> **Authentication** – The endpoint requires an OAuth 2.0 bearer token. Obtain a token via `POST https://api.aspose.cloud/connect/token` using your client‑id and client‑secret, then include `Authorization: Bearer <access_token>` in the request header.

### Function Description

- **Remove custom characters** – Specify any characters you want to delete. Enter each character in the *Remove custom characters* field; the API will delete every occurrence of those characters in the selected cells.  
- **Remove character sets** – Choose from the predefined sets:
  - **Non‑printing characters** – Deletes line‑breaks and the first 32 non‑printing ASCII characters (0‑31) plus additional codes (127, 129, 141, 143, 144, 157).  
  - **Text characters** – Removes all letters.  
  - **Numeric characters** – Deletes all digits.  
  - **Symbols** – Removes mathematical, geometric, technical, currency symbols and letter‑like symbols such as “?”, “1”, and “™”.  
  - **Punctuation marks** – Eliminates all punctuation.  
- **Remove a substring** – Deletes any specified substring (e.g., a word) from the selected cells.

### Request Parameters

| Parameter Name          | Type   | Location | Description                                                                 |
|-------------------------|--------|----------|-----------------------------------------------------------------------------|
| removeCharactersOptions | Class  | Body     | Options that define which characters, character sets, or substrings to remove. |

**Schema of `removeCharactersOptions`**

| Property          | Type    | Required | Description                                                                 |
|-------------------|---------|----------|-----------------------------------------------------------------------------|
| Range             | string  | Yes      | A‑1 notation or named range that identifies the cells to process (e.g., `"A1:C10"`). |
| CustomCharacters  | string  | No       | A string containing each custom character to delete (e.g., `"@#$"`). |
| CharacterSet      | string  | No       | Enum value specifying a predefined set (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring         | string  | No       | The exact substring to remove (e.g., `"USD"`). |
| IgnoreCase        | boolean | No       | When `true`, character removal is case‑insensitive. |

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

### Response Description

```json
{
  "Name": "FileInfo",
  "Description": [
    "Represents file information."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Filename",
      "Description": [
        "Represents filename."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    },
    {
      "Name": "FileSize",
      "Description": [
        "Represents file size."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "FileContent",
      "Description": [
        "Represents file content, byte to base64 string."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

> *(SDK examples remain unchanged as per the Cloud SDK Family requirement.)*

---

### FAQ (Frequently Asked Questions)

**Q:** How do I remove all non‑printing characters from a worksheet using Aspose.Cells Cloud?  
**A:** Send a POST request to `https://api.aspose.cloud/v3.0/cells/removecharacters` with a JSON body where `"CharacterSet"` is set to `"NonPrinting"` and `"Range"` points to the target cells. Include your OAuth 2.0 bearer token in the `Authorization` header. The response returns a `FileInfo` object containing the updated workbook.

**Q:** What authentication method is required for the RemoveCharacters endpoint?  
**A:** The API uses OAuth 2.0. Obtain an access token via `POST https://api.aspose.cloud/connect/token` with your client‑id and client‑secret, then pass `Authorization: Bearer <access_token>` on every request, including the RemoveCharacters call.

**Q:** Can I remove a specific substring (e.g., “USD”) from cells in column B?  
**A:** Yes. Set `"Substring"` to `"USD"` and `"Range"` to `"B:B"`. Optionally set `"IgnoreCase"` to `true` for case‑insensitive removal.

**Q:** What error responses might I encounter?  
**A:** Common status codes include `400 Bad Request` (invalid JSON or missing required fields), `401 Unauthorized` (invalid or missing token), `404 Not Found` (specified file or range does not exist), and `500 Internal Server Error` (unexpected server condition). Error bodies are returned in JSON with `Code` and `Message` fields.

**Q:** Do I need to upload the workbook before calling this endpoint?  
**A:** If the workbook is already stored in Aspose Cloud storage, provide its name in the request URL. Otherwise, upload the file first using the `UploadFile` endpoint, then reference it in the `removeCharactersOptions` request.