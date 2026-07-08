---
title: "How to Add Rows to an Excel Worksheet"
second_title: "Document"
linktitle: "Add"
type: docs
url: /rows/add/
keywords: "Aspose.Cells, add rows, Excel API, REST, C#, Java, Python, Node.js"
description: "Step‑by‑step guide to add single or multiple rows to an Excel worksheet using Aspose.Cells Cloud REST API, with code samples for C#, Java, Python, and Node.js."
weight: 20
ArticleTitle: "Add Rows to Excel Worksheet using Aspose.Cells Cloud API – Step‑by‑Step Guide"
---

## How to Add Rows to an Excel Worksheet

This article explains how to insert a single empty row or multiple rows into an existing worksheet by using the Aspose.Cells Cloud REST API. Ensure you have a valid API key and the appropriate SDK installed before proceeding.

**Prerequisites**  
- Aspose.Cells Cloud account with an active subscription.  
- API key/Access token generated from the Aspose Cloud dashboard.  
- One of the supported SDKs (C#, Java, Python, Node.js) installed and configured.  

**API Reference**  
- **HTTP Method:** `POST`  
- **Endpoint:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Required Path Parameters:**  
  - `fileName` – Name of the Excel file stored in the cloud.  
  - `sheetName` – Name of the worksheet where rows will be added.  
- **Query Parameters:**  
  - `startrow` – Zero‑based index of the row at which insertion begins.  
  - `totalRows` – Number of rows to insert.  
  - `folder` – (Optional) Cloud folder path of the file.  
  - `storage` – (Optional) Storage name if using a non‑default storage.  
- **Request Body (JSON example):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

- **Successful Response (HTTP 200):** Returns the updated worksheet information, including the new row count.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Status Codes:**  

  | Code | Meaning                              |
  |------|--------------------------------------|
  | 200  | Rows added successfully              |
  | 400  | Invalid parameters or malformed JSON |
  | 401  | Authentication failed                |
  | 404  | File or worksheet not found          |
  | 500  | Server error                         |

Below are quick links to the detailed examples for adding rows:

- [How to add an empty row on an Excel worksheet](/cells/rows/add/row/)
- [How to add multiple rows on an Excel worksheet](/cells/rows/add/rows/)