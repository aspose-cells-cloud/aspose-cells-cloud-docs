---
title: "Excel"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /export/excel-to-different-formats/
keywords: "REST API, convert, export，spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: export excel file to different format file."
weight: 20
---


## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/export|PUT|Export excel objects from request content to some format|[PostExport](https://apireference.aspose.cloud/cells/#/Export/PostExport)|


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Export/PostExport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.


{{< tabs tabTotal="1" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="2" >}}
```bash
{
    "Files":
    [
        { 
            "Filename":"Book1_xlsx.tif",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"myDocument_xlsx.tif",
            "FileSize":348126,
            "FileContent":"-----Base64String--------"
        }
    ]
}
```
{{< /tab >}}
{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
