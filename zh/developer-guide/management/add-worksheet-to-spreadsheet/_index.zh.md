---
title: Aspose.Cells Cloud Webb API - 将工作表添加到电子表格
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: 将工作表添加到电子表格
type: docs
url: /zh/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Aspose.Cells Cloud Web API 允许开发人员高效地将新工作表添加到工作簿，并控制工作表的类型、位置和名称。此功能增强了工作簿的管理和灵活性
weight: 100
kwords: Excel, Office 云、REST、电子表格、PDF、CSV、JSON、Markdown、管理 Excel 工作表、动态电子表格创建
---
向电子表格中添加工作表，指定工作表的类型和位置。

|**工作表类型** |描述|
|:- |:- |
|**VB** | Visual Basic 模块|
|**工作表** |工作表|
|**图表** |图表表|
|**BIFF4宏** |BIFF4 宏表|
|**国际宏观** |国际宏观表|
|**其他** |国际宏观表|
|**对话** |对话工作表|

## **将工作表添加到电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|sheetType|细绳|询问|指定新工作表的名称。如果未提供，则将分配默认名称。|
|位置|整数|询问|指定新工作表的插入位置。如果未提供，则工作表将添加到工作簿的末尾。|
|工作表名称|细绳|询问|指定要添加的工作表类型。如果未提供，则将使用默认工作表类型。|
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

## 我们应该在哪里使用“将工作表添加到电子表格 API”？

当您需要为电子表格添加工作表时，可以使用这个API。

## 为什么要使用“将工作表添加到电子表格 API”？

- 向电子表格中添加工作表，指定工作表的类型和位置。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将工作表添加到电子表格 API

### 将工作表添加到电子表格 API 规范

这[将工作表添加到电子表格 API 规范](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将工作表添加到电子表格中。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 对 Aspose.Cells Web 服务进行 API 调用：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
