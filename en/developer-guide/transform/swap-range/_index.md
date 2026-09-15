---
title: "Swap Ranges in Excel – Aspose.Cells Cloud API v4.0"
description: "Use Aspose.Cells Cloud API v4.0 to swap columns, rows, or ranges in Excel files while preserving formatting, formulas, and cell references."
keywords: "excel swap range, cloud spreadsheet api, aspose.cells cloud, exchange cells"
url: /swap-range/
linktitle: "Swap Ranges"
type: docs
date: 2024-05-15
weight: 100
tags: ["cells", "spreadsheet", "api", "transform"]
categories: ["api-reference", "cloud"]
summary: "Effortlessly exchange data between two columns, rows, or ranges in Excel files using Aspose.Cells Cloud API v4.0—ideal for financial modeling, ETL, and error correction."
---

{{% alert color="primary" %}}
**Prerequisites**  
- Valid Aspose Cloud account and API credentials (client ID and client secret).  
- Uploaded workbook to cloud storage (or include via `Spreadsheet` FormData).  
- See [Authentication](/authentication/) and [File Upload](/upload/) for setup guidance.
{{% /alert %}}

## Overview

The **Swap Ranges API** enables precise, one-step exchange of data between two ranges—columns, rows, or cell blocks—in Excel workbooks (.xlsx, .xls). It preserves formatting, formulas, conditional formatting, and cell references, making it ideal for dynamic data reorganization without manual intervention.

> **Key Benefits**  
> - ✅ **Formatting & formula integrity**: No broken references after swap.  
> - ✅ **Flexible scope**: Swap columns, rows, or arbitrary ranges (e.g., `A1:D10` ↔ `F1:I10`).  
> - ✅ **Batch-ready**: Integrate into automated ETL or data-cleaning pipelines.  
> - ✅ **Pay-per-use**: No fixed infrastructure costs.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

## Authentication

All requests require a [JWT access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

## Request Parameters

| Parameter Name     | Type   | Location   | Required | Description |
|--------------------|--------|------------|----------|-------------|
| `Spreadsheet`      | File   | FormData   | ✅ Yes   | The source Excel workbook (`.xlsx`, `.xls`). |
| `worksheet1`       | String | Query      | ✅ Yes   | Name of the worksheet containing the first range. |
| `range1`           | String | Query      | ✅ Yes   | First range to swap (e.g., `A1:D10`). |
| `worksheet2`       | String | Query      | ✅ Yes   | Name of the worksheet containing the second range (may equal `worksheet1`). |
| `range2`           | String | Query      | ✅ Yes   | Second range to swap (e.g., `F1:I10`). **Must match `range1` in dimensions**. |
| `outPath`          | String | Query      | ❌ No    | Cloud storage path to save the modified workbook (e.g., `/output/result.xlsx`). |
| `outStorageName`   | String | Query      | ❌ No    | Name of the configured cloud storage (e.g., `MyCompanyStorage`). **Required only if `outPath` is specified**. |
| `region`           | String | Query      | ❌ No    | Locale (e.g., `en-US`, `fr-FR`) for formatting and date/number parsing. |
| `password`         | String | Query      | ❌ No    | Password for encrypted workbooks. Omit if unencrypted. |

### Notes on Parameters
- `range1` and `range2` **must have identical dimensions** (e.g., both 5 rows × 4 columns). Mismatched ranges return `400 Bad Request`.
- `outStorageName` is only required when `outPath` is provided. If omitted, the response returns the modified file as a stream.
- If `region` is omitted, the server uses `en-US` by default.

### Example Request (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet1&range2=F1:I10&region=en-US" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

> 💡 **Tip**: To save directly to cloud storage, add `outPath=/results/swapped.xlsx&outStorageName=MyCompanyStorage`.

## Response

The API returns the modified Excel file as a binary stream.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

- If `outPath` is specified, the file is saved to cloud storage *and* returned in the response.
- If omitted, only the file stream is returned.

## Error Handling

| HTTP Code | Description |
|-----------|-------------|
| `400 Bad Request` | Invalid range dimensions, malformed parameters, or missing required fields. |
| `401 Unauthorized` | Missing, invalid, or expired JWT token. |
| `404 Not Found` | Source workbook not found in cloud storage or path. |
| `500 Server Error` | Internal processing failure (e.g., workbook corruption). |

## Use Cases

| Use Case | Description |
|----------|-------------|
| **Financial Model Restructuring** | Swap quarterly forecast blocks while preserving formulas and formatting. |
| **ETL Data Staging** | Exchange raw data ranges with cleaned/transformed ranges in a staging sheet. |
| **Error Correction** | Fix misaligned data imports by swapping misplaced ranges in bulk. |

## SDK Integration

Aspose.Cells Cloud provides SDKs for major languages. The following examples swap `A1:D10` and `F1:I10` on `Sheet1`:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1">}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs">}}
{{</tab>}}
{{<tab tabNum="2">}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java">}}
{{</tab>}}
{{<tab tabNum="3">}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php">}}
{{</tab>}}
{{<tab tabNum="4">}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb">}}
{{</tab>}}
{{<tab tabNum="5">}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts">}}
{{</tab>}}
{{<tab tabNum="6">}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py">}}
{{</tab>}}
{{<tab tabNum="7">}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl">}}
{{</tab>}}
{{<tab tabNum="8">}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go">}}
{{</tab>}}
{{< /tabs >}}

> 💡 **Pro Tip**: Use SDKs to avoid manual cURL handling and benefit from built-in error handling, retries, and type safety.

## API Specification

- [Swagger/OpenAPI Spec (Interactive)](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange)  
- [GitHub SDK Repositories](https://github.com/aspose-cells-cloud){rel="noopener noreferrer"}

## See Also

- [Copy Ranges](/copy-range/)  
- [Merge Ranges](/merge-range/)  
- [Move Ranges](/move-range/)  
- [Batch Transform Operations](/batch-transform/)

---

{{% alert color="info" %}}
**Version Note**: This API is part of Aspose.Cells Cloud v4.0. For deprecation policies, see [API Versioning](/api-versioning/).  
**Last Updated**: May 15, 2024  
{{% /alert %}}