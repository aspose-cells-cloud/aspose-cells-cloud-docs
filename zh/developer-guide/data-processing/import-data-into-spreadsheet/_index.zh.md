---
title: Aspose.Cells Cloud Web API - 将 Csv、JSON 或 XML 数据导入电子表格文件
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: 将数据导入电子表格
type: docs
url: /zh/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: 使用 Aspose.Cells Cloud Web API 将数据从 CSV、JSON 和 XML 等受支持的格式高效导入电子表格
weight: 100
kwords: Aspose.Cells 云 Web API，导入数据，Office 云，REST，电子表格，CSV，JSON，XM
---
将数据导入电子表格工作表。导入的数据文件支持以下格式：[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/)或者[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **将数据导入电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|数据文件|文件|表单数据|上传需要导入的数据文件。|
|电子表格|文件|表单数据|上传目标电子表格文件。|
|工作表|细绳|询问|指定导入数据的工作表。|
|启动细胞|细绳|询问|指定导入数据的起始位置。|
|插入|布尔值|询问|指示是否插入或覆盖指定的导入数据。|
|转换数字数据|布尔值|询问|指定导入时是否转换数值数据。|
|分离器|细绳|询问|指定 CSV 格式的分隔符。|
|输出路径|细绳|询问| （可选）存储工作簿的文件夹路径。默认值为 null。|
|输出存储名称|细绳|询问|指定输出文件存储名称。|
|字体位置|细绳|询问|定义要使用的自定义字体。|
|雷戈因|细绳|询问|设置电子表格区域配置。|
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

## 我们应该在哪里使用“将数据导入电子表格 API”？

- 将大量数据导入电子表格工作表。
- 导入的数据文件格式为[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/)和[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## 为什么要使用“将数据导入电子表格 API”？

- 将大量数据导入电子表格。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将数据导入电子表格 API

### 将数据导入电子表格 API 规范

这[将数据导入电子表格 API 规范](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet)提供一个可公开访问的编程接口，允许直接从您的 Web 浏览器进行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将数据导入电子表格工作表。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
