---
title: "Working with Excel OLE Objects"
second_title: "Document"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: [/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Use the Aspose.Cells Cloud REST API to retrieve, add, update, delete, and convert OLE objects in Excel worksheets. SDKs are available for Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift, and Android."
weight: 100
ArticleTitle: "Working with Excel OLE Objects – Guide to Retrieve, Add, Update, Delete, and Convert OLE Objects"
---

**How to work with OLE objects in an Excel worksheet**

The Aspose.Cells Cloud REST API provides a complete set of operations to manage OLE objects programmatically. Below is a concise reference for each operation, including the HTTP method, endpoint pattern, required parameters, and a brief example response.

- [How to get an OLE object from an Excel worksheet](/cells/oleobjects/get/)
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameters:** `fileName` (string), `sheetName` (string), `oleObjectIndex` (integer)  
  - **Sample response:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [How to add an OLE object into an Excel worksheet](/cells/oleobjects/add/)
  - **Method:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parameters:** `fileName`, `sheetName`, `oleObject` (binary or base‑64), `imageFormat` (optional)  
  - **Sample request body:** multipart/form‑data with the file stream.  
  - **Sample response:** `201 Created` with location header of the new OLE object.

- [How to update a specific OLE object in an Excel worksheet](/cells/oleobjects/update/)
  - **Method:** `PUT`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameters:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (updated content)  
  - **Sample response:** `200 OK` with updated object metadata.

- [How to convert an OLE object to an image in an Excel worksheet](/cells/oleobjects/convert/)
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parameters:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (e.g., `png`, `jpeg`)  
  - **Sample response:** Binary image stream of the converted OLE object.

- [How to delete all OLE objects in an Excel worksheet](/cells/oleobjects/clear/)
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parameters:** `fileName`, `sheetName`  
  - **Sample response:** `204 No Content` indicating all OLE objects were removed.

- [How to delete a specific OLE object in an Excel worksheet](/cells/oleobjects/delete/)
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameters:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Sample response:** `204 No Content` confirming the object was deleted.