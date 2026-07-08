---
title: "Working with Excel Metadata & Properties"
second_title: "Document"
linktitle: "Metadata & Properties"
type: docs
url: /metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel metadata, document properties API, REST API, GET metadata, update Excel properties, delete Excel metadata"
description: "Learn how to read, add, update, and delete Excel file metadata using Aspose.Cells Cloud REST API. Includes examples for cURL and SDKs across Java, .NET, Python, Node.js, and more."
ArticleTitle: "Working with Excel Metadata and Document Properties – Aspose.Cells Cloud"
weight: 100
---

Excel files can store a variety of metadata that helps identify, organize, and manage the documents. Aspose.Cells Cloud provides a straightforward REST API for reading, adding, updating, and deleting this metadata, enabling developers to integrate document‑property management into their applications. This guide covers the two main categories of properties—standard and custom—explains how to work with them, and supplies direct links to the relevant API endpoints. You’ll also find a concise API reference table with request details to accelerate implementation.

**Last updated:** July 8, 2026  

**Types of document properties**

Before learning how to use Aspose.Cells Cloud APIs to view, modify, and remove document properties (metadata) in Excel, let's clarify the kinds of properties an Excel document can have.

- **Standard properties** are common to Excel. They contain basic information such as Title, Subject, Author, Category, etc. You can assign custom text values to these properties to make the file easier to locate.

- **Custom properties** are user‑defined. They allow you to add additional metadata to your Excel document.

**How to work with document properties on an Excel file**

- [How to get a particular document property using storage](/cells/document-properties/get/)
- [How to get document properties without using storage](/cells/metadata/get/)
- [How to get all document properties using storage](/cells/document-properties/get-all/)
- [How to update a particular document property using storage](/cells/document-properties/update/)
- [How to update a particular document property without using storage](/cells/metadata/update/)
- [How to remove a particular document property using storage](/cells/document-properties/delete/)
- [How to remove document properties without using storage](/cells/metadata/delete/)
- [How to remove all document properties using storage](/cells/document-properties/clear/)

**API reference (without storage)**  

| Method | Endpoint | Description |
|--------|----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Retrieves all document properties of the workbook stored in the cloud. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Retrieves the value of a specific property (standard or custom) identified by `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Updates the value of an existing property. The request body contains the new value in JSON format. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Deletes a specific property from the workbook. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Clears all custom and standard properties from the workbook. |

*All requests require an OAuth 2.0 access token and may include optional query parameters such as `storage` and `folder` when a specific storage location is used.*