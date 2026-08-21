---
title: "Aspose.Cells Cloud API – 合并单元格区域"
second_title: "文档"
linktitle: "合并"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, 合并单元格, Excel API, REST, 云 SDK"
description: "使用 Aspose.Cells Cloud REST API 将单元格区域合并为单个单元格。了解请求格式、参数以及 C#、Java、Python 等语言的 SDK 示例。"
weight: 20
---

此 REST API 可将 Excel 工作表中的单元格区域合并为单个单元格。

**概述**：合并区域会将所选单元格合并为一个单元格，保留左上角单元格的值，并丢弃其余单元格。当您需要创建跨多列或多行的标题，或希望简化工作表布局时，可使用此操作。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **请求参数**

| 参数名称       | 类型   | 位置 | 描述                                   |
| -------------- | ------ | ---- | -------------------------------------- |
| **name**       | string | path | 工作簿名称。                           |
| **sheetName**  | string | path | 工作表名称。                           |
| **range**      | object | body | 指定待合并单元格的区域对象。           |
| **folder**     | string | query| 存储工作簿的文件夹。                   |
| **storageName**| string | query| 存储名称。                             |

#### 请求体架构

**Range** 对象必须包含以下字段（其余字段均为可选）：

| 属性          | 类型    | 必需 | 描述                                   |
| ------------- | ------- | ---- | -------------------------------------- |
| **FirstRow**  | integer | 是   | 区域中首行的从零开始的索引。           |
| **FirstColumn**| integer | 是   | 区域中首列的从零开始的索引。           |
| **RowCount**  | integer | 是   | 区域中包含的行数。                     |
| **ColumnCount**| integer | 是   | 区域中包含的列数。                     |
| **Name**      | string  | 否   | 区域的可选名称。                       |
| **RefersTo**  | string  | 否   | 区域所引用的公式。                     |
| **Worksheet** | string  | 否   | 工作表名称（若与路径参数不同）。       |
| **RowHeight** | number  | 否   | 区域内行高（像素）。                   |
| **ColumnWidth**| number | 否   | 区域内列宽（像素）。                   |

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### 响应详情

| HTTP 状态码                   | 描述                                           | 示例 JSON                                              |
| ----------------------------- | ---------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | 区域已成功合并。                               | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | 区域参数无效（例如索引越界）。                 | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | 缺少或无效的 JWT 令牌。                        | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | 工作簿或工作表未找到。                         | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | 服务器内部错误。                               | `{ "Code": 500, "Message": "Internal server error." }` |

## 云 SDK 开发工具包

使用 SDK 是加速开发的最佳方式。SDK 可处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}