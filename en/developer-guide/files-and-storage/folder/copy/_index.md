---
title: "Copy Folder"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /folder/copy/
keywords: "Learn how to copy folder with Aspose Cells Cloud REST API."
description: "Learn how to copy folder with Aspose Cells Cloud REST API SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
---

This REST API indicates `copy folder`.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| srcPath | string | path | Source folder path e.g. '/src' |
| destPath | string | query | Destination folder path e.g. '/dst' |
| srcStorageName | string | query | Source storage name |
| destStorageName | string | query | Destination storage name |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 