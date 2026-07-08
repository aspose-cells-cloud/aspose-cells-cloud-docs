---
title: "Calculate a formula on an Excel worksheet"
second_title: "Document"
linktitle: "Calculate"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, formula calculation, REST API, SDKs, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Calculate formulas in an Excel worksheet using Aspose.Cells Cloud REST API. Supports multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) with ready‑to‑use examples."
weight: 20
ArticleTitle: "Calculate a formula on an Excel worksheet – Aspose.Cells Cloud Documentation"
---

This REST API returns the **calculated value of a formula** in a worksheet. It can be used to **evaluate an Excel formula** directly from your application.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Request parameters**

| Parameter Name | Type   | Location | Description                                        |
| -------------- | ------ | -------- | -------------------------------------------------- |
| name           | string | path     | Name of the Excel file.                            |
| sheetName      | string | path     | Name of the worksheet that contains the formula.   |
| formula        | string | query    | The formula to be evaluated (e.g., `SUM(A5:A10)`). |
| folder         | string | query    | Folder where the document is stored.               |
| storageName    | string | query    | Name of the storage service (if applicable).       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### Authentication

All requests must include a valid **Bearer JWT token** in the `Authorization` header:

```
Authorization: Bearer <your_jwt_token>
```

You can obtain a token by following the OAuth 2.0 flow described in the Aspose.Cells Cloud authentication guide.

### Possible response status codes

| Code | Description                                 |
|------|---------------------------------------------|
| 200  | Request succeeded; the formula value is returned. |
| 400  | Bad request – missing or invalid parameters. |
| 401  | Unauthorized – invalid or missing JWT token. |
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

## Cloud SDK Family

Using an SDK is the fastest way to integrate the API. An SDK handles low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**See also:**  
- [Get Worksheet](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Update Worksheet](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Calculate All Formulas](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  