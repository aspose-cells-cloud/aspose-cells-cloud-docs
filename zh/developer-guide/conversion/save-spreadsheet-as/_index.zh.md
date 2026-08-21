---
title: "将电子表格另存为其他格式 – Aspose.Cells Cloud API（v4.0）"
second_title: "文档"
ArticleTitle: "如何在远程存储中将电子表格另存为其他格式文件：分步指南"
linktitle: "将电子表格另存为"
type: docs
url: /save-spreadsheet-as/
keywords: "Aspose Cells, 电子表格转换, 另存为, API, XLSX 转 PDF, 云存储, Excel 转 PDF, CSV 导出, 云转换"
description: "了解如何使用 Aspose.Cells Cloud 的“将电子表格另存为”API，将存储在 Aspose Cloud 中的电子表格转换为其他格式（XLSX、PDF、CSV 等）。包含请求语法、参数说明、curl 示例及 SDK 代码。"
weight: 100
---

将云中的电子表格或 Excel 文件保存为云存储中的其他格式。

## **将电子表格另存为 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称         | 类型   | 位置   | 描述                                                                                     |
| :--------------- | :----- | :----- | :--------------------------------------------------------------------------------------- |
| name             | String | Path   | **必填。** 需要转换的工作簿文件名。                                                       |
| format           | String | Query  | **必填。** 目标输出格式（例如 `Xlsx`、`PDF`、`CSV`）。                                    |
| saveOptionsData  | Class  | Body   | 可选的保存选项数据；若省略，则默认为 `null`。                                             |
| folder           | String | Query  | 可选；源工作簿所在的文件夹路径；若省略，则默认为 `null`。                                 |
| storageName      | String | Query  | 可选；自定义存储空间的名称；若省略，则使用默认存储空间。                                  |
| outPath          | String | Query  | 可选；转换后文件的输出路径；若省略，则默认为 `null`。                                     |
| outStorageName   | String | Query  | 可选；输出文件所用的存储空间名称。                                                        |
| fontsLocation    | String | Query  | 可选；自定义字体路径。                                                                    |
| region           | String | Query  | 可选；电子表格区域设置。                                                                  |
| password         | String | Query  | 可选；打开电子表格文件所需的密码。                                                        |

**支持的输出格式**

| 格式   | 扩展名                                           |
| :----- | :----------------------------------------------- |
| Xlsx   | .xlsx                                            |
| Pdf    | .pdf                                             |
| Csv    | .csv                                             |
| Html   | .html                                            |
| Ods    | .ods                                             |
| Xls    | .xls                                             |
| Txt    | .txt                                             |
| Mhtml  | .mhtml                                           |
| Tiff   | .tiff                                            |
| Pptx   | .pptx                                            |
| …（更多） | 请参阅 API 规范获取完整列表（共 20 多种格式） |

### **响应示例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**错误响应示例（400 Bad Request）**

```json
{
  "Code": 400,
  "Message": "Invalid request parameters."
}
```

**HTTP 状态码说明**

| 状态码 | 含义               | 描述                                       |
| :----- | :----------------- | :----------------------------------------- |
| 200    | OK（成功）         | 过滤器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                   |

## 应在何处使用“将电子表格另存为”API？

### 企业文档管理系统

- 自动将财务报表保存为 PDF 归档文件。
- 定期将销售数据备份为 CSV 格式。
- 将项目计划保存为只读文件以防止意外修改。

### 数据集成与 ETL 流程

- 导出 CRM 系统数据并保存为标准 Excel 模板。
- 将 ERP 数据转换为 CSV 格式以便导入其他系统。
- 将原始数据保存为 JSON 格式以供 API 传输使用。

### 开发与自动化场景

- Web 应用程序的后端处理。
- 自动化报表生成系统。
- 云协作平台。
- 审批流程集成。
- 数据备份与迁移。

## 为何应使用“将电子表格另存为”API？

- **开发者友好**：提供多种编程语言的 SDK 及详细文档，简化集成过程。
- **高效省力**：服务端完成格式转换，无需编写自定义转换代码。
- **按使用量计费**：仅对实际调用的 API 请求收费，无前期授权费用。
- **免服务器维护**：服务运行于云端，无需自行管理转换基础设施。
- **格式支持广泛**：支持超过 20 种电子表格格式之间的相互转换。
- **数据保真度高**：转换过程中保留布局、公式和样式。

## 如何结合 SDK 使用“将电子表格另存为”API？

### “将电子表格另存为”API 规范

[将电子表格另存为 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST API 调用。

**带请求体和 cURL 的示例**

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您仅需少量代码即可完成电子表格格式转换。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}