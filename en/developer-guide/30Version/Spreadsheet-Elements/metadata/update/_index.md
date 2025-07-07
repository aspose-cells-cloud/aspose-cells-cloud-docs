---
title: "Update Metadata"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Update without using storage"
type: docs
url: /metadata/update/
keywords: "Update metadata on excel files."
description: "Aspose.Cells Cloud REST API support updating metadata on excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 35
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Update Metadata
---

This REST API indicates to update  `metadata`  from multiple Excel files.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/metadata/update
 
```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| file | file | formData | File to upload |
| DocumentProperties |  | body | Cells document property. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PostMetadata) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/metadata/update" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'  \
-d '[{name="test",value="test"}]'
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
