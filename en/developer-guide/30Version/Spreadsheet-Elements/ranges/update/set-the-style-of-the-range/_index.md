---  
title: "Set Range Style – Aspose.Cells Cloud API"  
second_title: "Documentation"  
linktitle: "Set Range Style"  
type: docs  
url: /ranges/update/style/  
aliases: [/set-the-style-of-the-range/]  
keywords: "Aspose.Cells, range style, API, Excel, cloud"  
description: "Learn how to set the style of a cell range in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes authentication steps, request format, response details, and SDK examples for .NET, Java, Python, Go, and more."  
weight: 70  
---  

## **Introduction**  
This example demonstrates how to set the style of a range using the Aspose.Cells Cloud API. You can call the API from many programming languages, such as .NET, Java, PHP, Ruby, Python, JavaScript (jQuery), and others.  

## **API Information**  

| API                                                   | Type | Description                     | Resource Link                                                                                                                                 |
| ----------------------------------------------------- | ---- | -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Set the cell style of a named range | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL Example**  

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

**Prerequisites**  
1. Obtain an access token via the OAuth2 client‑credentials flow (`POST https://api.aspose.cloud/connect/token`).  
2. Include the header `Authorization: Bearer <access_token>` in every request.  

**Request**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*The `Range` object specifies the top‑left cell and the size of the range. The `Style` object contains the formatting options to apply.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**Response**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Error handling** – For unsuccessful calls the API returns an appropriate HTTP status code (e.g., 400, 401, 500) together with a JSON body that includes `Error` and `Message` fields. Inspect the `Code` value; any non‑200 result should be logged and processed according to your error‑handling policy.  

{{< /tab >}}

{{< /tabs >}}

## **SDK Source**  
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)

### **SDK Examples**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}