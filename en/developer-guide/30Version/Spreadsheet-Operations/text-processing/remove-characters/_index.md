---
title: "Remove Characters from Excel Worksheets – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Document"
linktitle: "Remove Characters"
type: docs
url: /excel-remove-characters/
keywords: "remove characters, Excel worksheet, Aspose.Cells Cloud API, text cleaning, data sanitization, character removal, Excel API, POST"
description: "Step-by-step guide to using Aspose.Cells Cloud API (POST /cells/removecharacters) to delete custom characters, predefined character sets, or substrings from Excel worksheets. Provides request schema, sample cURL, SDK examples, and error‑handling details."
weight: 100
---

A comprehensive set of tools for cleaning text content within selected cells. The API removes specific characters, predefined character sets, or substrings, ensuring that worksheet text is standardized and free from unwanted symbols.

## Remove Characters from Excel Web API

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

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

### Response Description

```json
{
  "Name": "FileInfo",
  "Description": ["Represents file information."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Filename",
      "Description": ["Represents filename."],
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
      "Description": ["Represents file size."],
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
      "Description": ["Represents file content, byte to base64 string."],
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
