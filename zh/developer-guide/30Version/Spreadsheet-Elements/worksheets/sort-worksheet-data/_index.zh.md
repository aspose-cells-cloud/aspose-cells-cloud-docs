---
title: "对 Excel 工作表中的范围数据进行排序"
second_title: "文档"
linktitle: "排序"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, Excel 排序 API, 工作表范围排序, REST API, dataSorter"
description: "使用 Aspose.Cells Cloud REST API 对 Excel 工作表中的特定范围进行排序。包含端点、必需参数、身份验证步骤、错误处理及 SDK 示例。"
weight: 20
---

REST API 可对 Excel 工作表中指定范围内的数据进行排序。

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### 请求参数

| 参数名称       | 类型   | 位置   | 必填 | 描述                                               |
| -------------- | ------ | ------ | ---- | -------------------------------------------------- |
| name           | string | 路径   | 是   | 工作簿名称。                                       |
| sheetName      | string | 路径   | 是   | 工作表名称。                                       |
| cellArea       | string | 查询   | 是   | 要排序的单元格范围（例如 `A5:A10`）。              |
| dataSorter     | object | 请求体 | 是   | 定义排序设置的 JSON 对象（见下方架构）。           |
| folder         | string | 查询   | 否   | 包含该工作簿的文件夹。                             |
| storageName    | string | 查询   | 否   | 工作簿所在的存储名称。                             |

**`dataSorter` 对象架构** —— 请求体必须包含一个具有以下属性的 JSON 对象：

- `CaseSensitive` _(布尔值，必需)_ —— 指定排序是否区分大小写。
- `HasHeaders` _(布尔值，必需)_ —— 指定该范围是否包含标题行。
- `KeyList` _(数组，必需)_ —— 排序键的集合。每个键对象包括：
  - `Key` _(整数)_ —— 从零开始的列索引。
  - `SortOrder` _(字符串)_ —— `"ascending"`（升序）或 `"descending"`（降序）。
- `SortLeftToRight` _(布尔值，必需)_ —— 若为 `true`，则按从左到右的方式排序；否则按从上到下排序。
- 其他可选字段（如 `CaseOrder`、`SortLeftToRight` 等）可依据 OpenAPI 规范提供。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**错误处理** —— API 可返回标准 HTTP 错误码。常见响应包括：

| HTTP 状态码 | 代码 | 消息                                           |
| ----------- | ---- | ---------------------------------------------- |
| 400         | 400  | 请求错误 —— 缺少或无效的参数。                 |
| 401         | 401  | 未授权 —— JWT 令牌无效或缺失。                 |
| 404         | 404  | 未找到 —— 工作簿或工作表不存在。               |
| 500         | 500  | 服务器内部错误。                               |

错误情况下，响应体遵循格式：`{ "Code": <状态码>, "Message": "<描述>", "Status": "Error" }`。

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 负责处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}