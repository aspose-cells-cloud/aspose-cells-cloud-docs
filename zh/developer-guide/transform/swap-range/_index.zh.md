---
title: Aspose.Cells Cloud Web API - 在电子表格中交换范围
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: 交换范围
type: docs
url: /zh/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: Excel 和 API 的交换范围功能提供了一个强大的工具，可以交换 Excel 文件中的任意两列、两行、两个范围或单个单元格。此 API 功能允许用户高效地重新排列表格，确保原始数据格式得以保留，所有现有公式继续正常运行。通过利用此 API 功能，用户可以简化数据操作任务并保持电子表格的完整性。
weight: 100
kwords: Excel, Office 云, REST, PDF, CSV, Json, Markdown
---
在 Excel 文件中的任意两列、行、范围或单个单元格之间交换数据。

## **掉期范围 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|工作表1|细绳|询问|指定作为交换数据区域源的工作表。|
|范围1|细绳|询问|指定交换数据的来源。|
|工作表2|细绳|询问|指定作为交换数据区域目标的工作表。|
|范围2|细绳|询问|指定交换数据的目标。|
|输出路径|细绳|询问|（可选）存储工作簿的文件夹路径。默认值为 null。|
|输出存储名称|细绳|询问|输出文件存储名称。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

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

## 我们应该在哪里使用交换范围 API？

当您需要在电子表格中交换范围数据时，可以使用这个 API。

## 为什么要使用交换范围 API？

- 在 Excel 电子表格中快速交换范围数据。
- 通过现有的SDK即可快速完成开发。

## 如何将掉期范围 API 与 SDK 结合使用

### 掉期范围 API 规格

这[掉期范围 API 规格](https://reference.aspose.cloud/cells/#/TransformController/SwapRange)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码交换范围。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
