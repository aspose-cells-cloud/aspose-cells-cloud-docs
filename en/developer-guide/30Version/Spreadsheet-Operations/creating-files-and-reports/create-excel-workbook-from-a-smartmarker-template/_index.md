---
title: "Build Excel Reports with Smart Marker Templates"
second_title: "Document"
linktitle: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Workbook, SDK, API"
description: "Learn how to generate Excel workbooks from Smart Marker templates using the Aspose.Cells Cloud REST API. Includes request/response details, cURL example, and SDK code samples."
weight: 40
---

This REST API creates a workbook using a Smart Marker template.

**What is a Smart Marker?**  
A Smart Marker is a placeholder syntax that maps data fields in an XML (or JSON) file to cells in an Excel template. At runtime Aspose.Cells replaces the markers with the corresponding data, allowing you to generate fully populated reports programmatically.

**Prerequisites**  
Before calling the API, ensure you have:

* A valid Aspose Cloud API key and access token.  
* The template workbook stored in your chosen storage (or included in the request).  
* A Smart Marker XML data file that follows the Aspose Smart Marker schema.  

**Query Parameters**

| Parameter Name | Type   | Description                                                               |
|----------------|--------|---------------------------------------------------------------------------|
| outPath        | string | Destination path where the generated workbook will be saved.             |
| folder         | string | Folder containing the original workbook.                                 |
| storageName    | string | Name of the storage service to use.                                       |

**Request Body Parameter**

| Parameter Name | Type | Description                                            |
|----------------|------|--------------------------------------------------------|
| xmlFile        | file | Smart Marker XML data file uploaded with the request. |

## REST API

| **API**                         | **Type** | **Description**                                            | **Swagger Link** |
|---------------------------------|----------|------------------------------------------------------------|------------------|
| /cells/{name}/smartmarker       | POST     | Create a new Excel workbook from a Smart Marker template file | [PostWorkbookGetSmartMarkerResult](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "status": "OK",
  "message": "Workbook generated successfully.",
  "downloadUrl": "https://api.aspose.cloud/v3.0/storage/file/GeneratedReport.xlsx"
}
```

{{< /tab >}}

{{< /tabs >}}

**Error Handling**  

| HTTP Status | Description                              | Typical Cause                                 |
|-------------|------------------------------------------|-----------------------------------------------|
| 400         | Bad Request                              | Missing template, malformed XML, or invalid parameters. |
| 401         | Unauthorized                             | Invalid or missing authentication token.      |
| 404         | Not Found                                | Specified workbook or storage location does not exist. |
| 500         | Internal Server Error                    | Unexpected server‑side failure.               |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}