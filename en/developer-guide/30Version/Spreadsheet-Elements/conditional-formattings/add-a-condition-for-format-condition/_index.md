---
title: Add Condition to Conditional Formatting
description: "Add Excel conditional formatting conditions via Aspose.Cells Cloud REST API v3.0 with parameters and examples"
keywords: "Aspose.Cells Cloud, Conditional Formatting, Add Condition, REST API, Excel, Worksheet"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
linktitle: "Add Condition"
ArticleTitle: "Add Condition to Conditional Formatting in Excel using Aspose.Cells Cloud API"
---

The **PutWorksheetFormatConditionCondition** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`) enables developers to add a new condition to an existing conditional formatting rule in a worksheet by specifying the condition type (e.g., CellValue, Expression), operator (e.g., GreaterThan, Between), and one or two formulas via query parameters; this Aspose.Cells Cloud REST API v3.0 operation supports precise, programmatic control over conditional formatting logic without requiring local Excel installations.

---

## The Put Worksheet Format Condition Condition Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                                                                                                                                                                                                           |
| -------------- | ------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | The file name.                                                                                                                                                                                                                                        |
| sheetName      | String  | Path                       | The worksheet name.                                                                                                                                                                                                                                   |
| index          | Integer | Path                       | Gets the Conditional Formatting element at the specified index.                                                                                                                                                                                       |
| type           | String  | Query                      | Format condition type(CellValue/Expression/ColorScale/DataBar/IconSet/Top10/UniqueValues/DuplicateValues/ContainsText/NotContainsText/BeginsWith/EndsWith/ContainsBlanks/NotContainsBlanks/ContainsErrors/NotContainsErrors/TimePeriod/AboveAverage). |
| operatorType   | String  | Query                      | Represents the operator type of conditional format and data validation(Between/Equal/GreaterThan/GreaterOrEqual/LessThan/None/NotBetween/NotEqual).                                                                                                   |
| formula1       | String  | Query                      | The value or expression associated with conditional formatting.                                                                                                                                                                                       |
| formula2       | String  | Query                      | The value or expression associated with conditional formatting.                                                                                                                                                                                       |
| folder         | String  | Query                      | The folder where the file is situated.                                                                                                                                                                                                                |
| storageName    | String  | Query                      | The storage name where the file is situated.                                                                                                                                                                                                          |

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

**HTTP Method:** `PUT`  
**URL:**

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parameter      | Location | Type    | Required | Description                                                                                                                                                                                                                                                                                                         |
| -------------- | -------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`         | Path     | string  | **Yes**  | Name of the workbook file (including extension).                                                                                                                                                                                                                                                                    |
| `sheetName`    | Path     | string  | **Yes**  | Name of the worksheet that contains the conditional formatting.                                                                                                                                                                                                                                                     |
| `index`        | Path     | integer | **Yes**  | Zero‑based index of the conditional‑formatting collection to modify.                                                                                                                                                                                                                                                |
| `type`         | Query    | string  | **Yes**  | Condition type. Allowed values: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Query    | string  | **Yes**  | Operator for the condition. Allowed values: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`.                                                                                                                                                                      |
| `formula1`     | Query    | string  | **Yes**  | First formula/value associated with the condition.                                                                                                                                                                                                                                                                  |
| `formula2`     | Query    | string  | No       | Second formula/value (required only for operators that need two values, e.g., `Between`).                                                                                                                                                                                                                           |
| `folder`       | Query    | string  | No       | Folder in storage where the workbook is located.                                                                                                                                                                                                                                                                    |
| `storageName`  | Query    | string  | No       | Name of the storage service.                                                                                                                                                                                                                                                                                        |

> **Note:** All path parameters (`name`, `sheetName`, `index`) and the query parameters `type`, `operatorType`, `formula1` are mandatory. `formula2`, `folder`, and `storageName` are optional.

## How to Use the Put Worksheet Format Condition Condition API with SDKs?

### Put Worksheet Format Condition Condition API Specification

The <a href="https://reference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition" rel="noopener noreferrer">Put Worksheet Format Condition Condition API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Below are ready‑to‑run snippets for the most popular SDKs. Replace placeholder values (`YOUR_FILE`, `YOUR_SHEET`, etc.) with your own data.

### cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

**Successful Response**

```json
{
  "Code": "200",
  "Status": "OK"
}
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFormatConditionCondition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFormatConditionCondition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFormatConditionCondition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFormatConditionCondition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFormatConditionCondition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFormatConditionCondition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFormatConditionCondition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFormatConditionCondition.go" >}}
{{</tab>}}
{{< /tabs >}}
