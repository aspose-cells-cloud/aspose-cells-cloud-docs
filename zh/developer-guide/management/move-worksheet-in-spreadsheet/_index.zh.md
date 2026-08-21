---
title: "Aspose.Cells Cloud Excel：移动工作表 Web API —— 编程方式更改工作表位置"
second_title: "文档"
ArticleTitle: "如何在 Excel 中移动工作表 —— 重新排列工作表顺序与位置"
linktitle: "在电子表格中移动工作表"
type: docs
url: /move-worksheet-in-spreadsheet/
keywords: "移动工作表 API，重新排列工作表 API，更改工作表顺序 API，Excel 标签管理 API，Aspose Cells REST API，自动化工作表定位，工作簿组织 API，电子表格结构 API，云端 Excel 自动化，批量工作表重排"
description: "了解如何在 Excel 工作簿内移动工作表，以重新组织工作表顺序并优化工作簿结构。更改工作表位置、重新排列标签以提升工作流程，并自动化工作表组织，实现专业级电子表格管理。"
weight: 100
---

通过 Aspose.Cells Cloud API 编程方式移动 Excel 工作簿中的工作表。通过 RESTful API 调用，变更工作表位置、重新排列工作表标签，并优化工作簿结构。适用于自动化电子表格组织及创建标准化工作簿布局。

## **电子表格中移动工作表 API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称         | 类型     | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                               |
| :--------------- | :------- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件     | FormData                    | **必填**。包含待重新定位工作表的源 Excel 工作簿文件（如 `.xlsx`、`.xls` 等）。                                                                  |
| worksheet        | 字符串   | 查询字符串                  | **必填**。待移动工作表的精确名称（例如 `Summary`、`RawData_2024`）。                                                                             |
| position         | 整数     | 查询字符串                  | **必填**。工作表的新零基索引位置。例如 `0` 表示移至首位，`2` 表示移至第三位。                                                                   |
| outPath          | 字符串   | 查询字符串                  | **可选**。云存储中用于保存重排后工作簿的目标文件夹路径。若为 `null` 或省略，则默认保存至源文件所在目录。                                         |
| outStorageName   | 字符串   | 查询字符串                  | **必填**。已配置的云存储服务的名称标识符（例如 `TeamDrive`），用于指定输出文件的存储位置。                                                       |
| region           | 字符串   | 查询字符串                  | **可选**。需应用的区域设置（例如 `zh-CN`），可能影响保存操作期间的某些格式规则。                                                                 |
| password         | 字符串   | 查询字符串                  | **可选**。打开并修改受密码保护的工作簿所需的解密密码。若文件未加密，可省略此项。                                                                 |

### **响应**

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

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
| ------ | ---------------- | ------------------------------------------ |
| 200    | OK（成功）       | 操作成功执行；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                 |

## 应在何处使用“电子表格中移动工作表” API？

- **标准化报告生成**：每月或每季度报告自动生成后，将 `Summary`（摘要）或 `Executive Overview`（执行摘要）工作表移至工作簿顶部，确保打开文件时首先呈现核心结论。
- **数据处理流水线**：在 ETL 流程中处理来自不同数据源的原始工作表后，将已清洗与转换的 `Processed_Data`（已处理数据）工作表移至工作簿中的逻辑位置（例如中间位置），形成清晰的流程结构（原始数据、分析结果分层排列）。
- **用户自定义文件交付**：用户通过配置界面（例如，将图表页置于顶部）选择偏好布局后，系统自动按其选择重排工作簿中的工作表顺序，并交付个性化文件。

## 为何应使用“电子表格中移动工作表” API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并附带详尽文档。相较自行构建解决方案，可显著减少开发工作量。
- **降低人工成本**：减少专门用于文档整合的人力投入。
- **按需付费**：无需前期投入；仅对实际使用的 API 调用计费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。

## 如何通过 SDK 使用“电子表格中移动工作表” API

### 移动工作表 API 规范

[电子表格中移动工作表 API 规范](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) 提供公开可访问的编程接口，便于直接通过 Web 浏览器进行 REST 交互。

可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[]（Base64 编码）",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您能以简洁代码移动电子表格中的工作表。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}