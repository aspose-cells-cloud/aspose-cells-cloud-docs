---
title: "Files and Storage"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "REST API, upload, download, delelte, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: upload, download and delete excel file to storage."
weight: 100
---

Aspose.Cells Cloud provides helper functions to work with files uploaded to Aspose.Cells Cloud Storage or any other Cloud Storage of your choice. If you need any help getting started with setting third party storage please refer to [Aspose Cloud UI Help Topics](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

## Downloading a file from Cloud Storage

|API|Type|Description|Swagger Link|
| :- | :- | :- | :- |
|/cells/storage/file/{path}|GET|Download a File from Storage|[DownloadFile](https://apireference.aspose.cloud/cells/#/File/DownloadFile)|

You can use cURL command-line utility to test this REST API. The following example shows how to make calls to Cloud API with cURL.

{{< nosnippet >}}
{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}
{{< tab tabNum="1" >}}

```bash
curl -v -X GET "https://api.aspose.cloud/v3.0/cells/storage/file/sample.docx" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```
<p style="margin-top:-32px;font-size:80%;font-style:italic">To get a JWT token use this <a href="/cells/getting-started/quickstart/">instruction</a></p>

{{< /tab >}}
{{< /tabs >}}
{{< /nosnippet >}}

## Uploading a file to Cloud Storage

|API|Type|Description|Swagger Link|
| :- | :- | :- | :- |
|/cells/storage/file/{path}|PUT|Upload a file to Cloud Storage|[UploadFile](https://apireference.aspose.cloud/cells/#/File/UploadFile)|

The following code demonstrates how to upload a file to Cloud Storage with cURL.

{{< nosnippet >}}
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl  -v -X PUT "https://api.aspose.cloud/v3.0/cells/storage/file/sample.xlsx" \
-H "Content-Type:application/octet-stream" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```
<p style="margin-top:-32px;font-size:80%;font-style:italic">To get a JWT token use this <a href="/cells/getting-started/quickstart/">instruction</a></p>

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
   "uploaded":[
      "sample.xlsx"
   ],
   "errors":[
   ]
}
```

{{< /tab >}}
{{< /tabs >}}
{{< /nosnippet >}}

## Copying a file to a new location in Cloud Storage

|API|Type|Description|Swagger Link|
| :- | :- | :- | :- |
|/cells/storage/file/copy/{srcPath}|PUT|Duplicate a file to a new location on Cloud Storage|[CopyFile](https://apireference.aspose.cloud/cells/#/File/CopyFile)|

The following code demonstrates how to copy a file to a new location in Cloud Storage with cURL.

{{< nosnippet >}}
{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}
{{< tab tabNum="1" >}}

```bash
curl -v -X PUT "https://api.aspose.cloud/v3.0/cells/storage/file/copy/sample.xlsx/%2F?destPath=MyFolder" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```
<p style="margin-top:-32px;font-size:80%;font-style:italic">To get a JWT token use this <a href="/cells/getting-started/quickstart/">instruction</a></p>

{{< /tab >}}
{{< /tabs >}}
{{< /nosnippet >}}

## Moving a file to a new location in Cloud Storage

|API|Type|Description|Swagger Link|
| :- | :- | :- | :- |
|/cells/storage/file/MOVE/{srcPath}|PUT|Move a file to a new location on Cloud Storage|[MoveFile](https://apireference.aspose.cloud/cells/#/File/MoveFile)|

The following code demonstrates how to move a file to a new location in Cloud Storage with cURL.

{{< nosnippet >}}
{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}
{{< tab tabNum="11" >}}

```bash
curl -v -X PUT "https://api.aspose.cloud/v3.0/cells/storage/file/move/input.xlsx/%2F?destPath=MyFolder" \
-H "Content-Type:application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```
<p style="margin-top:-32px;font-size:80%;font-style:italic">To get a JWT token use this <a href="/cells/getting-started/quickstart/">instruction</a></p>

{{< /tab >}}
{{< /tabs >}}
{{< /nosnippet >}}

## Deleting a file from Cloud Storage

|API|Type|Description|Swagger Link|
| :- | :- | :- | :- |
|/cells/storage/file/{path}|DELETE|Delete a file from Cloud Storage|[DeleteFile](https://apireference.aspose.cloud/cells/#/File/DeleteFile)|

The following code demonstrates how to delete a file from Cloud Storage with cURL.

{{< nosnippet >}}
{{< tabs tabTotal="1" tabID="14" tabName14="Request" >}}
{{< tab tabNum="14" >}}

```bash
curl -v -X DELETE "https://api.aspose.cloud/v3.0/cells/storage/file/input.xlsx" \
-H "Content-Type:application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```
<p style="margin-top:-32px;font-size:80%;font-style:italic">To get a JWT token use this <a href="/cells/getting-started/quickstart/">instruction</a></p>

{{< /tab >}}
{{< /tabs >}}
{{< /nosnippet >}}
