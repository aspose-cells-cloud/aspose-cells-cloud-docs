---  
title: "Get Conditional Formatting Rules"  
type: docs  
url: /conditional-formattings/get-all/  
aliases: [/get-conditional-formattings-of-worksheet/]  
keywords: "Aspose.Cells Cloud, REST API, Excel, Conditional Formatting, Worksheet, Conditional Formatting API"  
description: "Retrieve all conditional formatting rules applied to a worksheet using the Aspose.Cells Cloud REST API. Includes request syntax, authentication steps, parameters, concise response examples, and error handling."  
weight: 20  
---  

This REST API retrieves the conditional‑formatting rules that are applied to a worksheet.  

## Prerequisites / Authentication  

The Aspose.Cells Cloud API uses OAuth 2.0. Obtain an access token by sending a **client‑credentials** request to  

```
https://api.aspose.cloud/connect/token
```  

with your **client ID** and **client secret**. The response contains an `access_token` that must be supplied in every request via the `Authorization` header:

```
Authorization: Bearer <access_token>
```  

> **Note** – All examples below use **HTTPS** endpoints.

## REST API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```  

The request parameters are:

| Parameter Name | Type   | Location | Description                                   |
|----------------|--------|----------|-----------------------------------------------|
| name           | string | path     | The name of the Excel file.                   |
| sheetName      | string | path     | The name of the worksheet.                    |
| folder         | string | query    | The folder path where the file is stored.     |
| storageName    | string | query    | The name of the storage service (optional).  |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

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

*The example above shows only the most relevant fields to keep the payload concise.*  

{{< /tab >}}

{{< /tabs >}}

## Error Responses  

| HTTP Status | Description                              | Example JSON |
|-------------|------------------------------------------|--------------|
| 400         | Bad request – missing or invalid parameters. | `{ "Error": "Invalid parameter", "Code": 400 }` |
| 401         | Unauthorized – missing or expired token. | `{ "Error": "Invalid token", "Code": 401 }` |
| 404         | Not found – the file or worksheet does not exist. | `{ "Error": "Resource not found", "Code": 404 }` |
| 500         | Internal server error – unexpected condition on the server. | `{ "Error": "Server error", "Code": 500 }` |

## SDK Source  

The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)

### SDK Examples  

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}