---
title: "Group Columns – Aspise.Cells Cloud API Documentation"
description: "Group worksheet columns in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request syntax, parameters, cURL and SDK examples, and response details."
keywords: "Aspose.Cells, group columns, Excel API, REST, cloud SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Group Columns on an Excel Worksheet

**API version:** v3.0  
**Operation:** `PostGroupWorksheetColumns` – Group worksheet columns in the worksheet.

---

## Overview

This REST API lets you group a range of columns in a worksheet. Grouped columns can be shown or hidden, enabling you to create collapsible sections similar to those in Microsoft Excel.

---

## Prerequisites

- A valid **JWT access token** obtained from the Aspose Cloud authentication service.  
- The workbook must be stored in a location accessible to Aspose.Cells Cloud (default storage or a custom storage name).  
- Required SDK version (if using an SDK): the latest release that supports API version **v3.0**.  

---

## Authentication

All requests require **Bearer token** authentication.

```http
Authorization: Bearer <access_token>
```

For details on obtaining a token, see the [JWT authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP Request

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parameter | Location | Required | Description |
|-----------|----------|----------|-------------|
| `name` | Path | Yes | The workbook file name (e.g., `test.xlsx`). |
| `sheetName` | Path | Yes | The worksheet that contains the columns to group. |
| `firstIndex` | Query | Yes | Zero‑based index of the first column to include in the group. |
| `lastIndex` | Query | Yes | Zero‑based index of the last column to include in the group. |
| `hide` | Query | No | If `true`, the grouped columns are hidden; otherwise they remain visible. |
| `folder` | Query | No | Path to the folder that contains the workbook. |
| `storageName` | Query | No | Name of the storage service where the file is located. |

---

## Request Example (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Note:** The request uses **HTTPS** to ensure encrypted communication.

---

## Response

### Success (200)

| Field  | Type    | Description |
|--------|---------|-------------|
| `Code` | integer | HTTP status code (`200`). |
| `Status` | string | Textual status of the operation (`OK`). |

**Example**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error (e.g., 400 Bad Request)

| Field        | Type    | Description |
|--------------|---------|-------------|
| `Code`       | integer | HTTP status code (`400`, `401`, `404`, `500`, …). |
| `Status`     | string  | Textual status (`Error`). |
| `ErrorMessage` | string | Human‑readable description of the problem. |
| `ErrorCode`  | string  | Programmatic identifier for the error. |

**Example – Bad Request**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Invalid column index.",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK Examples

The following snippets demonstrate how to call the **Group Worksheet Columns** operation using the supported SDKs.

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

---

## Remarks

- **Grouping behavior:** The API creates a column group that can be expanded or collapsed in Excel. Setting `hide=true` collapses the group immediately.  
- **Zero‑based indexing:** Both `firstIndex` and `lastIndex` start at **0**; the first column in a worksheet is index 0.  
- **Storage considerations:** If the workbook resides in a non‑default storage, provide both `folder` and `storageName` query parameters.  

---

## See Also

- [Authentication – JWT token based](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [OpenAPI Specification for Group Worksheet Columns](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDKs (GitHub)](https://github.com/aspose-cells-cloud)  
- [Group Rows on an Excel Worksheet](/rows/group/)  

---

> *Illustration:* ![Screenshot showing grouped columns in an Excel worksheet](./images/group-columns.png){: .img-fluid alt="Screenshot showing grouped columns in an Excel worksheet" }

*The above placeholder image should be replaced with an actual screenshot that demonstrates the visual result of grouping columns.*