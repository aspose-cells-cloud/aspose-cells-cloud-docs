---
title: "Files and Storage"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Learn how to work with Aspose Cells Cloud file storage."
description: "Learn how to work with Aspose Cells Cloud file storage. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Files and Storage
---

Aspose.Cells Cloud provides helper functions to work with files uploaded to Aspose.Cells Cloud Storage or any other Cloud Storage of your choice. If you need any help getting started with setting third party storage please refer to [Aspose Cloud UI Help Topics](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud provides kinds of file/folder/storage operating APIs.**

## How to upload file

### Upload File API Information
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```

The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | Path where to upload including filename and extension e.g. /file.ext or /Folder 1/file.ext If the content is multipart and path does not contains the file name it tries to get them from filename parameter from Content-Disposition header. |
| file | File | formData | File to upload |
| storageName | string | query | Storage name |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/UploadFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
### Upload File Example 

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}} 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}


## How to download file

### Download File API Information 

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
 
### Download File Example 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="14" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
{{< /tabs >}}
 

## How to delete file

### Delete File API Information

 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | File path e.g. '/folder/file.ext' |
| storageName | string | query | Storage name |
| versionId | string | query | File version ID to delete |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/DeleteFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}} 
{{< tab tabNum="16" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}
{{< /tabs >}}
 
## How to copy file

### Copy File Information

 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| srcPath | string | path | Source file path e.g. '/folder/file.ext' |
| destPath | string | query | Destination file path |
| srcStorageName | string | query | Source storage name |
| destStorageName | string | query | Destination storage name |
| versionId | string | query | File version ID to copy |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/CopyFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
### Copy File Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName16="Response" >}}
 
{{< tab tabNum="17" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="18" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}} 
{{< /tabs >}}

## How to move file

### Move File API Information

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

### Move File Example

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
 
## How to create folder

### Create Folder API Information

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | Folder path to create e.g. 'folder_1/folder_2/' |
| storageName | string | query | Storage name |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Create Folder Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```
 
{{< /tab >}}
{{< tab tabNum="4" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
 
```
 
{{< /tab >}} 
{{< /tabs >}}

## How to get files in folder

### Get Files API Information

```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | Folder path e.g. '/folder' |
| storageName | string | query | Storage name |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
### Get Files Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="6" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```
 
{{< /tab >}}
{{< /tabs >}}
 
## How to delete folder

### Delete Folder API Information

 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | Folder path e.g. '/folder' |
| storageName | string | query | Storage name |
| recursive | boolean | query | False |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Delete Folder API Information

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}
 
{{< tab tabNum="7" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}} 
{{< tab tabNum="8" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}} 
{{< /tabs >}}

## How to copy folder

### Copy Folder API Information

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
 
### Copy Folder Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="22" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
{{< /tabs >}}
 

## How to move folder

### Move Folder API Information

 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| srcPath | string | path | Folder path to move e.g. '/folder' |
| destPath | string | query | Destination folder path to move to e.g '/dst' |
| srcStorageName | string | query | Source storage name |
| destStorageName | string | query | Destination storage name |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Move Folder Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}} 
{{< tab tabNum="24" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}} 
{{< /tabs >}}

## How to check if storage exists

### Storage Exists API Information

 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| storageName | string | path | Storage name |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 

### Storage Exists Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}} 
{{< tab tabNum="33" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="34" >}}
 
```bash
{
  "Exists": true
}
 
```
 
{{< /tab >}} 
{{< /tabs >}}


## How to check if file or folder exists

### Object Exists API Information

 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | File or folder path e.g. '/file.ext' or '/folder' |
| storageName | string | query | Storage name |
| versionId | string | query | File version ID |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
### Object Exists Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
{{< tab tabNum="38" >}}
 
```bash
{
  "Exists": true,
  "IsFolder": false
}
 
```
 
{{< /tab >}} 
{{< /tabs >}}


## How to get disc usage

### Get Disc Usage API Information

 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/disc
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| storageName | string | query | Storage name |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Get Disc Usage Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}
 
{{< tab tabNum="40" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}} 
{{< tab tabNum="41" >}}
 
```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
 
```

{{< /tab >}} 
{{< /tabs >}}

## How to get file versions

### Get File Versions API Information

 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | File path e.g. '/file.ext' |
| storageName | string | query | Storage name |

 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Get File Versions Example

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}} 
{{< tab tabNum="47" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}} 
{{< /tabs >}}

