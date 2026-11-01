---
title: "Set Range Style – Aspose.Cells Cloud API"  
second_title: "Documentation"  
linktitle: "Set Range Style"  
type: docs  
url: /ranges/update/style/  
aliases: [/set-the-style-of-the-range/]  
keywords: "Aspose.Cells, range style, API, Excel, cloud"  
description: "Update Excel range style using Aspose.Cells Cloud API: POST /cells/{name}/worksheets/{sheetName}/ranges/style"
weight: 70  
ArticleTitle: "Set Range Style in Excel via Aspose.Cells Cloud REST API"
---
The **PostWorksheetCellsRangeStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/style`) enables developers to set the style for a specified range in a worksheet using Aspose.Cells Cloud, allowing programmatic formatting of cell ranges such as applying fonts, borders, and fill patterns. The operation requires the workbook name, worksheet name, and a `RangeSetStyleRequest` body containing the desired style settings, with optional query parameters for folder and storage name. This REST API supports integration across multiple programming languages, including .NET, Java, Python, and JavaScript, streamlining spreadsheet styling workflows in cloud-based applications.

## The Post Worksheet Cells Range Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/style
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| rangeOperate | class:rangesetstylerequest | HTTPBody | RangeSetStyleRequest Range Set Style Request |
| folder | String | Query | Original workbook folder. |
| storageName | String | Query | Storage name. |

### **Response**

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

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