---
title: "更新工作表属性 – Aspose.Cells Cloud API 参考 (v3.0)"
second_title: "文档"
linktitle: "更新"
type: docs
url: /zh/worksheets/update-properties/
aliases: [  /zh/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "工作表",
    "更新属性",
    "REST API",
    "云",
    "v3.0",
  ]
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 更新 Excel 工作表的基本属性（例如，显示零值、标尺可见性）。包含 cURL 请求示例、SDK 示例、参数说明及错误处理。"
ArticleTitle: "更新工作表属性 – Aspose.Cells Cloud API 参考 (v3.0)"
---

此 REST API 用于更新工作表的基本属性。

## REST API

**前提条件：** 您必须拥有有效的 Aspose Cloud 账户，获取 JWT 访问令牌，并确保目标工作簿存储在受支持的存储位置中。所有请求均需通过 **HTTPS** 发起。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **请求参数**

| 参数名称      | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| ------------- | ------ | --------------------------- | -------------------------------------------------------------------- |
| name          | string | path                        | 工作簿文件名（包含扩展名）。                                         |
| sheetName     | string | path                        | 要更新的工作表名称。                                                 |
| sheet         | object | body                        | JSON 对象，包含工作表属性键值对（例如 `DisplayZeros`、`IsRulerVisible`）。 |
| folder        | string | query                       | 工作簿所在存储中的文件夹路径。                                       |
| storageName   | string | query                       | 要使用的存储名称。                                                   |

**sheet** 对象以 JSON 格式发送至请求体中。可修改的属性示例包括 `DisplayZeros`、`IsRulerVisible`、`IsGridlinesVisible` 等，具体详见 API 规范。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

典型响应码：

- **200** – 成功。工作表属性已更新。
- **400** – 请求无效（例如 JSON 格式错误或缺少必需参数）。
- **401** – 未授权（缺少或无效的 JWT 令牌）。
- **404** – 工作簿或工作表未找到。
- **500** – 服务器内部错误。

| 状态码 | 含义 |
|--------|------|
| 200    | 成功 — 工作表属性已更新。 |
| 400    | 请求错误 — JSON 格式错误或缺少必需参数。 |
| 401    | 未授权 — 缺少或无效的 JWT 令牌。 |
| 404    | 未找到 — 工作簿或工作表不存在。 |
| 500    | 服务器内部错误。 |

## 云 SDK 开发工具包

使用 SDK 是加速开发的最快方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}