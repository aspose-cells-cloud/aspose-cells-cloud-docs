---
title: "Get Conditional Formatting Rules"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, Conditional Formatting, Worksheet, Conditional Formatting API"
description: "Get all conditional formatting rules from a worksheet via Aspose.Cells Cloud REST API with cURL and SDK examples"
weight: 100
linktitle: "Get Conditional Formatting Rules"
ArticleTitle: "Get All Conditional Formatting Rules from Worksheet via Aspose.Cells Cloud API"
---
The **GetWorksheetConditionalFormattings** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings`) retrieves descriptions of all conditional formatting rules applied to a specified worksheet in a cloud-stored spreadsheet file, enabling developers to inspect formatting logic programmatically via Aspose.Cells Cloud's REST API, which supports multiple SDKs including .NET, Java, Python, and Node.js.

## The Get Worksheet Conditional Formattings Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worksheet name.                          |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

### Response

```json
[
  {
    "Name": "ConditionalFormattingsResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ConditionalFormattingsResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| HTTP Code | Reason                                             | Example Body                                                        |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – missing or invalid parameters.       | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – missing or invalid JWT token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist.  | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

The <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_The example above shows only the most relevant fields to keep the payload concise._

**Response Parameters**

| Parameter                                        | Type    | Description                                                    |
| ------------------------------------------------ | ------- | -------------------------------------------------------------- |
| Status                                           | string  | Result status of the request (e.g., **OK**).                   |
| ConditionalFormattings                           | object  | Container for conditional formatting data.                     |
| ConditionalFormattings.Count                     | integer | Number of conditional formatting rules returned.               |
| ConditionalFormattings.ConditionalFormattingList | array   | List of conditional formatting objects.                        |
| ConditionalFormattingList[].sqref                | string  | Cell range to which the formatting applies (e.g., **A1:B10**). |
| ConditionalFormattingList[].FormatConditions     | array   | Collection of format condition objects for the range.          |
| FormatConditions[].Priority                      | integer | Evaluation priority of the condition.                          |
| FormatConditions[].Type                          | string  | Type of condition (e.g., **CellValue**).                       |
| FormatConditions[].Operator                      | string  | Operator used for the condition (e.g., **GreaterThan**).       |
| FormatConditions[].Formula1                      | string  | First formula or value for the condition.                      |
| FormatConditions[].Style                         | object  | Styling applied when the condition is met.                     |
| Style.Font.Color                                 | object  | RGBA color definition for the font.                            |
| Style.Font.IsBold                                | boolean | Indicates whether the font is bold.                            |

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

{{< /tab >}}

{{< /tabs >}}

## How to Use the Get Worksheet Conditional Formattings API with SDKs?

### Get Worksheet Conditional Formattings API Specification

The <a href="https://reference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" rel="noopener noreferrer">Get Worksheet Conditional Formattings API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetConditionalFormattings.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetConditionalFormattings.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetConditionalFormattings.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetConditionalFormattings.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetConditionalFormattings.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetConditionalFormattings.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetConditionalFormattings.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetConditionalFormattings.go" >}}
{{</tab>}}
{{< /tabs >}}
