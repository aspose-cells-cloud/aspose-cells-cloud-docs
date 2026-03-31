---  
title: "Worksheet Page Setup"  
second_title: "Document"  
linktitle: "Page setup"  
type: docs  
url: /page-setup/  
keywords: "Aspose.Cells, pageSetup, worksheet, print settings, margins, orientation, paper size, header, footer, scaling"  
description: "Learn how to configure Excel worksheet print layout with Aspose.Cells Cloud’s pageSetup object. Includes property list, defaults, ranges, and code samples for C#, Java, and Python."  
weight: 20  
---  

# **pageSetup**

Excel print page settings  

## Overview  

The **pageSetup** object defines the print‑layout options for an Excel worksheet, such as margins, orientation, scaling, headers, footers, and other print‑related settings. Configuring these properties lets developers produce printable workbooks that match the desired appearance and pagination.

## Prerequisites  

- Aspose.Cells Cloud SDK version **23.12** (or later).  
- Valid authentication token (OAuth 2.0 or JWT).  
- A `Worksheet` instance obtained from a workbook that you intend to modify.

## Code Example  

Below are short snippets that demonstrate how to read a worksheet, modify a few `pageSetup` properties, and save the workbook. Choose the language that matches your project.

```csharp
// C#
var api = new CellsApi("<client_id>", "<client_secret>");
var workbook = api.GetWorksheet("Book1.xlsx", "Sheet1");
workbook.PageSetup.Orientation = OrientationType.Landscape;
workbook.PageSetup.Zoom = 90;               // 90 %
api.UpdateWorksheet("Book1.xlsx", "Sheet1", workbook);
```

```java
// Java
CellsApi api = new CellsApi("<client_id>", "<client_secret>");
Worksheet worksheet = api.getWorksheet("Book1.xlsx", "Sheet1");
worksheet.getPageSetup().setOrientation("Landscape");
worksheet.getPageSetup().setZoom(90);       // 90 %
api.updateWorksheet("Book1.xlsx", "Sheet1", worksheet);
```

```python
# Python
api = CellsApi(client_id, client_secret)
worksheet = api.get_worksheet("Book1.xlsx", "Sheet1")
worksheet.page_setup.orientation = "Landscape"
worksheet.page_setup.zoom = 90              # 90 %
api.update_worksheet("Book1.xlsx", "Sheet1", worksheet)
```

## Properties  

| Property Name            | Property Type | Nullable | ReadOnly | DefaultValue | Description |
|--------------------------|---------------|----------|----------|--------------|-------------|
| BlackAndWhite            | bool          | false    | false    | false        | Prints the worksheet in black‑and‑white mode. |
| BottomMargin             | float         | true     | false    | 2.54 cm      | Size of the bottom margin in centimeters. |
| CenterHorizontally       | bool          | false    | false    | false        | Centers the sheet horizontally when printed. |
| CenterVertically         | bool          | false    | false    | false        | Centers the sheet vertically when printed. |
| FirstPageNumber          | int           | true     | false    | 1            | The first page number used when the sheet is printed. |
| FitToPagesTall           | int           | false    | false    | 1            | Number of pages tall to which the worksheet will be scaled. |
| FitToPagesWide           | int           | false    | false    | 1            | Number of pages wide to which the worksheet will be scaled. |
| FooterMargin             | float         | true     | false    | 2.54 cm      | Distance from the bottom of the page to the footer, in centimeters. |
| HeaderMargin             | float         | true     | false    | 2.54 cm      | Distance from the top of the page to the header, in centimeters. |
| IsAutoFirstPageNumber   | bool          | false    | false    | false        | Assigns the first page number automatically. |
| IsHFAlignMargins         | bool          | false    | false    | true         | When true, header/footer margins align with the page margins. |
| IsHFDiffFirst            | bool          | false    | false    | false        | Indicates that the header/footer on the first page differs from other pages. |
| IsHFDiffOddEven          | bool          | false    | false    | false        | Indicates that the header/footer on odd pages differs from even pages. |
| IsHFScaleWithDoc         | bool          | false    | false    | false        | Scales header and footer together with the document (Excel 2007+). |
| IsPercentScale           | bool          | false    | false    | true         | When false, `FitToPagesWide` and `FitToPagesTall` control scaling. |
| LeftMargin               | float         | true     | false    | 2.54 cm      | Size of the left margin in centimeters. |
| Order                    | string        | true     | false    | "DownThenOver"| The order Excel uses to number pages when printing a large worksheet. |
| Orientation              | string        | false    | false    | "Portrait"   | Page orientation: **Landscape** or **Portrait**. |
| PaperSize                | string        | true     | false    | "A4"         | Paper size used for printing. |
| PrintArea                | string        | true     | false    | (none)       | Range of cells to be printed (e.g., `"A1:D20"`). |
| PrintComments            | string        | true     | false    | "NoComments" | How comments are printed with the sheet. |
| PrintCopies              | int           | true     | false    | 1            | Number of copies to print. |
| PrintDraft               | bool          | false    | false    | false        | Prints the worksheet in draft mode (no graphics). |
| PrintErrors              | string        | true     | false    | "Display"    | Type of print error displayed. |
| PrintGridlines           | bool          | false    | false    | false        | Prints cell gridlines. |
| PrintHeadings            | bool          | false    | false    | false        | Prints row and column headings. |
| PrintQuality             | int           | true     | false    | 600          | Print quality setting (dots per inch). |
| PrintTitleColumns        | string        | true     | false    | (none)       | Columns to repeat on the left side of each printed page. |
| PrintTitleRows           | string        | true     | false    | (none)       | Rows to repeat at the top of each printed page. |
| RightMargin              | float         | true     | false    | 2.54 cm      | Size of the right margin in centimeters. |
| TopMargin                | float         | true     | false    | 2.54 cm      | Size of the top margin in centimeters. |
| Zoom                     | int           | false    | false    | 100          | Scaling factor in percent (10 – 400%). |
| Header                   | object        | true     | false    | (none)       | Page header configuration. |
| Footer                   | object        | true     | false    | (none)       | Page footer configuration. |

> **Note on the *Nullable* column:**  
> `false` indicates that the property must be supplied when creating a `pageSetup` payload; `true` means the property is optional. The default values shown above are applied when an optional property is omitted.

### Sample JSON Payload  

```json
{
  "Orientation": "Landscape",
  "Zoom": 90,
  "TopMargin": 2.54,
  "BottomMargin": 2.54,
  "LeftMargin": 2.54,
  "RightMargin": 2.54,
  "PrintGridlines": false,
  "PrintHeadings": true
}
```

## Related Objects  

- **Header** – Configures the worksheet header.  
- **Footer** – Configures the worksheet footer.  
- **PrintOptions** – Additional print‑related settings such as page breaks and print area.

## FAQ  

**Q:** *How do I set a worksheet to print in landscape mode?*  
**A:** Set the `Orientation` property to `"Landscape"` and then call the appropriate update API (e.g., `UpdateWorksheet`).

**Q:** *What is the default margin size if I don’t specify `TopMargin`?*  
**A:** The default margin is **2.54 cm** (1 inch) for all sides when the property is omitted.

**Q:** *How can I repeat the first row as a title on every printed page?*  
**A:** Assign `"1:1"` to `PrintTitleRows` and ensure `IsHFDiffFirst` is `true`.

---

*Last updated: 2024‑06‑15* &nbsp;|&nbsp; **Version:** v23.12  