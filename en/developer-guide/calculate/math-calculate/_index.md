---
title: "Aspose.Cells Cloud – Math Calculate API (Add, Subtract, Multiply, Divide, %)"
second_title: "Document"
ArticleTitle: "Math Calculate API"
linktitle: "Math Calculate"
date: 2024-03-15
lastmod: 2024-03-15
description: "Use Aspose.Cells Cloud Math Calculate API to perform bulk Excel operations—including addition, subtraction, multiplication, division, and percentage calculations—via REST API. Includes request format, SDK examples, and error codes."
keywords: "Math Calculate API, Aspose.Cells Cloud, Excel calculations, Add, Subtract, Multiply, Divide, Percentage, Bulk Excel processing, REST API"
type: docs
url: /math-calculate/
weight: 100
---

## Introduction

Perform bulk calculations across entire columns, rows, or tables without writing formulas or using VBA.

- **Basic math**: add, subtract, multiply, or divide every cell in a range by a numeric value  
- **Percentages**: increase/decrease values by a percentage or compute a percentage of a number (e.g., +15%, −8%, 20% of)  
- **Bulk processing**: instantly apply operations to thousands of cells—no drag-fill, no array formulas  

| Calculate Operation | Description |
|---------------------|-------------|
| `Add`               | Addition (`+`) |
| `Subtract`          | Subtraction (`-`) |
| `Multiply`          | Multiplication (`*`) |
| `Divide`            | Division (`/`) |
| `Percentage`        | Percentage calculation (`%`) |

## Math Calculate API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### Security and Authentication

Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){: rel="noopener noreferrer"}.

### Request Parameters

| Parameter Name | Type   | Location           | Description |
|----------------|--------|--------------------|-------------|
| `Spreadsheet`  | File   | FormData           | Upload the spreadsheet file for processing. |
| `operation`    | String | Query              | Mathematical operation: `Add`, `Subtract`, `Multiply`, `Divide`, or `Percentage`. |
| `value`        | String | Query              | Numeric value used in the calculation (e.g., `13` for +13%, or `2.2046` for unit conversion). |
| `worksheet`    | String | Query              | Name of the worksheet to operate on. |
| `range`        | String | Query              | Cell range (e.g., `A1:B10`). Must be a valid Excel address. |
| `region`       | String | Query              | Locale setting (e.g., `en-US`, `fr-FR`). Affects number and date formatting. |
| `password`     | String | Query              | Password for protected workbooks. |

> **Note**: The `value` parameter is required for all operations except `Percentage`, where it may represent the base value (e.g., `20% of 100`). For percentage changes (e.g., +15%), use `value` as the percentage amount.

### Response

The API returns the updated spreadsheet as a downloadable binary stream.

| Response Name | Data Type | Reference |
|---------------|-----------|-----------|
| `ResponseFile` | File      | Stream    |

#### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| `200` | OK                    | Calculation applied successfully; response contains updated spreadsheet. |
| `400` | Bad Request           | Invalid or missing parameters (e.g., unsupported file type, invalid range). |
| `401` | Unauthorized          | Missing or invalid JWT token. |
| `413` | Payload Too Large     | Uploaded file exceeds 200 MB limit. |
| `500` | Internal Server Error | Unexpected server-side failure. |

## Use Cases

- **Finance**: Add 13% VAT to purchase prices across an entire column.  
- **Inventory**: Multiply weight (kg) column by `2.2046` to convert to pounds.  
- **Payroll**: Add a flat bonus (`1000`) to all employees’ bonus columns.  
- **FX Conversion**: Divide sales column by a live exchange rate to compute USD values.  
- **Grading**: Subtract 5 points from all student scores for attendance penalties.  
- **E‑commerce**: Apply a 15% promotional discount by reducing product prices.

## Why Use the Math Calculate API?

- ⚡ **Fast calculations** – generate month-end reports in seconds.  
- 📈 **Bulk percentage changes** – update prices, forecasts, or commissions in one request.  
- 📊 **Consistent operations** – apply identical logic across large datasets.  
- 🧑‍💼 **Non-technical friendly** – no Excel formula or VBA knowledge required.  
- 🛠️ **Rapid development** – integrate quickly using our SDKs.

> **Limitations**: Maximum file size is 200 MB. Very large worksheets may require additional processing time. The `range` must be a valid Excel cell address (e.g., `A1:B10`).

## How to Use the Math Calculate API with SDKs

The [Math Calculate API specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) defines the public REST interface. For streamlined integration, use one of the Aspose.Cells Cloud SDKs.

View the [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"}.

The following examples demonstrate how to call the API using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}

> **Tip**: Ensure your SDK is initialized with valid `ClientID` and `ClientSecret`. Refer to the [Getting Started guide](https://docs.aspose.cloud/total/getting-started/) for setup instructions.