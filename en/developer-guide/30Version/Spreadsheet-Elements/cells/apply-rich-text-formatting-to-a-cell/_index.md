---
title: "Apply Rich Text Formatting to a Cell"
description: "Step-by-step guide to applying rich text formatting—such as mixed bold, italic, and font sizes—to individual cells in Excel via Aspose.Cells Cloud REST API, including cURL and SDK examples."
date: 2023-11-15T10:30:00Z
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells Cloud, Excel REST API, rich text formatting, mixed font styles, cell characters, cURL example, SDK integration"
article_type: how-to
---

## Apply Rich Text Formatting to a Cell

This guide explains how to apply **rich text formatting**—where different parts of a cell’s content use distinct fonts, sizes, or styles—to a specific cell in an Excel worksheet using the **Aspose.Cells Cloud REST API**.

### Prerequisites

- ✅ A valid [JWT token](/getting-started/authentication/) for authentication  
- ✅ The target Excel file must already exist in your Aspose.Cells Cloud storage  
- ✅ The Excel file must be in a supported format (e.g., `.xlsx`, `.xls`)  
- ⚠️ The total payload size must not exceed **200 MB** (see [HTTP 413 handling](#http-status-codes))

> 💡 **Tip**: Rich text formatting is ideal for dashboards, reports, or any scenario where visual emphasis (e.g., highlighting key terms) improves data readability.

---

## PostCellCharacters API

Apply formatting to specific character ranges within a cell.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### Request Parameters

| Parameter   | Type   | Location | Description |
|-------------|--------|----------|-------------|
| `name`      | string | path     | Name of the Excel file (e.g., `Book1.xlsx`). |
| `sheetName` | string | path     | Name of the worksheet (e.g., `Sheet1`). |
| `cellName`  | string | path     | Cell address (e.g., `A1`). |
| `options`   | object | body     | JSON object containing an array of `FontSetting` objects. Each defines a character range and its formatting. |
| `folder`    | string | query    | Folder path in storage where the file resides (e.g., `/Reports/Q3`). |
| `storageName` | string | query  | Custom storage name (if using non-default storage). |

#### `options` Body Structure

The `options` object must include a `FontSetting` array, where each item specifies:
- `StartIndex`: Starting position of the range (0-based)
- `Length`: Number of characters to format
- `Font`: Formatting options (e.g., `IsBold`, `IsItalic`, `Size`, `Color`, `Name`)

Example `FontSetting`:
```json
{
  "FontSetting": [
    {
      "Font": { "IsBold": true, "Size": 24 },
      "Length": 5,
      "StartIndex": 0
    },
    {
      "Font": { "IsItalic": true, "Size": 15 },
      "Length": 4,
      "StartIndex": 5
    }
  ]
}
```

> 🔍 **Note**: Fonts apply cumulatively. If `IsBold` is set but `IsItalic` is omitted, only bold formatting is applied to that range.

---

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| `200` | OK                    | Formatting applied successfully. |
| `400` | Bad Request           | Invalid cell name, missing `options`, or unsupported file format. |
| `401` | Unauthorized          | Missing, expired, or invalid JWT token. |
| `413` | Payload Too Large     | Request body exceeds 200 MB limit. |
| `500` | Internal Server Error | Unexpected server-side failure. |

---

### cURL Example

The following command applies **bold 24pt** formatting to the first 5 characters and **italic 15pt** to the next 4 characters in cell `A1` of `Sheet1`:

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <your_jwt_token>" \
-d '{
  "FontSetting": [
    { "Font": { "IsBold": true, "Size": 24 }, "Length": 5, "StartIndex": 0 },
    { "Font": { "IsItalic": true, "Size": 15 }, "Length": 4, "StartIndex": 5 }
  ]
}'
```

**Expected Response**:
```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

### Use Aspose.Cells Cloud SDKs

SDKs simplify integration by handling authentication, serialization, and error handling. All examples below format cell `A1` in `Sheet1` of `Book1.xlsx`.

#### .NET (C#)
```csharp
var api = new CellsApi(clientId, clientSecret);
var request = new PostCellCharactersRequest
{
    Name = "Book1.xlsx",
    SheetName = "Sheet1",
    CellName = "A1",
    Options = new FontSetting[]
    {
        new FontSetting { StartIndex = 0, Length = 5, Font = new Font { IsBold = true, Size = 24 } },
        new FontSetting { StartIndex = 5, Length = 4, Font = new Font { IsItalic = true, Size = 15 } }
    }
};
api.PostCellCharacters(request);
```

#### Java
```java
CellsApi api = new CellsApi(clientId, clientSecret);
Font[] fonts = {
    new Font().isBold(true).size(24),
    new Font().isItalic(true).size(15)
};
FontSetting[] options = {
    new FontSetting().startIndex(0).length(5).font(fonts[0]),
    new FontSetting().startIndex(5).length(4).font(fonts[1])
};
api.postCellCharacters("Book1.xlsx", "Sheet1", "A1", options, null, null);
```

#### Node.js
```javascript
const { CellsApi } = require("aspose-cells-cloud");
const api = new CellsApi(process.env.ASPOSE_CLOUD_CLIENT_ID, process.env.ASPOSE_CLOUD_CLIENT_SECRET);
const options = [
  { font: { isBold: true, size: 24 }, length: 5, startIndex: 0 },
  { font: { isItalic: true, size: 15 }, length: 4, startIndex: 5 }
];
await api.postCellCharacters("Book1.xlsx", "Sheet1", "A1", options);
```

#### Python
```python
from asposecellscloud.api import CellsApi
from asposecellscloud.models import FontSetting, Font

api = CellsApi(client_id, client_secret)
options = [
    FontSetting(font=Font(is_bold=True, size=24), length=5, start_index=0),
    FontSetting(font=Font(is_italic=True, size=15), length=4, start_index=5)
]
api.post_cell_characters("Book1.xlsx", "Sheet1", "A1", options=options)
```

> 📚 **Full SDK Examples**: See the [Aspose.Cells Cloud GitHub organization](https://github.com/aspose-cells-cloud) for language-specific repos (e.g., [`aspose-cells-cloud-dotnet`](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/v24.6), [`aspose-cells-cloud-node`](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/v24.6)).

---

### Related Documentation

- [Authentication Overview](/getting-started/authentication/)  
- [Working with Excel Files](/working-with-excel-files/)  
- [Aspose.Cells Cloud SDK Reference](/sdks/)  
- [Release Notes](https://products.aspose.cloud/cells/release-notes/) (verify `v3.0` compatibility)  

---

### Best Practices

- ✅ **Use semantic folder structures** (e.g., `/reports/2023/`) in the `folder` parameter for easier file management.  
- ✅ **Validate cell names** before sending requests (e.g., `A1`, `Z100`, not `1A`).  
- ✅ **Pre-upload large files** via `/cells` endpoints to avoid payload limits.  
- ✅ **Test formatting ranges** incrementally to prevent overwriting adjacent character styles.  

> 📝 **Accessibility**: If adding screenshots to this documentation, ensure every image includes descriptive alt text (e.g., `alt="Excel cell A1 with 'Hello' in bold 24pt and 'World' in italic 15pt"`).