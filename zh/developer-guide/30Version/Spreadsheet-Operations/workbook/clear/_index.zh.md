---
title: "清除 Excel 文件中的对象"
second_title: "文档"
linktitle: "清除"
type: docs
url: /zh/clear/
aliases: [  /zh/clearobjects/ ]
keywords: "Aspose.Cells, Excel, 清除对象, REST API, 云 SDK, 删除注释, 删除图表"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作簿中删除注释、图表、形状及其他对象。支持多种 SDK，并以 Base64 格式返回已清理的文件。"
weight: 39
---

此 REST API 可清除 Excel 文件中的对象。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### 请求参数

| 参数名     | 类型   | 位置       | 是否必需 | 默认值 | 可选值                                                                                                                                                                                                 | 描述                                 |
| ---------- | ------ | ---------- | -------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------ |
| file       | 文件   | form‑data  | 是       | —      | —                                                                                                                                                                                                      | 要上传的 Excel 文件                  |
| objecttype | 字符串 | query      | 否       | —      | `duplicaterows`, `blankcolumns`, `blankrows`, `formula`, `content`, `style`, `chart`, `comment`, `picture`, `shape`, `listobject`, `hyperlink`, `oleobject`, `pivottable`, `validation`, `background` | 要清除的对象类型（以逗号分隔）       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostClearObjects) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 封装了底层细节，使您可以专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}