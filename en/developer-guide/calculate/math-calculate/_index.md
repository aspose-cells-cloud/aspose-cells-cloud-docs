---
title: "Aspose.Cells Cloud – Math Calculate API (Add, Subtract, Multiply, Divide, %)"
second_title: "Document"
ArticleTitle: "Add, Subtract, Multiply, Divide, and Percentage in Spreadsheets/Excel"
linktitle: "Math Calculate"
type: docs
url: /math-calculate/
keywords: "Math Calculate API, Aspose.Cells Cloud, Excel calculations, Add, Subtract, Multiply, Divide, Percentage, Bulk Excel processing, REST API"
description: "Learn how to use Aspose.Cells Cloud Math Calculate API to bulk‑apply add, subtract, multiply, divide or percentage operations on Excel ranges. Includes request format, sample code and error handling."
weight: 100
---

## **Introduction**: Spreadsheet Quick Calculate – Add, Multiply, Subtract, Divide & Percent Formulas in One Running API

_Perform bulk calculations across entire columns, rows, or tables without writing a formula._

- **Basic math**: add, subtract, multiply or divide every cell in a range by any number
- **Percentages**: increase/decrease by %, or find % of a number (e.g. +15%, -8%, 20% of…)
- **Bulk**: apply to thousands of cells instantly—no drag‑fill, no array formula, no VBA

| **Calculate Operation** | Description |
| :---------------------- | :---------- |
| **Add**                 | +           |
| **Subtract**            | -           |
| **Multiply**            | \*          |
| **Divide**              | /           |
| **Percentage**          | %           |

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## **Math Calculate API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                              |
| :------------- | :----- | :-------------------------- | :--------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Upload the spreadsheet file for processing.                                              |
| operation      | String | Query                       | The mathematical operation to perform (Add, Subtract, Multiply, Divide, and Percentage). |
| value          | String | Query                       | A value to use in the calculation, if applicable.                                        |
| worksheet      | String | Query                       | The name of the worksheet to operate on.                                                 |
| range          | String | Query                       | The range of cells to include in the calculation.                                        |
| region         | String | Query                       | The spreadsheet region setting.                                                          |
| password       | String | Query                       | The password for opening the spreadsheet file, if protected.                             |


### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Where should we use the Math Calculate API?

- Finance: add 13% VAT to an entire column of purchase prices.
- Inventory: multiply kg column by 2.2046 to bulk‑convert to pounds.
- Payroll: add a flat bonus of 1,000 to the bonus column for all staff.
- FX conversion: divide sales column by live exchange rate to get USD amounts.
- Grading: subtract 5 points from every student score for attendance penalty.
- E‑commerce: apply a 15% promotional discount by reducing product prices in one click.

## Why should you use the Math Calculate API?

- **Fast Excel calculations** – finish month‑end reports in seconds.
- **Bulk percentage increase Excel** – update prices, forecasts, commissions in one click.
- **Add same number to entire column** – inventory, currency conversion, unit conversion.
- **Excel without formulas** – non‑technical users love the simplicity.
- Development can be quickly completed through the existing SDK.

**Notes**  
The maximum file size supported is 200 MB. The `range` parameter must be a valid Excel address (e.g., A1:B10). Very large worksheets may require additional processing time.

## How to Use the Math Calculate API with SDKs

### Math Calculate API Specification

The [Math Calculate Specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) defines a publicly accessible programming interface, allowing developers to interact with the API directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to perform math calculations by cell with just a short code.  
Please check out the [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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