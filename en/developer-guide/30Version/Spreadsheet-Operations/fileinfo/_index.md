---
title: "File Info"
second_title: "Document"
linktitle: "File Info"
type: docs
url: /file-info/
keywords: "File, Info, Excel, Aspose.Cells, Cloud API, Metadata, Base64"
description: "Retrieve Excel file name, size, and Base64 content using Aspose.Cells Cloud API. Includes request syntax, sample code, and error handling."
weight: 79
ArticleTitle: "File Info – Excel File Metadata and Base64 Content (Aspose.Cells Cloud API)"
---

## FileInfo Properties


| Name            | Type   | Description                                         |
| --------------- | ------ | --------------------------------------------------- |
| **FileName**    | string | The name of the file, including its extension.      |
| **FileSize**    | long   | The size of the file in bytes.                      |
| **FileContent** | string | Contains the raw Excel file data encoded in Base64. |

The response is returned as JSON with the same three properties shown in the table above, for example:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Errors

| HTTP Code | Meaning                 | When It Occurs                           |
| --------- | ----------------------- | ---------------------------------------- |
| 200       | OK – request succeeded. | Normal response.                         |
| 401       | Unauthorized            | Missing or invalid authentication token. |
| 404       | Not Found               | The specified file does not exist.       |
| 500       | Internal Server Error   | Unexpected server‑side failure.          |

For each error, ensure the authentication token is valid (401), verify the file path (404), or consult the generic error‑handling guide for retry strategies (500).

## See Also

- [Get Workbook](https://docs.aspose.cloud/cells/get-workbook) – retrieve a workbook object and its worksheets.  
- [Download File](https://docs.aspose.cloud/cells/download-file) – download raw file bytes without Base64 encoding.  
- [Authentication Overview](https://docs.aspose.cloud/cells/authentication) – how to obtain and use access tokens.  