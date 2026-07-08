---
title: "Add or Delete Worksheet Background Image – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Background"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, worksheet background, Excel API, add background image, delete worksheet background, SDK examples"
description: "Learn how to add or remove a background image on an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax, SDK examples for Java, .NET, Python, PHP, and error handling."
weight: 20
ArticleTitle: "Add or Delete Worksheet Background Image with Aspose.Cells Cloud API"
---

## Working with background on an Excel worksheet

**Overview:** A worksheet background is an image that appears behind the cells of a worksheet, useful for branding or visual cues. Aspose.Cells Cloud API lets you add or delete this background image programmatically.

**Prerequisites:**  
- Valid Aspose.Cells Cloud access token (OAuth 2.0).  
- An Excel workbook stored in the cloud.  
- An image file (PNG, JPEG, BMP) for the background.

- **Add background** – Set a background image on a worksheet. See the detailed guide [How to set background on an Excel worksheet](/cells/worksheets/background/add/).  
- **Delete background** – Remove an existing background image from a worksheet. See the detailed guide [How to delete background on an Excel worksheet](/cells/worksheets/background/delete/).

Using a worksheet background can improve branding, highlight important sections, or provide visual cues for end‑users. The Aspose.Cells Cloud API makes it straightforward to set or clear this background image directly from your application.

### API reference

| Operation | HTTP Method | Endpoint | Path parameters | Request body | Success response |
|-----------|-------------|----------|----------------|--------------|------------------|
| Add background | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – workbook file name<br>`sheetName` – target worksheet | Image file (PNG, JPEG, BMP) as multipart/form‑data | `200 OK` – background applied |
| Delete background | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – workbook file name<br>`sheetName` – target worksheet | *none* | `200 OK` – background removed |

#### Example (Java SDK)

```java
// Add a background image
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Delete the background image
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Example (Python SDK)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# Add background
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Delete background
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

For additional language examples (C#, PHP, Ruby), refer to the SDK documentation.

**Related topics**  
- Learn more about managing worksheets in general: [Worksheets overview](/cells/worksheets/).  
- Understand how to authenticate with Aspose.Cells Cloud: [API authentication guide](/cells/authentication/).  
- Explore other spreadsheet elements such as charts, tables, and formulas: [Spreadsheet elements index](/cells/elements/).