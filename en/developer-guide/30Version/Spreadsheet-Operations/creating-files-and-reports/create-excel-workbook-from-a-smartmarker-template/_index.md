---
title: "How to build an Excel report with a smart marker template"
second_title: "Document"
linktitle: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Workbook, SDK"
description: "Learn how to create an Excel workbook using a Smart Marker template with Aspose.Cells Cloud REST API. Includes request parameters, a cURL example, and SDK code samples for multiple languages."
weight: 40
---

This REST API creates a workbook using a Smart Marker template.

**Query Parameters**

| Parameter Name | Type   | Description                                               |
|----------------|--------|-----------------------------------------------------------|
| xmlFile        | string | Path or URL of the SmartMarker XML data file.            |
| outPath        | string | Destination path where the generated workbook will be saved. |
| folder         | string | Folder containing the original workbook.                 |
| storageName    | string | Name of the storage service to use.                       |

**Request Body Parameter**

| Parameter Name | Type | Description                              |
|----------------|------|------------------------------------------|
| xmlFile        | file | SmartMarker template file uploaded with the request. |

## REST API

| **API**                         | **Type** | **Description**                                            | **Swagger Link** |
|---------------------------------|----------|------------------------------------------------------------|------------------|
| /cells/{name}/smartmarker       | POST     | Create a new Excel workbook from a SmartMarker template file | [PostWorkbookGetSmartMarkerResult](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?xmlFile=Sample_SmartMarker_Data.xml" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HttpResponseMessage with the processing result in content.
```

{{< /tab >}}

{{< /tabs >}}

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