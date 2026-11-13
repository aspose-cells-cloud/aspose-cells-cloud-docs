---
title: "Calculate a formula on an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Calculate"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, formula calculation, REST API, SDKs, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Calculate formulas in an Excel worksheet using Aspose.Cells Cloud REST API. Supports multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) with ready‑to‑use examples."
weight: 100
ArticleTitle: "Calculate a formula on an Excel worksheet – Aspose.Cells Cloud Documentation"
---
The **GetWorksheetCalculateFormula** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult`) enables developers to calculate and retrieve the evaluated result of a specified Excel formula within a worksheet using Aspose.Cells Cloud, supporting direct formula evaluation without requiring local Excel installation.

## The Get Worksheet Calculate Formula Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### Security and Authentication

All requests must include a valid **Bearer JWT token** in the `Authorization` header:

```
Authorization: Bearer <your_jwt_token>
```

You can obtain a token by following the OAuth 2.0 flow described in the Aspose.Cells Cloud authentication guide.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| formula | String | Query | The formula. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### Response

```json
[
  {
    "Name": "SingleValueResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "SingleValueResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Possible response status codes

| Code | Description                                                 |
| ---- | ----------------------------------------------------------- |
| 200  | Request succeeded; the formula value is returned.           |
| 400  | Bad request – missing or invalid parameters.                |
| 401  | Unauthorized – invalid or missing JWT token.                |
| 404  | Not found – the specified file or worksheet does not exist. |
| 500  | Internal server error – unexpected condition on the server. |

You can use the **cURL** command‑line tool to call Aspose.Cells Cloud web services easily. The example below shows how to request a formula result with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## How to Use the Get Worksheet Calculate Formula API with SDKs?

### Get Worksheet Calculate Formula API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula" rel="noopener noreferrer">Get Worksheet Calculate Formula API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

---

**See also:**

- [Get Worksheet](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)
- [Update Worksheet](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)
- [Calculate All Formulas](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCalculateFormula.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCalculateFormula.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCalculateFormula.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCalculateFormula.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCalculateFormula.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCalculateFormula.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCalculateFormula.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCalculateFormula.go" >}}
{{</tab>}}
{{< /tabs >}}
