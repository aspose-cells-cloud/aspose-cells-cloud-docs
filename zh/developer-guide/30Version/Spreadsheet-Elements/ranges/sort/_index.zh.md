---
title: 范围排序
second_title: "文档"
linktype: "sort"
type: docs
keywords: "范围排序, Aspose.Cells Cloud, REST API, 电子表格, Excel, API"
url: /zh/ranges/sort/
description: 提供一种使用 Aspose.Cells Cloud 对工作簿内指定单元格范围进行排序的 API。
weight: 20
---

此 REST API 用于对指定的单元格范围进行排序。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort
```

请求参数如下：

| 参数名        | 类型   | 位置   | 描述                           |
|---------------|--------|--------|--------------------------------|
| name          | String | Path   | 工作簿名称。                   |
| sheetName     | String | Path   | 工作表名称。                   |
| rangeOperate  | Class  | Body   | 范围排序请求对象。             |
| folder        | String | Query  | 包含原始工作簿的文件夹。       |
| storageName   | String | Query  | 存储名称。                     |

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell
#（响应示例将在此处显示）
```

{{< /tab >}}
{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 GitHub 仓库，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}