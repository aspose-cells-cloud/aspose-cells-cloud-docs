---
title: "An API of Aspose.Cells Cloud for Add, Minus, Multiply, Divide, and Percentage on a range of Spreadsheet/Excel"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Excel"
linktitle: "Math Calculate"
type: docs
url: /math-calculate/
keywords: "Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cells"
description: "Comprehensive guide for using the Math Calculate API to perform calculations in Excel spreadsheets."
weight: 100
kwords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cells
---

The API allows developers to perform addition, subtraction, multiplication, division, and percentage calculations on specified ranges of spreadsheets/Excel with a RESTful interface.

| **Calculate Operation** | Description |
| **Add** |  |
| **Minus** |  |
| **Multiply** |  |
| **Divide** |  |
| **Percentage** |  |

## **Math Calculate API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file for processing. |
| operation | String | Query | The mathematical operation to perform (Add, Minus, Multiply, Divide, and Percentage). |
| value | String | Query | A value to use in the calculation, if applicable. |
| worksheet | String | Query | The name of the worksheet to operate on. |
| range | String | Query | The range of cells to include in the calculation. |
| region | String | Query | Defines the specific region of the spreadsheet. |
| password | String | Query | The password for opening the spreadsheet file, if protected. |

### **Response**

```json
{
File
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Math Calculate API?

The mathematical computation API is suitable for batch calculations on spreadsheets.

## Why should you use the Math Calculate API?

- Perform batch mathematical calculations.
- Development can be quickly completed through the existing SDK.

## How to Use the Math Calculate API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) defines a publicly accessible programming interface, allowing developers to interact with the API directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement math calculations for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
