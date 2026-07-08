---
title: "Working with Excel Comments"
second_title: "Document"
linktitle: "Comments"
type: docs
url: /comments/
aliases: [/working-with-comments/]
keywords: "Excel comments, cell notes, comment box, Aspose Cells Cloud API, REST API, spreadsheet annotation"
description: "Learn how to programmatically add, retrieve, update, and delete Excel comments using the Aspose.Cells Cloud REST API (v3.0). Includes request/response examples, prerequisites, version info, and error‑handling guidance."
weight: 100
ArticleTitle: "Working with Excel Comments – Aspose.Cells Cloud API Guide"
---

When creating an Excel workbook, users can add comments for various reasons. A common use is to explain a formula in a cell, especially when the file will be shared with others. Comments can also serve as reminders, notes for collaborators, or as a means of cross‑referencing with other workbooks. Once a comment has been added, Excel allows users to resize, reshape, and format the comment box to suit their preferred style. Mastering comment management helps users get the most out of this feature.

**Prerequisites**

- An active Aspose.Cells Cloud account.  
- A valid **access token** obtained via OAuth 2.0.  
- API version **v3.0** (the endpoints used in this guide belong to this version).  
- Optional: Aspose.Cells SDK for your preferred language to simplify request construction.

**Version**

The examples below target **Aspose.Cells Cloud REST API v3.0**. Future API releases may introduce additional parameters or modify response structures; always consult the latest API reference for up‑to‑date details.

**Add a Comment**

To add a comment, send a **POST** request to the following endpoint:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Path parameters**

| Parameter | Type   | Required | Description                              |
|-----------|--------|----------|------------------------------------------|
| `file`    | string | Yes      | Name of the workbook file (including extension). |
| `sheet`   | string | Yes      | Worksheet name where the comment will be added. |

**Request body schema**

| Field     | Type   | Required | Description                              |
|-----------|--------|----------|------------------------------------------|
| `CellName`| string | Yes      | A1‑style address of the cell (e.g., **B2**). |
| `Comment` | string | Yes      | Text of the comment to be stored. |
| `Author`  | string | No       | Name of the comment author. |

**Sample request body**

```json
{
  "CellName": "B2",
  "Comment": "Review needed",
  "Author": "John Doe"
}
```

**Sample successful response** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "John Doe",
    "HtmlComment": "Review needed",
    "Note": "Review needed"
  }
}
```

**Common error codes**

| Code | Meaning                              |
|------|--------------------------------------|
| 400  | Invalid cell address or request body |
| 401  | Unauthorized – missing/invalid token |
| 404  | Workbook or worksheet not found      |

**Get Comments**

Retrieve all comments from a worksheet:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Path parameters**

| Parameter | Type   | Required | Description                              |
|-----------|--------|----------|------------------------------------------|
| `file`    | string | Yes      | Workbook file name. |
| `sheet`   | string | Yes      | Worksheet name. |

**Sample response**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "Initial value",
      "Note": "Initial value"
    },
    {
      "CellName": "B2",
      "Author": "John Doe",
      "HtmlComment": "Review needed",
      "Note": "Review needed"
    }
  ]
}
```

**Update a Comment**

To modify an existing comment, send a **PUT** request. The comment is identified by its **index** in the worksheet’s comment collection (starting at 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Path parameters**

| Parameter      | Type   | Required | Description |
|----------------|--------|----------|-------------|
| `file`         | string | Yes      | Workbook file name. |
| `sheet`        | string | Yes      | Worksheet name. |
| `commentIndex` | int    | Yes      | Zero‑based index of the comment to update. |

**Request body schema**

| Field    | Type   | Required | Description |
|----------|--------|----------|-------------|
| `Comment`| string | Yes      | New comment text. |
| `Author` | string | No       | Updated author name (optional). |

**Sample request body**

```json
{
  "Comment": "Updated note text",
  "Author": "John Doe"
}
```

The response follows the same structure as the **Add a Comment** response.

**Delete a Comment**

Remove a single comment by its index:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Path parameters**

| Parameter      | Type   | Required | Description |
|----------------|--------|----------|-------------|
| `file`         | string | Yes      | Workbook file name. |
| `sheet`        | string | Yes      | Worksheet name. |
| `commentIndex` | int    | Yes      | Zero‑based index of the comment to delete. |

A successful deletion returns:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Delete All Comments**

To clear every comment from a worksheet:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Path parameters**

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `file`    | string | Yes      | Workbook file name. |
| `sheet`   | string | Yes      | Worksheet name. |

**Error‑handling guidance**

- **404 Not Found** – Verify that the workbook ID, worksheet name, and comment index are correct.  
- **400 Bad Request** – Check JSON syntax and required fields (`CellName`, `Comment`).  
- **429 Too Many Requests** – Implement exponential back‑off and respect the `Retry-After` header.

**Summary**

- Excel comments are used to [add a note or explain a formula in a cell](/cells/comments/add/).  
- Excel provides users with the flexibility of [editing](/cells/comments/update/), [deleting](/cells/comments/delete/), and [showing](/cells/comments/get/) or [hiding](/cells/comments/update/) comments on a worksheet.  
- Users can also [resize](/cells/comments/update/) and [move](/cells/comments/update/) the comment box.  

For more information on working with other spreadsheet elements, see the guide on [working with cells](/cells/working-with-cells/).