---
title: "Aspose.Cells Cloud API – File & Folder Management (Upload, Download, Copy, Move)"
second_title: "Document"
ArticleTitle: "Cloud File Management for Excel – An Efficient and Secure Solution for Excel File Storage and Intelligent Organization"
linktitle: "Files and Storage"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud, file storage API, upload Excel file, download Excel file, copy file, move file, delete file, folder management, REST API, cURL examples"
description: "Comprehensive guide to managing Excel files and folders in Aspose.Cells Cloud storage. Includes upload, download, copy, move, delete, and folder operations with cURL examples, required parameters, and authentication notes."
weight: 100
---

Aspose.Cells Cloud provides a comprehensive set of helper functions for working with files stored in Aspose.Cells Cloud Storage or any third‑party cloud storage of your choice. For assistance with setting up third‑party storage, please refer to [Aspose Cloud UI Help Topics](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud offers a range of file, folder, and storage operation APIs.**

> **Note:** All API calls must use **HTTPS**. See the [Authentication Guide](/cells/authentication/) for details on obtaining a JWT token.

**Prerequisites:** To use these APIs you must have a valid Aspose Cloud account, obtain a JWT access token, and have a storage location configured (either Aspose Cloud Storage or a connected third‑party storage).

**Last updated:** 2024‑12‑01

## **How to Upload a File**

### Upload File API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | Path to upload the file, including the filename and extension (e.g., `/folder1/Report.xlsx`). |
| file           | file   | formData | The file to upload. |
| storageName    | string | query    | Name of the storage to use. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | File uploaded successfully.              |
| 400  | Bad request – missing or invalid parameters. |
| 401  | Unauthorized – invalid or missing JWT token. |
| 404  | Storage not found.                       |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/UploadFile) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Upload File Example

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to upload a file with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: The maximum file size for upload is 100 MB. Rate limits may apply.*

## **How to Download a File**

### Download File API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | File path (e.g., `/folder/Report.xlsx`). |
| storageName    | string | query    | Name of the storage to use. |
| versionId      | string | query    | Identifier of the file version to download (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | File downloaded; binary stream returned. |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | File not found.                          |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/DownloadFile) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Download File Example

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<binary data>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: The response contains the file’s binary stream. Save the output to a file when using cURL (`-o filename.xlsx`).*

## **How to Delete a File**

### Delete File API Information

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | File path (e.g., `/folder/Report.xlsx`). |
| storageName    | string | query    | Name of the storage to use. |
| versionId      | string | query    | Identifier of the file version to delete (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | File deleted successfully.               |
| 400  | Bad request – missing or invalid parameters. |
| 401  | Unauthorized – invalid JWT token.        |
| 404  | File not found.                          |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/DeleteFile) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Delete File Example

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: Deleting a file is permanent; ensure you have a backup if needed.*

## **How to Copy a File**

### Copy File API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

The request parameters are listed below:

| Parameter Name   | Type   | Location | Description |
|------------------|--------|----------|-------------|
| srcPath          | string | path     | Source file path (e.g., `/folder/Source.xlsx`). |
| destPath         | string | query    | Destination file path (e.g., `/folder/Destination.xlsx`). |
| srcStorageName   | string | query    | Source storage name (optional). |
| destStorageName  | string | query    | Destination storage name (optional). |
| versionId        | string | query    | File version ID to copy (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | File copied successfully.                |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Source file not found.                   |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/CopyFile) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Copy File Example

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: The copy operation does not remove the source file.*

## **How to Move a File**

### Move File API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

The request parameters are listed below:

| Parameter Name   | Type   | Location | Description |
|------------------|--------|----------|-------------|
| srcPath          | string | path     | Source file path (e.g., `/folder/Source.xlsx`). |
| destPath         | string | query    | Destination file path (e.g., `/folder/Destination.xlsx`). |
| srcStorageName   | string | query    | Source storage name (optional). |
| destStorageName  | string | query    | Destination storage name (optional). |
| versionId        | string | query    | File version ID to move (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | File moved successfully.                 |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Source file not found.                   |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/MoveFile) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Move File Example

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: Moving a file retains the file’s version history.*

