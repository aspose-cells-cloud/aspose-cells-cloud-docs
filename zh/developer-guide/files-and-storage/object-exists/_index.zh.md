---
title: 对象存在
second_title: Documen
linktitle: 对象存在
type: docs
url: /zh/object-exists/
keywords: Excel API, Object Exists, REST API, Aspose, File Management, Excel, Office Cloud, Spreadsheet, PDF, CSV, JSON, Markdow
description: 对象存在 API 检查指定的文件或文件夹是否存在于 Aspose.Cells 云存储中
weight: 100
kwords: Excel API，对象存在，REST API，Aspose，Office 云，文件管理，电子表格，PDF，CSV，JSON，Markdown，检查 Excel 中的文件是否存在
---
## **Excel API：对象存在**

```
GET http://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **功能描述**

`objectExists` API 允许开发人员验证 Aspose.Cells 云存储中指定文件或文件夹的存在。

### 请求参数**对象存在**API 是

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|云存储中文件或文件夹的路径。|
|存储名称|细绳|询问|文件所在存储的名称。|
|版本号|细绳|询问|文件的版本 ID（如果适用）。|

### **响应描述**

```json
{
  "Name": "ObjectExist",
  "Description": [
    "Object exists"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates that the file or folder exists."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    },
    {
      "Name": "IsFolder",
      "Description": [
        "True if it is a folder, false if it is a file."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
