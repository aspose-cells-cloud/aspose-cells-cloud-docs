---
title: "导出表格 – Aspose.Cells Cloud API | 将 Excel 转换为 PDF、PNG、CSV"
second_title: "文档"
ArticleTitle: "如何将远程电子表格表格导出为其他格式：分步指南"
linktype: "导出表格为指定格式"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, 导出表格, Excel 转 PDF, 云 API, REST"
description: "使用 Aspose.Cells Cloud API 将远程 Excel 表格导出为 PDF、PNG、CSV、JSON 或其他格式。通过安全的 HTTPS 端点及 JWT 身份验证，并提供 SDK 示例。"
weight: 100
---

导出存储于云端的电子表格（Excel）表格为其他格式的文件。

## **导出表格为指定格式 API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名             | 类型   | 路径/查询字符串/HTTPBody | 说明                                                                                                                                           |
| :----------------- | :----- | :----------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| name               | String | Path                     | **必填。** 待获取的工作簿文件名。                                                                                                              |
| worksheet          | String | Path                     | 工作表名称。                                                                                                                                   |
| tableName          | String | Path                     | 表格名称。                                                                                                                                     |
| format             | String | Query                    | **必填。** 目标输出格式（例如：“png”、“pdf”、“svg”）。                                                                                        |
| folder             | String | Query                    | 可选。工作簿所在文件夹路径；默认为 `null`。                                                                                                    |
| storageName        | String | Query                    | 可选。使用自定义云存储时指定存储名称；省略时使用默认存储。                                                                                    |
| outPath            | String | Query                    | 可选。输出文件所在文件夹路径；默认为 `null`。                                                                                                  |
| outStorageName     | String | Query                    | 可选。输出文件存储的名称。                                                                                                                     |
| fontsLocation      | String | Query                    | 可选。自定义字体所在路径。                                                                                                                     |
| region             | String | Query                    | 可选。电子表格区域/语言设置（例如：`zh-CN`、`fr-FR`），影响数字格式、日期解析及区域性相关行为。                                                |
| password           | String | Query                    | 可选。打开电子表格文件所需的密码。                                                                                                             |

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

| 状态码 | 含义             | 说明                                       |
| ------ | ---------------- | ------------------------------------------ |
| 200    | OK（成功）       | 过滤操作成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 服务器内部意外错误。                   |

## **在哪些场景下应使用导出表格为其他格式 API？**

- **遗留系统迁移**：将成千上万份旧版 XLS 文件转换为 XLSX，适配现代系统。
- **归档标准化**：将多种电子表格格式（XLS、XLSM、ODS、CSV）统一转换为单一格式用于归档。
- **办公套件互操作性**：将 Excel 文件转换为 LibreOffice、Google Sheets 或 Apple Numbers 兼容格式。
- **数据源标准化**：将各类电子表格格式转换为 CSV 或 JSON，以便导入数据库。
- **网页发布**：将财务模型转换为 HTML 以供网页展示。

## **为何应使用导出表格为其他格式 API？**

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发，并配有详尽文档；相较于自行构建图表渲染解决方案，可大幅减少开发工作量。
- **降低人工成本**：减少对专职文档整合岗位的需求。
- **按需付费**：无需前期投入；仅对实际调用的 API 接口计费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。
- **API 仅返回原始表格数据，不含工作簿样式信息。**

## **如何使用 SDK 调用导出电子表格表格为指定格式 API？**

### 导出表格为指定格式 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">导出表格为指定格式 API 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

使用 SDK 是开发速度最快的方式，因其屏蔽了底层细节，您只需少量代码即可完成将电子表格表格导出为指定格式文件的操作。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}