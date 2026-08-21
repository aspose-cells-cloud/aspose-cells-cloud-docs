---
title: "删除 Excel 工作表中的一行"
second_title: "文档"
linktitle: "行"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "使用 DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} 端点，通过 Aspose.Cells Cloud REST API 从 Excel 工作表中删除指定行。包含 cURL 命令、SDK 示例及完整的参数参考。"
keywords: "Aspose.Cells, 删除行, Excel, API, REST, 云, SDK"
weight: 80
ArticleTitle: "删除 Excel 工作表中的一行 – Aspose.Cells Cloud API 指南"
---

此 REST API 用于从 Excel 工作表中删除一行。

**前置条件**  
- 有效的 JWT **Authorization**（授权）令牌。  
- 工作簿必须存储在受支持的 Aspose Cloud 存储中（默认存储或自定义存储）。  
- 目标文件夹（如已指定）必须存在于所选存储中。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **请求参数**

| 参数名称           | 类型    | 路径 / 查询参数 | 必需 | 描述                                                                 |
| ------------------ | ------- | --------------- | ---- | -------------------------------------------------------------------- |
| **name**           | string  | path            | 是   | 工作簿名称。                                                         |
| **sheetName**      | string  | path            | 是   | 工作表名称。                                                         |
| **rowIndex**       | integer | path            | 是   | 待删除行的从零开始的索引。                                           |
| **startrow**       | integer | query           | 否   | 待删除首行的索引（通常与 `rowIndex` 相同）。                         |
| **totalRows**      | integer | query           | 否   | 待删除的连续行数。                                                   |
| **updateReference**| boolean | query           | 否   | 若为 `true`（默认值），删除后将更新公式、命名区域及其他引用。       |
| **folder**         | string  | query           | 否   | 包含该工作簿的文件夹。                                               |
| **storageName**    | string  | query           | 否   | 存储服务的名称。                                                     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了一个完整且可执行的调用。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**可能的 HTTP 响应代码**

| 代码 | 含义           | 描述                                   |
|------|----------------|----------------------------------------|
| 200  | OK（成功）     | 行已成功删除。                         |
| 400  | Bad Request（错误请求） | 缺少或无效的参数（例如，`rowIndex` 非数字）。 |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 404  | Not Found（未找到）   | 指定的工作簿、工作表或行不存在。       |
| 500  | Internal Server Error（服务器内部错误） | 意外服务器错误；详情请参阅错误响应。   |

**错误响应示例**

```json
{
  "Code": 400,
  "Message": "提供的行索引无效。"
}
```

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加速开发的最理想方式。SDK 抽象了底层细节，让您能专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**相关操作**  
- [添加一行](/cells/rows/add/row/)  
- [删除多行](/cells/rows/delete/rows/)  
- [获取行详情](/cells/rows/get/row/)  
---