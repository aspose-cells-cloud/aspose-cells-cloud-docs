---
title: "Move File"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /file/move/
keywords: "REST API, upload, download, delelte, copy, move, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: upload, download and delete excel file to storage."
weight: 100
---

This REST API indicates `move file`
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| srcPath | string | path | Source file path e.g. '/src.ext' |
| destPath | string | query | Destination file path e.g. '/dest.ext' |
| srcStorageName | string | query | Source storage name |
| destStorageName | string | query | Destination storage name |
| versionId | string | query | File version ID to move |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/MoveFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
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
 
 