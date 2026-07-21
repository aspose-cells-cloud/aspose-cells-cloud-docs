---
title: "Calculate Cell Formula – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, calculate cell formula, Excel API, REST API, SDK"
description: "Calculate an Excel cell formula via Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, and SDK snippets."
ArticleTitle: "Calculate Cell Formula – Aspose.Cells Cloud API Documentation"
---

## REST API

This REST API calculates the **cell formula** in an Excel workbook.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type   | Parameter location (path/query/body) | Description                                                          |
| -------------- | ------ | ------------------------------------ | -------------------------------------------------------------------- |
| name           | string | path                                 | Name of the Excel file (e.g., `Book1.xlsx`).                         |
| sheetName      | string | path                                 | Name of the worksheet that contains the cell.                        |
| cellName       | string | path                                 | Address of the cell to be calculated (e.g., `A1`).                   |
| options        | object | body                                 | JSON object with calculation options (see **Options object** table). |
| folder         | string | query                                | Folder in storage where the file is located.                         |
| storageName    | string | query                                | Name of the Aspose Cloud storage.                                    |

#### Options object

| Field         | Type    | Description                                                                    | Default |
| ------------- | ------- | ------------------------------------------------------------------------------ | ------- |
| CalcStackSize | string  | Maximum calculation stack size.                                                | `"1"`   |
| IgnoreError   | boolean | If `true`, calculation errors are ignored and the cell value is set to `#N/A`. | `false` |
| Recursive     | boolean | Enables recursive calculation of dependent cells.                              | `false` |
| Precision     | string  | Number of decimal places for numeric results.                                  | `"15"`  |
| UseThreading  | boolean | Enables multi‑threaded calculation.                                            | `false` |


### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the PostCellCalculate API with SDKs

### PostCellCalculate API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL. **First obtain a JWT token** by authenticating against the `/connect/token` endpoint and replace `<jwt token>` with the token value.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}