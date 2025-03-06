---
title: "Repair"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /repair-excel-files/
keywords: "Repair Excel, ODS, WPS, and so on files."
description: "Repair Excel files using Aspose.Cells Cloud REST API. The API supports multiple development languages ​​including Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby and Swift for quick integration in your projects."
weight: 39
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Repair
---

This REST API indicates to `repair` Excel files.

- Repair XLS, XLSX, XLSM, XLSB, ODS, and so on.
- Support multi-files.

Aspose.Cells Cloud Excel Repair recovers data from corrupt Excel files online without installation. Corrupted Excel files can be a problem because you won't be able to open them. You can try the Aspose.Cells Cloud Excel Repair App to recover data from corrupted Excel files.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| file | file | formData | File to upload |
| format | string | query |  Output format, Default value is null, output format is equal to input file format. |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
    "Files":
    [
        {
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        {
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```

{{< /tab >}}

{{< /tabs >}}



## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}


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

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "" >}}
{{< /tab >}}

{{< /tabs >}}
