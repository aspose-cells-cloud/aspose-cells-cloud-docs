---
title: "File Info"
second_title: "Document"
linktitle: "File Info"
type: docs
url: /file-info/
keywords: "File Info, Excel file metadata, Base64 file content, Aspose.Cells Cloud API"
description: "Get Excel file name, size, and Base64 content via Aspose.Cells Cloud API. Learn request syntax, sample code, and error handling."
weight: 79
---

## FileInfo Properties

| Name            | Type   | Description                                         |
| --------------- | ------ | --------------------------------------------------- |
| **FileName**    | string | The name of the file, including its extension.      |
| **FileSize**    | long   | The size of the file in bytes.                      |
| **FileContent** | string | Contains the raw Excel file data encoded in Base64. |

### Errors

| HTTP Code | Meaning                 | When It Occurs                           |
| --------- | ----------------------- | ---------------------------------------- |
| 200       | OK – request succeeded. | Normal response.                         |
| 401       | Unauthorized            | Missing or invalid authentication token. |
| 404       | Not Found               | The specified file does not exist.       |
| 500       | Internal Server Error   | Unexpected server‑side failure.          |

## See Also

- [Get Workbook](https://docs.aspose.cloud/cells/get-workbook)
- [Download File](https://docs.aspose.cloud/cells/download-file)
- [Authentication Overview](https://docs.aspose.cloud/cells/authentication)
