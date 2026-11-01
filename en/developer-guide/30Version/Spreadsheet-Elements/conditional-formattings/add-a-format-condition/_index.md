---
title: "Add Format Condition"
type: docs
url: /conditional-formattings/add-format-condition/
aliases: [/add-a-format-condition/]
keywords: "Aspose.Cells Cloud, Conditional Formatting API, Add Format Condition, Excel REST API, Cells API"
description: "Add Excel conditional formatting via Aspose.Cells Cloud REST API using PUT request with cell area, type, and formulas."
ArticleTitle: "Add Format Condition – Aspose.Cells Cloud API Documentation"
weight: 50
linktitle: "Add Format Condition"
---
The **PutWorksheetFormatCondition** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`) adds a format condition to a specified worksheet in Aspose.Cells Cloud, supporting types such as CellValue, Expression, ColorScale, DataBar, IconSet, Top10, UniqueValues, DuplicateValues, and ContainsText; it requires parameters including the cell area, condition type, operator type, and one or two formulas to define the formatting rule.

## Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Put Worksheet Format Condition Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| index | Integer | Path | Gets the Conditional Formatting element at the specified index. |
| cellArea | String | Query | Adds a conditional formatted cell range. |
| type | String | Query | Format condition type(CellValue/Expression/ColorScale/DataBar/IconSet/Top10/UniqueValues/DuplicateValues/ContainsText/NotContainsText/BeginsWith/EndsWith/ContainsBlanks/NotContainsBlanks/ContainsErrors/NotContainsErrors/TimePeriod/AboveAverage). |
| operatorType | String | Query | Represents the operator type of conditional format and data validation(Between/Equal/GreaterThan/GreaterOrEqual/LessThan/None/NotBetween/NotEqual). |
| formula1 | String | Query | The value or expression associated with conditional formatting. |
| formula2 | String | Query | The value or expression associated with conditional formatting. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### Success Response

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

| HTTP Code | Reason            | Example Body                              |
| --------- | ----------------- | ------------------------------------------ |
| **200**   | OK – condition added or updated successfully. | `{ "Code": "200", "Status": "OK" }` |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** to call the Aspose.Cells API. The example below shows a complete request, including an empty JSON body.

### Error Responses

| HTTP Code | Reason                                             | Example Body                                                        |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – missing or invalid parameters.       | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – missing or invalid JWT token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist.  | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### cURL Example

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}