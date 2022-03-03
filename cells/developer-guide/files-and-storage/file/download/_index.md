---
title: "Download File"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /file/download/
keywords: "Learn how to download file with Aspose Cells Cloud REST API."
description: "Learn how to download file with Aspose Cells Cloud REST API SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
---

This REST API indicates `download file`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | File path e.g. '/folder/file.ext' |
| storageName | string | query | Storage name |
| versionId | string | query | File version ID to download |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/DownloadFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 
 
 

