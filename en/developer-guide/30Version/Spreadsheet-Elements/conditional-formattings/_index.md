---
title: "Working with Excel Conditional Formatting"
second_title: "Document"
linktitle: "Conditional Formatting"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, Conditional Formatting, Aspose.Cells Cloud, API"
description: "The Aspose.Cells Cloud API for Excel provides endpoints to retrieve, add, modify, and clear conditional formatting rules, enabling dynamic visual analysis of worksheet data."
weight: 100
ArticleTitle: "Working with Excel Conditional Formatting – API Guide"
---

Conditional formatting in Excel enables you to highlight cells with a specific color, depending on the cell’s value.

Use conditional formatting to help you visually explore and analyze data, detect critical issues, and identify patterns and trends.

Conditional formatting makes it easy to highlight interesting cells or ranges of cells, emphasize unusual values, and visualize data by using data bars, color scales, and icon sets that correspond to specific variations in the data.

A conditional format changes the appearance of cells based on the conditions you specify. If the conditions are true, the cell range is formatted; if the conditions are false, the cell range remains unchanged. There are many built‑in conditions, and you can also create your own (including by using a formula that evaluates to **TRUE** or **FALSE**).

The Aspose.Cells Cloud API provides a set of endpoints to manage conditional formatting rules programmatically. The following operations are available:

- **Get Conditional Formattings of Worksheet** – Retrieves all conditional formatting rules applied to a worksheet.  
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parameters:** `fileName` (string, required), `sheetName` (string, required), optional query parameters such as `folder`, `storageName`  
  - **Example cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Get Conditional Formatting** – Returns a specific conditional formatting rule by its identifier.  
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parameters:** `index` (int, required) identifies the rule position.  
  - **Example cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Add a Cell Area for Format Condition** – Adds a cell range that the specified conditional format will affect.  
  - **Method:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Request Body (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Example cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Add a Condition for Format Condition** – Defines a new condition (e.g., value, formula) for an existing format rule.  
  - **Method:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Request Body (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Example cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Add a Format Condition** – Creates a complete conditional formatting rule, including type and style.  
  - **Method:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Request Body (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Example cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Clear All Condition Formattings** – Removes every conditional formatting rule from the target worksheet.  
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Example cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Remove Cell Area from Conditional Formatting** – Deletes a previously defined cell area from a conditional formatting rule.  
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Example cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Remove Conditional Formatting** – Deletes an entire conditional formatting rule from the worksheet.  
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Example cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

These examples illustrate the required HTTP method, URL pattern, key parameters, and sample request payloads for each operation. Use the appropriate SDK (C#, Java, Python, etc.) for language‑specific code snippets if preferred.