---
title: "Export Chart"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Chart"
type: docs
url: /export/excel-chart-to-different-formats/
keywords: "Export Excel chart to kinds of format files."
description: "Aspose.Cells Cloud REST API support exporting Excel chart to kinds of format files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 20
---


You can export formats:  [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/),  [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), [PDF](https://docs.fileformat.com/pdf/).

- **REST API**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/export|POST|Export Excel objects from request content to some format|[PostExport](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)|


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.


- **Request**
```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Response**

```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
        "FileSize": 10040,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
        "FileSize": 12978,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
        "FileSize": 7002,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
        "FileSize": 11532,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
        "FileSize": 8270,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
        "FileSize": 42570,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
        "FileSize": 12102,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
        "FileSize": 8290,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-chart-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export-chart-tiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< /tabs >}}
