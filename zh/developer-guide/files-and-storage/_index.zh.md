---
title: 文件和存储
second_title: Documen
type: docs
url: /zh/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: 全面指导如何使用 Aspose Cells Cloud 进行文件存储操作，包括上传、下载和管理文件。SDK 支持各种编程语言，例如 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift
weight: 100
kwords: Aspose Cells，云存储，REST API，文件管理，Excel，PDF，CSV，JSON，Markdow
---
 Aspose.Cells Cloud 提供全面的辅助功能，可处理上传到 Aspose.Cells Cloud Storage 或您选择的任何其他云存储的文件。如需设置第三方存储的帮助，请参阅[Aspose 云 UI 帮助主题](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud 提供一系列文件、文件夹和存储操作 API。**

## **如何上传文件**

### 上传文件 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|上传文件的路径，包括文件名和扩展名（例如，/file.ext 或 /Folder 1/file.ext）。如果内容是多部分的，且路径不包含文件名，则会尝试从 Content-Disposition 标头中的 filename 参数中获取文件名。|
|文件|文件|表单数据|要上传的文件|
|存储名称|细绳|询问|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/UploadFile)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 上传文件示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何下载文件**

### 下载文件 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件路径（例如，“/folder/file.ext”）|
|存储名称|细绳|询问|存储名称|
|版本号|细绳|询问|要下载的文件版本ID|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/DownloadFile)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 下载文件示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何删除文件**

### 删除文件 API 信息

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件路径（例如，“/folder/file.ext”）|
|存储名称|细绳|询问|存储名称|
|版本号|细绳|询问|要删除的文件版本 ID|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/DeleteFile)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何复制文件**

### 复制文件 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|源路径|细绳|小路|源文件路径（例如，“/folder/file.ext”）|
|目标路径|细绳|询问|目标文件路径|
|源存储名称|细绳|询问|源存储名称|
|目标存储名称|细绳|询问|目标存储名称|
|版本号|细绳|询问|要复制的文件版本 ID|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/CopyFile)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 复制文件示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

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

## **如何移动文件**

### 移动文件 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|源路径|细绳|小路|源文件路径（例如，“/src.ext”）|
|目标路径|细绳|询问|目标文件路径（例如，“/dest.ext”）|
|源存储名称|细绳|询问|源存储名称|
|目标存储名称|细绳|询问|目标存储名称|
|版本号|细绳|询问|要移动的文件版本 ID|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/File/MoveFile)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 移动文件示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何创建文件夹**

### 创建文件夹 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|要创建的文件夹路径（例如，“文件夹_1/文件夹_2/') |
|存储名称|细绳|询问|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 创建文件夹示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何获取文件夹中的文件**

### 获取文件 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件夹路径（例如“/folder”）|
|存储名称|细绳|询问|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 获取文件示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何删除文件夹**

### 删除文件夹 API 信息

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件夹路径（例如“/folder”）|
|存储名称|细绳|询问|存储名称|
|递归|布尔值|询问|错误的|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 删除文件夹示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何复制文件夹**

### 复制文件夹 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|源路径|细绳|小路|源文件夹路径（例如“/src”）|
|目标路径|细绳|询问|目标文件夹路径（例如“/dst”）|
|源存储名称|细绳|询问|源存储名称|
|目标存储名称|细绳|询问|目标存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 复制文件夹示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何移动文件夹**

### 移动文件夹 API 信息

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|源路径|细绳|小路|要移动的文件夹路径（例如“/folder”）|
|目标路径|细绳|询问|要移动到的目标文件夹路径（例如“/dst”）|
|源存储名称|细绳|询问|源存储名称|
|目标存储名称|细绳|询问|目标存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 移动文件夹示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **如何检查存储是否存在**

### 存储存在 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|存储名称|细绳|小路|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Storage/StorageExists)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 存储存在示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何检查文件或文件夹是否存在**

### 对象存在 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件或文件夹路径（例如，“/file.ext”或“/folder”）|
|存储名称|细绳|询问|存储名称|
|版本号|细绳|询问|文件版本 ID|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 对象存在示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何获取磁盘使用情况**

### 获取磁盘使用情况 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|存储名称|细绳|询问|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 获取磁盘使用情况示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## **如何获取文件版本**

### 获取文件版本 API 信息

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|文件路径（例如，“/file.ext”）|
|存储名称|细绳|询问|存储名称|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互。

### 获取文件版本示例

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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
{{< tab tabnum="47" >}}

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
