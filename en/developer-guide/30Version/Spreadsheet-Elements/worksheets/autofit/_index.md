---
title: "Working with Autofit on an Excel Worksheet"
second_title: "Document"
linktitle: "Autofit"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "autofit column, autofit row, Aspose.Cells Cloud, Excel API, resize column, resize row, SDK"
description: "Learn how to automatically resize rows and columns in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL, .NET, Java, and Python examples."
weight: 20
---

## Working with autofit on an Excel worksheet

**Introduction**  
Autofit is a feature of the Aspose.Cells Cloud API that automatically adjusts the height of rows and the width of columns so that the cell contents are fully visible. This operation saves developers from manually calculating dimensions and improves the visual quality of generated spreadsheets. The API works with any Excel file stored in Aspose Cloud storage and is available through REST calls as well as language‑specific SDKs (C#, Java, .NET, Python, Go, Node.js, PHP, Ruby, Swift, and Android). Using autofit is especially useful after inserting or updating data, applying styles, or importing large data sets where column widths and row heights are unknown in advance.

### Prerequisites
- A valid Aspose Cloud **client ID** and **client secret**.  
- The workbook must be uploaded to Aspose Cloud storage (or provided as a base‑64 stream).  
- API version **v3.0** (default) is used in the examples below.  

### How‑to autofit

#### Column
To autofit a single column, call the `POST /cells/{file}/worksheets/{sheet}/autofit` endpoint with `type=column` and the column index.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/autofit?type=column&column=2" \
     -H "Authorization: Bearer {access_token}"
```

**Parameters**  
- `type` – must be `column`.  
- `column` – zero‑based index of the column to resize.

#### Columns
To autofit a range of columns, set `type=columns` and optionally specify `firstColumn` and `lastColumn`.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/autofit?type=columns&firstColumn=0&lastColumn=4" \
     -H "Authorization: Bearer {access_token}"
```

#### Row
Autofit a single row by using `type=row` and the row index.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/autofit?type=row&row=5" \
     -H "Authorization: Bearer {access_token}"
```

#### Rows
Autofit multiple rows with `type=rows` and optional `firstRow` / `lastRow` parameters.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/autofit?type=rows&firstRow=0&lastRow=10" \
     -H "Authorization: Bearer {access_token}"
```

### Response
A successful request returns HTTP **200 OK** with an empty body. Errors are reported with standard HTTP status codes:

| Code | Meaning                                 |
|------|-----------------------------------------|
| 200  | Autofit operation completed successfully |
| 400  | Invalid parameters or missing required fields |
| 401  | Authentication failed or token expired   |
| 404  | Specified workbook, worksheet, or range not found |
| 500  | Server‑side error                        |

### See also
- [Resize columns and rows](/cells/worksheets/resize/)  
- [Set column width](/cells/worksheets/setcolumnwidth/)  
- [Set row height](/cells/worksheets/setrowheight/)

---

- [How to autoFit a column on an Excel worksheet.](/cells/worksheets/autofit/column/)
- [How to autoFit columns on an Excel worksheet.](/cells/worksheets/autofit/columns/)
- [How to autoFit a row on an Excel worksheet.](/cells/worksheets/autofit/row/)
- [How to autoFit rows on an Excel worksheet.](/cells/worksheets/autofit/rows/)