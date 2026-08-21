---
title: "获取 Excel 工作表的页数"
second_title: "文档"
linktitle: "页数"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel API, 工作表页数, REST, 云 SDK, Excel 分页"
description: "使用 Aspose.Cells Cloud REST API (v3.0) 获取 Excel 工作表中的可打印页数。包含 HTTPS 请求格式、认证步骤、示例 cURL 命令、完整的 JSON 响应、状态码以及 SDK 代码示例。"
weight: 10
ArticleTitle: "获取 Excel 工作表的页数 – Aspose.Cells Cloud API"
---

此 REST API 返回工作表的**页数**。

**认证说明：** 所有 Aspose.Cells Cloud 接口均需通过 OAuth2 流程获取的 Bearer 令牌进行身份验证。请按下方 cURL 示例所示，将该令牌包含在 `Authorization` 请求头中。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### 请求参数

| 参数名称     | 类型   | 位置   | 描述                     |
| ----------- | ------ | ------ | ------------------------ |
| name        | string | path   | 文档名称。               |
| sheetName   | string | path   | 工作表名称。             |
| folder      | string | query  | 包含该文档的文件夹。     |
| storageName | string | query  | 存储空间名称。           |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 调用。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### 响应详情

| HTTP 状态码 | 含义                                               |
| ----------- | -------------------------------------------------- |
| **200**     | 成功 – 返回上述 JSON 负载。                        |
| **401**     | 未授权 – 缺少或令牌无效。                          |
| **404**     | 未找到 – 文件或工作表不存在。                      |
| **500**     | 服务器内部错误 – 出现意外的服务器问题。            |

### 版本历史

_API 版本 **v3.0**（发布于 2025 年）。若您使用的是更高版本，请参考更新后的接口文档。_

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 将底层细节封装起来，使您能专注于业务逻辑。您可在 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 注意事项

- 页数反映的是可打印布局，考虑了分页符、页边距和缩放设置。隐藏的行或列可能影响最终结果。
- 在发起请求前，请确保目标工作表存在，且文件已存储在指定的 `folder` 和 `storageName` 中。