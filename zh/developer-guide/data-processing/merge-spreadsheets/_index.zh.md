---
title: Aspose.Cells Cloud Web API - 将多个电子表格合并为一个电子表格
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: 合并电子表格
type: docs
url: /zh/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: 使用 Excel API 轻松将本地电子表格文件合并为各种格式（XLSX、CSV、PDF）
weight: 100
kwords: Excel API，合并电子表格，Office 云，REST API，电子表格合并，CSV 格式，JSON，Markdow
---
将多个本地电子表格文件合并为一个文件，同时支持 30 多种文件格式的输出。

## **合并电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|输出格式|细绳|询问|指定输出文件格式。|
|合并到一张表中|布尔值|询问|指示是否将所有数据合并到单个工作表中。|
|输出路径|细绳|询问| （可选）输出工作簿的文件夹路径。默认为 null。|
|输出存储名称|细绳|询问|指定输出文件存储名称。|
|字体位置|细绳|询问|定义要使用的自定义字体。|
|地区|细绳|询问|设置电子表格区域。|
|密码|细绳|询问|提供打开电子表格文件的密码。|

### **回复**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用合并本地电子表格 API？

当您需要将多个数据文件合并在一起时，您可以使用这个API。

## 为什么要使用合并本地电子表格 API？

- 无需云存储空间，直接合并即可。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 合并本地电子表格 API

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)提供可公开访问的编程接口，允许用户直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将多个电子表格合并为一个电子表格。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
