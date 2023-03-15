---
title: 使用存储导入数据
second_title: Aspose.Cells Cloud Documen
linktitle: 使用存储导入数据
type: docs
url: /zh/import/with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/]
description: Cells.Cloud API for Excel操作：Import Data into Excel Worksheet
weight: 10
---
这个 REST API 表示 `import data` 到 Excel 文件。
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路||
|文件夹|细绳|询问||
|存储名称|细绳|询问|存储名称。|
|导入数据||身体||

**导入数据选项参数**描述于[参考链接](/cells/zh/import/#import-data-option-parameter).

 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
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
 
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

