---
title: "Flip Data"
ArticleTitle: "Flip Data – Aspose.Cells Cloud"
second_title: "Developer Guide"
linktitle: "Flip Data"
type: docs
url: /flip
aliases: []
keywords: "Flip Data, Transform, Aspose.Cells"
description: "Transposes a specified data range in a spreadsheet file."
weight: 100
---
The **FlipData** API (`PUT https://api.aspose.cloud/v4.0/cells/flip`) in Aspose.Cells Cloud transposes a specified data range by flipping its orientation—rows become columns and columns become rows—enabling restructuring of data matrices (e.g., converting a 3x2 range into a 2x3 range) to meet input requirements for charts, reports, or data models; it accepts a spreadsheet file, worksheet name, and cell area as required parameters.

## The Flip Data Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | The worksheet name. |
| cellArea | String | Query | A specified data range |
| Horizontal | Boolean | Query | Horizontal/Vertical Flip. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
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

**Response Status Codes**

This API flips the orientation of a given data matrix. For example, a 3x2 range (3 rows, 2 columns) will become a 2x3 range (2 rows, 3 columns) in the output. It is commonly used for restructuring data to meet the input requirements of different charts, reports, or data models.

### Request Body Parameter

| Parameter Name | Type  | Description                                                                     |
| -------------- | ----- | ------------------------------------------------------------------------------- |
| _None_         | _N/A_ | _No additional JSON body is required; the file is sent as multipart/form-data._ |

## How to Use the FlipData with SDKs

### FlipData Specification

The [FlipData API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<binary stream of the transformed workbook>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
