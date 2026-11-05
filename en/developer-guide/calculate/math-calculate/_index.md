---
title: "Aspose.Cells Cloud – Math Calculate API (Add, Subtract, Multiply, Divide, %)"
second_title: "Developer Guide"
ArticleTitle: "Math Calculate API"
linktitle: "Math Calculate"
description: "Use Aspose.Cells Cloud Math Calculate API to perform bulk Excel operations—including addition, subtraction, multiplication, division, and percentage calculations—via REST API. Includes request format, SDK examples, and error codes."
keywords: "Math Calculate API, Aspose.Cells Cloud, Excel calculations, Add, Subtract, Multiply, Divide, Percentage, Bulk Excel processing, REST API"
type: docs
url: /math-calculate/
weight: 100
---
The **MathCalculate** API (`PUT https://api.aspose.cloud/v4.0/cells/calculate/math`) enables bulk mathematical operations on spreadsheet data via Aspose.Cells Cloud, allowing users to perform calculations across entire columns, rows, or tables without writing formulas or using VBA by uploading a spreadsheet file and specifying an operation (e.g., `SUM`, `AVERAGE`) and numeric value as query parameters.

## Overview

Perform bulk calculations across entire columns, rows, or tables without writing formulas or using VBA.

- **Basic math**: add, subtract, multiply, or divide every cell in a range by a numeric value
- **Percentages**: increase/decrease values by a percentage or compute a percentage of a number (e.g., +15%, −8%, 20% of)
- **Bulk processing**: instantly apply operations to thousands of cells—no drag-fill, no array formulas

| Calculate Operation | Description                  |
| ------------------- | ---------------------------- |
| `Add`               | Addition (`+`)               |
| `Subtract`          | Subtraction (`-`)            |
| `Multiply`          | Multiplication (`*`)         |
| `Divide`            | Division (`/`)               |
| `Percentage`        | Percentage calculation (`%`) |

## The Math Calculate Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### Security and Authentication

Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| operation | String | Query | - |
| value | String | Query | - |
| worksheet | String | Query | - |
| range | String | Query | - |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> **Note**: The `value` parameter is required for all operations except `Percentage`, where it may represent the base value (e.g., `20% of 100`). For percentage changes (e.g., +15%), use `value` as the percentage amount.

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

The API returns the updated spreadsheet as a downloadable binary stream.

| Response Name  | Data Type | Reference |
| -------------- | --------- | --------- |
| `ResponseFile` | File      | Stream    |

#### HTTP Status Codes

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

## How to Use the Math Calculate API with SDKs?

### Math Calculate API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/MathCalculate" rel="noopener noreferrer">Math Calculate API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The [Math Calculate API specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) defines the public REST interface. For streamlined integration, use one of the Aspose.Cells Cloud SDKs.

View the [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"}.

The following examples demonstrate how to call the API using various SDKs:

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="1" tabID="1" tabName1="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}
