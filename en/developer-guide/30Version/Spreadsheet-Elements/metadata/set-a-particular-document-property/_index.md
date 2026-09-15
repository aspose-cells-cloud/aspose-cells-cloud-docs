---
title: "Update (Set) Document Property"
date: 2024-05-12T08:00:00Z
lastmod: 2024-05-12T08:00:00Z
description: "Learn how to update (set) or add a document property in Excel files via Aspose.Cells Cloud REST API. Includes cURL examples, JWT authentication, and SDK code for C#, Java, Python, Node.js, Go, Ruby, PHP, and Perl."
tags: ["excel", "document-properties", "rest-api", "cloud"]
canonical: /total/getting-started/rest-api-overview/set-document-property/
robots: index, follow
weight: 120
api_version: "v3.0 (Stable)"
aliases: [/set-a-particular-document-property/]
---

## Overview

The **Update (Set) Document Property** operation lets you create a new document property or modify an existing one in an Excel workbook stored in Aspose Cloud Storage.

**Endpoint**  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`

The request accepts a JSON payload that describes the property to be set.

## Prerequisites

- A valid **JWT access token** (see the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).
- The target workbook (`{name}`) must already exist in Aspose Cloud Storage (or a folder you specify).
- The storage name (`storageName`) is optional; if omitted, the default storage is used.

## Authentication

Aspose.Cells Cloud uses **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt-token>
```

For details on obtaining a JWT token, see the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## HTTP Request

| Element          | Value                                             |
| ---------------- | ------------------------------------------------- |
| **Method**       | `PUT`                                             |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type** | `application/json`                                |
| **Accept**       | `application/json`                                |

### Path Parameters

| Name           | Type   | Required | Description                                         |
| -------------- | ------ | -------- | --------------------------------------------------- |
| `name`         | string | ✅       | The name of the Excel file (including extension).   |
| `propertyName` | string | ✅       | The name of the document property to set or create. |

### Query Parameters

| Name          | Type   | Required | Description                                                           |
| ------------- | ------ | -------- | --------------------------------------------------------------------- |
| `folder`      | string | ❌       | Folder path in storage where the workbook resides.                    |
| `storageName` | string | ❌       | Name of the storage service. If omitted, the default storage is used. |

### Request Body – Document Property Object

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "false",
  "Link": {
    "Href": "https://docs.aspose.cloud/cells/authoring-guide",
    "Rel": "self",
    "Title": "Author link",
    "Type": "text/html"
  }
}
```

| Field       | Type   | Required | Description                                                         |
| ----------- | ------ | -------- | ------------------------------------------------------------------- |
| **Name**    | string | ✅       | Property name (e.g., `author`).                                     |
| **Value**   | string | ✅       | Property value.                                                     |
| **BuiltIn** | string | ❌       | Indicates whether the property is built‑in (`"true"` or `"false"`). |
| **Link**    | object | ❌       | Hyperlink information (`Href`, `Rel`, `Title`, `Type`).             |

> **Note**: Field naming conventions vary by SDK language (e.g., `BuiltIn` in JSON vs `builtIn` in Node.js). Always consult the SDK’s type definitions for correct casing and naming.

## Example Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://docs.aspose.cloud/cells/authoring-guide",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### Example Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## HTTP Status Codes

| Code | Meaning               | Description                                                  |
| ---- | --------------------- | ------------------------------------------------------------ |
| 200  | OK                    | Property updated or created successfully.                    |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                |
| 413  | Payload Too Large     | Request body exceeds size limit.                             |
| 500  | Internal Server Error | Unexpected server error.                                     |

## SDK Examples
