---
title: Aspose.Cells Cloud Web API - 将工作表移动到电子表格中的新位置
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: 在电子表格中移动工作表
type: docs
url: /zh/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API 使用户能够有效地重新定位工作簿中的指定工作表，从而增强电子表格数据的组织性和可访问性
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, 移动工作表, 工作簿组织, PDF, CSV, JSON, Markdown
---
将工作表移动到电子表格中的新位置。

## **从电子表格 API 移动工作表**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|工作表|细绳|询问|要移动的工作表的当前名称。|
|位置|整数|询问|工作表的新位置。|
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

## 我们应该在哪里使用电子表格 API 中的移动工作表？

当您需要将工作表移动到电子表格中的新位置时，您可以使用此 API。

## 为什么要使用电子表格 API 中的移动工作表？

- 快速从电子表格中移动工作表。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDKs 在电子表格 API 中使用移动工作表

### 在电子表格中移动工作表 API 规范

这[在电子表格中移动工作表 API 规范](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet)提供一个可公开访问的编程接口，以方便从 Web 浏览器进行直接 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码在电子表格中移动工作表。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
