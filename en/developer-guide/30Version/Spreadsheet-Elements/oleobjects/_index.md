---
title: "Working with Excel OLE Objects – Aspose.Cells Cloud REST API Guide"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: ["/working-with-oleobjects/"]
keywords: ["OLE object", "Excel", "Aspose.Cells", "REST API", "cloud"]
description: "Use Aspose.Cells Cloud REST API to retrieve, add, update, delete, and convert OLE objects in Excel worksheets. Includes code examples, SDKs for Java, .NET, Python, PHP, and more."
date: 2024-03-15
lastmod: 2024-06-10
weight: 100
ArticleTitle: "Working with Excel OLE Objects – Guide to Retrieve, Add, Update, Delete, and Convert OLE Objects"
---

## How to work with OLE objects in an Excel worksheet

The Aspose.Cells Cloud REST API provides a complete set of operations to manage OLE objects programmatically. Below is a concise reference for each operation, including the HTTP method, endpoint pattern, required parameters, and a brief example response.

- [How to get an OLE object from an Excel worksheet](/cells/oleobjects/get/)
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameters:** `fileName` (string), `sheetName` (string), `oleObjectIndex` (integer)  
  - **Sample request (`curl`):**  
    ```bash
    curl -v "https://api.aspose.cloud/v3.0/cells/myfile.xlsx/worksheets/Sheet1/oleobjects/0" \
      -H "Authorization: Bearer <token>"
    ```
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
  - **Parameters:** `fileName`, `sheetName`, `oleObject` (binary or base64-encoded file), `imageFormat` (optional)  
  - **Sample request body:** `multipart/form-data` with the OLE file uploaded as the `oleObject` field.  
  - **Sample response:** `201 Created` with `Location` header pointing to the new OLE object.

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
  - **Note:** Use this endpoint to remove **all** OLE objects in the specified worksheet.  
  - **Sample response:** `204 No Content` confirming all OLE objects were removed.

- [How to delete a specific OLE object in an Excel worksheet](/cells/oleobjects/delete/)
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameters:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Note:** Use this endpoint to remove a **specific** OLE object by index.  
  - **Sample response:** `204 No Content` confirming the object was deleted.

For background on Excel OLE objects, see [Understanding OLE Objects in Excel](/cells/oleobjects/understanding/).  
To manage worksheet images, also check [Working with Images](/cells/images/).