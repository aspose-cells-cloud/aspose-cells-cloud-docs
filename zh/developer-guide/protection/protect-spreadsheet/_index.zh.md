---
title: Aspose.Cells 云网 API - 保护电子表格
second_title: Developer Guide for Excel Protectio
ArticleTitle: Protect the Spreadsheet with passwor
linktitle: 保护电子表格
type: docs
url: /zh/protect-spreadsheet/
keywords: Aspose.Cells Cloud Web API, password protection, encrypt spreadsheet, modify passwor
description: 此 API 对 Excel 电子表格应用双层密码保护，通过加密确保安全访问和修改
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, JSON, Markdown, 双层密码保护, 加密电子表格, 安全 Exce
---
对Excel电子表格应用密码保护，支持打开和修改密码。

## **保护电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传要保护的电子表格文件。|
|密码|细绳|询问|电子表格文件的加密密码。|
|修改密码|细绳|询问|修改电子表格需要密码。|
|输出路径|细绳|询问|（可选）受保护工作簿的存储文件夹路径。默认值为 null。|
|输出存储名称|细绳|询问|输出文件的存储名称。|
|地区|细绳|询问|定义电子表格的区域设置。|

## **回复**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用保护电子表格 API？

当您需要用密码锁定电子表格时，您可以使用这个 API。

## 为什么要使用保护电子表格 API？

- 使用密码快速锁定电子表格。
- 通过现有的SDK即可快速完成开发。

## 如何将 Protect Spreadsheet API 与 SDK 结合使用

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet)提供了详细的编程接口，用于直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现单元格的电子表格保护。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 与 Aspose.Cells Web 服务进行交互：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
