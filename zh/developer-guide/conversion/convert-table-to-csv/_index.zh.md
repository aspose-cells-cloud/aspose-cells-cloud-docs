---
title: "Aspose.Cells Cloud Web API — 将工作表表格数据转换为 CSV 文件的免费在线工具"
second_title: "文档"
ArticleTitle: "如何将工作表表格数据转换为 CSV 文件：分步指南"
linktype: "convert-table-to-csv"
type: docs
url: /zh/convert-table-to-csv/
keywords: "Aspose.Cells Cloud、表格转 CSV、电子表格转换、Excel 转 CSV、API、REST、数据导出"
description: "借助 Aspose.Cells Cloud API 快速将 Excel 电子表格中的表格转换为 CSV 文件。"
weight: 100
---

使用 Cloud API 将本地 Excel 文件中的表格数据导出为 CSV 文件。

## **将表格转换为 CSV 的 API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 正文 | 描述                                                                                                                 |
|------------------|--------|---------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件   | FormData                  | 上传电子表格文件。                                                                                                   |
| worksheet        | 字符串 | 查询字符串                | 电子表格中工作表的名称。                                                                                             |
| tableName        | 字符串 | 查询字符串                | 待转换表格的名称。                                                                                                   |
| outPath          | 字符串 | 查询字符串                | （可选）工作簿存储所在的文件夹路径；默认为 null。                                                                   |
| outStorageName   | 字符串 | 查询字符串                | 输出文件所用存储的名称。                                                                                             |
| fontsLocation    | 字符串 | 查询字符串                | 自定义字体的路径。                                                                                                   |
| region           | 字符串 | 查询字符串                | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式、日期解析及区域特定行为。                     |
| password         | 字符串 | 查询字符串                | 打开电子表格文件所需的密码。                                                                                         |

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
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 成功应用筛选条件；响应包含操作详细信息。   |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                   |

## **应在何处使用将表格转换为 CSV 的 API？**

- **数据库迁移**：将 Excel 表格转换为 CSV 格式，以便批量导入 SQL 数据库（如 MySQL、PostgreSQL、SQL Server）。
- **数据仓库加载**：将基于 Excel 的报表表格转换为 CSV 格式，以加载至 Snowflake、Redshift 或 BigQuery。
- **批量 API 载荷**：将 Excel 表格数据转换为 CSV 格式，用于批量上传至 REST 服务。
- **服务间通信**：在微服务之间使用 CSV 作为轻量级数据交换格式。
- **机器学习数据准备**：将 Excel 中的特征表格转换为 CSV 格式，供 Python/R 的机器学习库使用。
- **统计分析**：将研究数据表格转换为 CSV 格式，以便导入 SPSS、SAS 或 Stata。
- **内容迁移**：通过 CSV 将结构化内容从 Excel 迁移至 CMS 系统。

## **为何应使用将表格转换为 CSV 的 API？**

- **开发友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，可快速开发，并配有详尽文档；相比构建自定义解决方案，显著减少开发工作量。
- **成本效益高**：无需先上传工作簿即可转换表格数据，从而节省存储空间并降低成本。
- **纯数据提取，不包含格式信息**。
- **CSV 几乎被所有系统支持**：
  - 数据库（所有主流关系型数据库管理系统）
  - 编程语言（所有语言均内置解析器）
  - 商业智能工具（Tableau、Power BI、Looker）
  - 电子表格软件（Excel、Google Sheets、LibreOffice）
  - 命令行工具（awk、sed、grep）

## **如何使用 SDK 调用将表格转换为 CSV 的 API？**

### 将表格转换为 CSV 的 API 规范

[将表格转换为 CSV 的 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) 提供了公开可访问的编程接口，允许直接从 Web 浏览器发起 REST 请求。
您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能以极少代码完成电子表格表格数据向 CSV 文件的转换。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}