---
title: "ConvertRangeToPdf"
ArticleTitle: "Convert Range to PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "ConvertRangeToPdf"
type: docs
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, Convert Range to PDF, API"
description: "Converts a specified range of a spreadsheet to PDF using Aspose.Cells Cloud."
weight: 1
---

## The ConvertRangeToPdf of Aspose.Cells Cloud Web Services

Converts a range of spreadsheet on a local drive to the pdf file.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                                                                                                                    |
|------------------|--------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file.                                                                                                                       |
| worksheet        | String | Query                       | worksheet name of spreadsheet.                                                                                                                |
| range            | String | Query                       | cell area. e.g. A1:C10                                                                                                                         |
| outPath          | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                                 |
| outStorageName   | String | Query                       | Output file Storage Name.                                                                                                                      |
| fontsLocation    | String | Query                       | Use Custom fonts.                                                                                                                              |
| AutoRowsFit      | Boolean| Query                       | (Optional) Autofits all rows in worksheets.                                                                                                   |
| AutoColumnsFit   | Boolean| Query                       | (Optional) Autofits all columns in worksheets.                                                                                                |
| region           | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior.       |
| password         | String | Query                       | The password for opening spreadsheet file.                                                                                                     |

### Request Body Parameter

| Parameter Name | Type | Description |
|----------------|------|-------------|
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "file": "<binary PDF content>"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Successful conversion; returns the generated PDF file stream. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

## How to Use the ConvertRangeToPdf with SDKs

### ConvertRangeToPdf Specification

The [ConvertRangeToPdf API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binary PDF content>"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
```csharp
// SDK example code for C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// SDK example code for Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# SDK example code for Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// SDK example code for JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`