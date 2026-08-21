---
title: "Aspose.Cells Cloud Excel 添加工作表 Web API — 使用类型与位置控制插入新工作表"
second_title: "文档"
ArticleTitle: "如何向 Excel 添加工作表 — 在指定位置插入新工作表"
linktitle: "向电子表格添加工作表"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, 添加工作表, aspose cells api, 电子表格, 云 api, 工作表类型, 工作表位置"
description: "了解如何使用 Aspose.Cells Cloud API 以编程方式向 Excel 工作簿添加新的工作表、图表工作表或宏工作表。通过单个 REST 调用控制工作表类型、名称及插入位置。"
weight: 100
---

使用完全可控的工作表类型与位置，以编程方式向 Excel 文件添加工作表。可在工作簿中任意位置插入标准工作表、图表工作表或宏工作表。此 RESTful 操作支持自动化 Excel 工作簿的管理与组织。

**前置条件**

- 拥有一个活跃的 Aspose.Cells Cloud 账户，并持有有效的 JWT 访问令牌。
- 已配置云存储名称（例如 `CompanyOneDrive`），用于保存工作簿。
- 目标工作簿必须位于指定存储中且可访问；若受密码保护，则需提供正确密码。

| **工作表类型**         | 描述                        |
| :--------------------- | :-------------------------- |
| **VB**                 | Visual Basic 模块           |
| **Worksheet**          | 标准工作表                  |
| **Chart**              | 图表工作表                  |
| **BIFF4Macro**         | BIFF4 宏工作表              |
| **InternationalMacro** | 国际化宏工作表              |
| **Other**              | 未列出的自定义或较罕见工作表类型 |
| **Dialog**             | 对话框工作表                |

## **向电子表格添加工作表 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称           | 类型    | 位置     | 描述                                                                                                                                                              |
| :----------------- | :------ | :------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File    | FormData | **必填。** 待添加新工作表的 Excel 工作簿文件（如 .xlsx、.xls 等）。                                                                                              |
| **sheetType**      | String  | Query    | **可选。** 要创建的工作表类型。可选值包括 `worksheet`（默认值）、`chartsheet`、`macrosheet`、`vbmodule` 和 `dialog`。                                            |
| **position**       | Integer | Query    | **可选。** 新工作表插入位置的从零开始索引。`0` 表示插入到第一张工作表之前；`2` 表示作为第三张工作表插入。省略该参数则将工作表追加至末尾。                         |
| **sheetName**      | String  | Query    | **可选。** 新工作表名称。必须在工作簿内唯一。若省略，则生成默认名称（如 “SheetX”）。                                                                             |
| **outPath**        | String  | Query    | **可选。** 修改后工作簿在云存储中的目标目录路径。若为 `null` 或省略，则保存至源文件所在位置或默认路径。                                                          |
| **outStorageName** | String  | Query    | **必填。** 已配置云存储的标识符（例如 `CompanyOneDrive`），用于指定输出文件的写入位置。                                                                         |
| **region**         | String  | Query    | **可选。** 区域设置（例如 `zh-CN`），可能影响新工作表的格式化及区域规则。                                                                                       |
| **password**       | String  | Query    | **可选。** 解密并修改受密码保护工作簿所需的密码。若文件未加密，请省略此项。                                                                                      |

### 响应

成功时，API 返回 **HTTP 200 OK**（若生成新文件则为 **201 Created**），并附带更新后的工作簿文件。

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
| :----- | :--------------- | :------------------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。     |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。             |

## 应在何处使用“向电子表格添加工作表” API？

- **自动化报告生成**：在财务报表生成过程中，动态创建并插入月度工作表（例如 `2024-05`）。
- **批量模板初始化**：在批量生成销售报价单或提案时，为每位新客户或项目添加专用分析工作表。
- **动态仪表板扩展**：随着新数据维度的出现，实时插入新的图表工作表。
- **合规与审计归档**：在年度审计期间自动添加证据收集工作表，确保各检查点相互隔离。

- 如需删除工作表，请参阅 **[删除工作表](/delete-worksheet/)** 操作。
- 如需移动工作表，请参阅 **[移动工作表](/move-worksheet/)** 操作。

## 为何应使用“向电子表格添加工作表” API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK，降低开发难度，并提供详尽的文档支持。
- **降低人工成本**：消除手动创建工作表及重复粘贴操作的需求。
- **按使用量计费**：仅对实际调用的 API 进行付费。
- **零维护成本**：无需管理服务器，无需软件更新，也无需担心兼容性问题。

## 如何使用 SDK 调用“向电子表格添加工作表” API

### “向电子表格添加工作表” API 规范

[“向电子表格添加工作表”API 规范](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可屏蔽底层细节，仅需少量代码即可添加工作表。SDK 完整列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示如何使用不同 SDK 调用该服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}