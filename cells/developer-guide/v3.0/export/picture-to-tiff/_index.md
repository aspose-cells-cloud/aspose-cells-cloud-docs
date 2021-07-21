---
title: "Excel Pictures"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /export/excel-picture-to-different-formats/
keywords: "REST API, convert, export，spreadsheets, excel,picture"
description: "Cells.Cloud API for Excel operate: export excel pictures to different format file."
weight: 20
---

You can export formats:  [PNG](https://docs.fileformat.com/Image/png/), [GIF]](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/),  [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/).

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/export|PUT|Export excel objects from request content to some format|[PostExport](https://apireference.aspose.cloud/cells/#/Export/PostExport)|


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Export/PostExport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.


{{< tabs tabTotal="1" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="2" >}}
```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
        "FileSize": 21680,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
        "FileSize": 21286,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
        "FileSize": 130084,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
        "FileSize": 120062,
        "FileContent": "-----Base64String--------"
    }]
}
```
{{< /tab >}}
{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