## **How to Create a Folder**

### Create Folder API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | Folder path to create (e.g., `folder1/folder2/`). |
| storageName    | string | query    | Name of the storage to use. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Folder created successfully.             |
| 400  | Bad request – invalid path or parameters. |
| 401  | Unauthorized – missing or invalid JWT.   |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Create Folder Example

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: Folder paths are case‑sensitive.*

## **How to Get Files in a Folder**

### Get Files API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | Folder path (e.g., `/folder`). |
| storageName    | string | query    | Name of the storage to use. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | List of files and sub‑folders returned.  |
| 400  | Bad request – invalid path.              |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Folder not found.                        |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Get Files Example

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: The response lists both files and sub‑folders within the specified path.*

## **How to Delete a Folder**

### Delete Folder API Information

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

The request parameters are listed below:

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| path           | string  | path     | Folder path (e.g., `/folder`). |
| storageName    | string  | query    | Name of the storage to use. |
| recursive      | boolean | query    | Set to `true` to delete the folder recursively. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Folder deleted successfully.             |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Folder not found.                        |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Delete Folder Example

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: Deleting a folder with `recursive=true` removes all its contents permanently.*

## **How to Copy a Folder**

### Copy Folder API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

The request parameters are listed below:

| Parameter Name   | Type   | Location | Description |
|------------------|--------|----------|-------------|
| srcPath          | string | path     | Source folder path (e.g., `/src`). |
| destPath         | string | query    | Destination folder path (e.g., `/dst`). |
| srcStorageName   | string | query    | Source storage name (optional). |
| destStorageName  | string | query    | Destination storage name (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Folder copied successfully.              |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Source folder not found.                 |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Copy Folder Example

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: The copy operation creates a new folder with the same contents as the source.*

## **How to Move a Folder**

### Move Folder API Information

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

The request parameters are listed below:

| Parameter Name   | Type   | Location | Description |
|------------------|--------|----------|-------------|
| srcPath          | string | path     | Source folder path (e.g., `/folder`). |
| destPath         | string | query    | Destination folder path (e.g., `/dst`). |
| srcStorageName   | string | query    | Source storage name (optional). |
| destStorageName  | string | query    | Destination storage name (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Folder moved successfully.               |
| 400  | Bad request – invalid parameters.        |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Source folder not found.                 |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Move Folder Example

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Note: Moving a folder retains its internal structure and file versions.*

## **How to Check if Storage Exists**

### Storage Exists API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| storageName    | string | path     | Name of the storage to check. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Storage existence returned (`true` or `false`). |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | Storage not found.                       |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Storage Exists Example

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **How to Check if a File or Folder Exists**

### Object Exists API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | File or folder path (e.g., `/file.xlsx` or `/folder`). |
| storageName    | string | query    | Name of the storage to check. |
| versionId      | string | query    | File version identifier (optional). |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Existence information returned.          |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | File or folder not found.                |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Object Exists Example

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **How to Get Disk Usage**

### Get Disk Usage API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| storageName    | string | query    | Name of the storage to query. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | Disk usage information returned.         |
| 401  | Unauthorized – missing or invalid JWT.   |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Get Disk Usage Example

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **How to Get File Versions**

### Get File Versions API Information

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| path           | string | path     | File path (e.g., `/file.xlsx`). |
| storageName    | string | query    | Name of the storage to query. |

**HTTP Responses**

| Code | Description                              |
|------|------------------------------------------|
| 200  | List of file versions returned.          |
| 401  | Unauthorized – missing or invalid JWT.   |
| 404  | File not found.                          |
| 500  | Internal server error.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) defines a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Get File Versions Example

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}