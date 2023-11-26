---
title: 将Json数据导入Exce
second_title: Aspose.Cells Cloud Documen
linktitle: 导入JSO
type: docs
url: /zh/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API 支持将字符串数组数据导入到 Excel 文件中。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 40
---
此 REST API `import json data` 到 Excel 工作表中。


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

重要参数说明如下表：


**导入字符串数组选项**

|参数名称|类型|描述|
|:- |:- |:- |
|姓名|细绳|作业簿名称|
|导入Json请求|班级|导入json请求。|
|密码|细绳|工作簿的密码。|
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|存储名称。|
|输出路径|细绳|输出文件路径。|
|输出存储名称|细绳|输出文件的存储名称。|
|检查Excel限制|细绳|检查 Excel 限制。|


**例子**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## 云SDK系列

使用 SDK 是加快开发速度的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：





