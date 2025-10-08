---
title: Aspose.Cells Cloud Web API - 将电子表格范围数据转换为 CSV 文件
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: 将范围转换为 CS
type: docs
url: /zh/convert-range-to-csv/
keywords: Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to cs
description: 使用 Excel API 将指定范围从本地电子表格文件转换为 CSV 格式，确保无缝云执行
weight: 100
kwords: 范围转为 csv，将电子表格转为 csv，Aspose Cloud Web API，云转换，Excel 转为 csv
---
将本地电子表格/Excel 文件中的范围数据转换为[CSV](https://docs.fileformat.com/spreadsheet/csv/)文件。

## **将范围转换为 CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|工作表|细绳|询问|电子表格/Excel的工作表名称|
|范围|细绳|询问|指定单元格区域（例如，A1:C10）。|
|输出路径|细绳|询问|（可选）存储工作簿的文件夹路径。默认值为空。|
|输出存储名称|细绳|询问|输出文件存储的名称。|
|字体位置|细绳|询问|如果需要，请指定自定义字体。|
|地区|细绳|询问|定义电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件需要密码。|

### **回复**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 为什么要使用将图表转换为 Csv API？

- 无需云存储，减少云资源负担。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将图表转换为 Csv API？

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv)概述了可公开访问的 API，可直接从 Web 浏览器实现 REST 交互。

## 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将范围数据转换为 csv 文件。
探索我们的 Aspose.Cells 云 SDK 的完整列表[GitHub 存储库](https://github.com/aspose-cells-cloud).

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
