---
title: "Aspose.Cells Cloud API – Retrieve File Info (Name, Size, Base64 Content)"
second_title: "Document"
linktitle: "File Info"
type: docs
url: /file-info/
keywords: "Aspose Cells, file info API, Excel file size, Base64 Excel, Cloud storage API"
description: "Retrieve an Excel workbook’s name, size (bytes), and Base64‑encoded content with Aspose.Cells Cloud API. Includes request syntax, sample code, and error handling guidance."
weight: 79
---

## FileInfo Properties

| Name            | Type   | Description                                         |
| --------------- | ------ | --------------------------------------------------- |
| **FileName**    | string | The name of the file, including its extension.      |
| **FileSize**    | long   | The size of the file in bytes.                      |
| **FileContent** | string | Contains the Excel file data encoded in Base64.     |

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