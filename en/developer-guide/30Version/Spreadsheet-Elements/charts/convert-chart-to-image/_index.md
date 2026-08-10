---
title: "Convert Excel Chart to Image – Aspose.Cells Cloud REST API"
type: docs
url: /charts/to-image/
aliases: [/convert-charts-to-image/]
weight: 50
keywords: "Aspose.Cells Cloud, chart to image, Excel chart conversion, REST API, image format, PNG, JPEG, BMP, TIFF, GIF"
description: "Learn how to convert Excel chart objects to PNG, JPEG, BMP, TIFF, or GIF images using Aspise.Cells Cloud REST API. Includes endpoint details, parameters, cURL example, SDK snippets, response example, and error handling."
ArticleTitle: "Convert Excel Chart to Image – Aspose.Cells Cloud REST API"
---

This REST API demonstrates how to convert an **Excel chart** to an image using **Aspose.Cells Cloud**.

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Supported image formats include `png`, `jpeg`, `bmp`, `tiff`, and `gif`.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description               |
| -------------- | ------- | -------- | ------------------------- |
| name           | string  | path     | Document name.            |
| sheetName      | string  | path     | Worksheet name.           |
| chartNumber    | integer | path     | The chart number.         |
| format         | string  | query    | The exported file format. |
| folder         | string  | query    | The document folder.      |
| storageName    | string  | query    | Storage name.             |

### **Response**

The endpoint returns the image file in the requested format as a binary stream (e.g., `byte[]`). The response `Content‑Type` header matches the selected image format such as `image/png`, `image/jpeg`, etc.

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PutWorksheetAddChart API with SDKs

### PutWorksheetAddChart API Specification

The <a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Example coming soon.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}