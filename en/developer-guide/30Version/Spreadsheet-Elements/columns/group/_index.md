---
title: "Group Columns on an Excel Worksheet"
secondtitle: "Aspose.Cells Cloud API Documentation"
linktitle: "Group Columns"
url: /cells/group-columns/
description: "Group Excel worksheet columns programmatically using Aspose.Cells Cloud REST API v3.0. Includes cURL and SDK examples, authentication guidance, and collapsible section support to reduce manual effort and enhance Excel-like interactivity."
keywords: ["Excel grouping", "column grouping API", "Aspose.Cells Cloud", "REST API", "collapsible columns", "Excel automation", "worksheet grouping"]
weight: 10
type: docs
date: 2023-11-15
aliases:
  - /cells/group-columns/
  - /excel/group-columns/
---

# Group Columns on an Excel Worksheet

**API Version:** v3.0  
**Operation:** `PostGroupWorksheetColumns` – Group worksheet columns in a worksheet.

## Introduction

Grouping columns in Excel enables you to create collapsible sections, improving data readability and user interaction. With Aspose.Cells Cloud, you can programmatically group ranges of columns—ideal for automating dashboard generation, report formatting, or interactive workbook creation. This API supports immediate visibility control (e.g., collapse/expand on creation), ensuring your Excel workflows mirror native Excel behavior.

## Prerequisites

- A valid **JWT access token** from Aspose Cloud authentication.  
- The workbook must reside in Aspose.Cells Cloud’s default storage or a named custom storage.  
- Use SDKs compatible with API version **v3.0** (latest releases recommended).

## Authentication

All requests require a **Bearer token**:

```http
Authorization: Bearer <access_token>
```

For detailed token acquisition steps, see the [JWT Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## HTTP Request

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parameter     | Location | Required | Description                                                               |
|---------------|----------|----------|---------------------------------------------------------------------------|
| `name`        | Path     | Yes      | Workbook filename (e.g., `report.xlsx`).                                 |
| `sheetName`   | Path     | Yes      | Worksheet name containing the columns to group.                          |
| `firstIndex`  | Query    | Yes      | Zero-based index of the first column in the group.                       |
| `lastIndex`   | Query    | Yes      | Zero-based index of the last column in the group.                        |
| `hide`        | Query    | No       | If `true`, the grouped columns are hidden (collapsed) upon grouping.     |
| `folder`      | Query    | No       | Folder path containing the workbook (if not in default storage).         |
| `storageName` | Query    | No       | Custom storage name (if applicable).                                     |

### Notes
- Column indices are **zero-based** (e.g., column A = index `0`, column B = index `1`).
- Setting `hide=true` immediately collapses the group, matching Excel’s UI behavior.

## Request Example (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=3&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Security Note:** All requests use **HTTPS** for encrypted communication.

## Response

### Success (200 OK)

| Field    | Type    | Description                             |
|----------|---------|-----------------------------------------|
| `Code`   | integer | HTTP status code (`200`).               |
| `Status` | string  | Operation status (`OK`).                |

**Example Response:**
```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error Responses

| Field          | Type    | Description                                       |
|----------------|---------|---------------------------------------------------|
| `Code`         | integer | HTTP error code (`400`, `401`, `404`, `500`, etc.) |
| `Status`       | string  | Error status (`Error`).                           |
| `ErrorMessage` | string  | Human-readable error description.                 |
| `ErrorCode`    | string  | Programmatic error identifier (e.g., `InvalidParameter`). |

**Example – Bad Request (400):**
```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Invalid column index: lastIndex must be greater than or equal to firstIndex.",
  "ErrorCode": "InvalidParameter"
}
```

## SDK Examples

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Usage Tips

- **Collapsible Sections**: Use `hide=true` to collapse groups immediately; users can later expand them in Excel.
- **Index Validation**: Ensure `firstIndex ≤ lastIndex` and both indices are within valid column bounds (e.g., ≤ 16,383 for modern Excel).
- **Storage Paths**: For non-default storage, provide both `folder` and `storageName` query parameters.

## See Also

- [JWT Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI Reference: PostGroupWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)
- [Aspose.Cells Cloud SDKs (GitHub)](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"}
- [Group Rows on an Excel Worksheet](/cells/group-rows/)

![Collapsed grouped columns in Excel showing the +/– expand/collapse indicator.](/images/group-columns.png)

> *Figure: Collapsed column group in Excel, with the +/- toggle visible.*

---