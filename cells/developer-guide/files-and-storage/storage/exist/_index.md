---
title: "Storage Exist"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /storage/exist/
keywords: "Learn how to check storage exist with Aspose Cells Cloud REST API."
description: "Learn how to check storage exist with Aspose Cells Cloud REST API SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
---

This REST API indicates check if `storage exists`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| storageName | string | path | Storage name |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Exists": true
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 