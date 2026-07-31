---
title: "Working with Excel pictures"
second_title: "Document"
linktitle: "Pictures"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, picture, Aspose.Cells Cloud, REST API, image handling, Excel pictures"
description: "Learn how to retrieve, add, update, and delete pictures in Excel worksheets using Aspose.Cells Cloud REST API. Includes code samples for C#, Java, Python, and more."
weight: 100
ArticleTitle: "Working with Excel pictures – Aspose.Cells Cloud Documentation"
---

## Working with pictures on an Excel file

This guide explains how to work with **pictures** (also called images) in Excel worksheets through the Aspose.Cells Cloud REST API. It covers the main picture‑related operations—retrieving, adding, updating, and deleting Excel pictures—and points you to detailed examples for each task.

**Prerequisites**: an Aspose.Cells Cloud account, a valid API key, and the appropriate SDK installed for your chosen language.

- [How to get a specific format picture from an Excel worksheet.](/cells/pictures/get/) – Retrieve a single picture in the requested format (PNG, JPEG, etc.) from a worksheet.  
- [How to get all pictures information from an Excel worksheet.](/cells/pictures/get-all/) | List metadata for every picture contained in a worksheet.  
- [How to add a picture for an Excel worksheet.](/cells/pictures/add/) – Insert a new picture into a worksheet, specifying its position and size.  
- [How to update a specific picture from an Excel worksheet.](/cells/pictures/update/) – Modify the properties (e.g., dimensions, placement) of an existing picture.  
- [How to delete all pictures from an Excel worksheet.](/cells/pictures/clear/) – Remove every picture object from a worksheet in a single call.  
- [How to delete a picture from an Excel worksheet.](/cells/pictures/delete/) – Delete a single picture identified by its index.  

**API reference**

**Get a specific format picture**  

| HTTP Method | Endpoint | Required Parameters | Sample Request | Sample Response | Status Codes |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path), `format` (query) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Binary image data (PNG, JPEG, etc.) | 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Server Error |

**Get all pictures information**  

| HTTP Method | Endpoint | Required Parameters | Sample Request | Sample Response | Status Codes |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | JSON array with picture metadata (index, name, position, size) | 200 OK, 400, 401, 404, 500 |

**Add a picture**  

| HTTP Method | Endpoint | Required Parameters | Sample Request Body | Sample Response | Status Codes |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `{ "image": "<base64‑encoded‑image>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Created, 400, 401, 404, 500 |

**Update a picture**  

| HTTP Method | Endpoint | Required Parameters | Sample Request Body | Sample Response | Status Codes |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Delete all pictures**  

| HTTP Method | Endpoint | Required Parameters | Sample Request | Sample Response | Status Codes |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**Delete a specific picture**  

| HTTP Method | Endpoint | Required Parameters | Sample Request | Sample Response | Status Codes |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**Related topics**

Explore other image‑related operations in Aspose.Cells Cloud:  
- [Working with Shapes](/cells/shapes/) – add, edit, and delete drawing shapes.  
- [Working with Charts](/cells/charts/) – create and manipulate chart objects.  
- [Working with Images in Worksheets](/cells/images/) – embed and manage raw image files.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Working with Excel pictures – Aspose.Cells Cloud Documentation",
  "description": "Guide for retrieving, adding, updating, and deleting Excel pictures via Aspose.Cells Cloud REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel pictures, Aspose.Cells Cloud, REST API, image handling",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>