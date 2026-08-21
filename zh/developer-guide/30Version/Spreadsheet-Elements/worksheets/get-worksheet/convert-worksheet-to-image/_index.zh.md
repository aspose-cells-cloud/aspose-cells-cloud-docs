---
title: "将工作表转换为 PDF、PNG、CSV 等格式 — Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "转换工作表"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, 工作表转换, REST API, cURL, SDK, PDF, PNG, CSV"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 工作簿中的单个工作表转换为 PDF、PNG、CSV 以及超过 15 种其他格式。包含 cURL 示例、SDK 代码片段及完整的参数参考。"
weight: 130
ArticleTitle: "将工作表转换为 PDF、PNG、CSV 等格式 — Aspose.Cells Cloud API"
---

**工作表转换 API** – `GET /cells/{name}/worksheets/{sheetName}` 端点用于将 Excel 工作簿中的单个工作表（即工作表）转换为其他文件格式。

> **前置条件：** 调用此端点前，您必须已获取有效的 JWT 令牌，并将工作簿存储在支持的 Aspose Cloud 存储位置中。

支持的**可导入**格式（工作表可从中读取）：

- XLS、XLSX、XLSB、CSV、TSV、XLSM、ODS、TXT

支持的**仅导出**格式（工作表可保存为）：

- PDF、OTS、XPS、DIF、PNG、JPEG、BMP、SVG、TIFF、EMF、NUMBERS、FODS

## REST API

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) 描述了公开可用的接口。

### **请求参数**

| 参数名                   | 类型    | 必填 | 默认值 | 允许值                                                         | 描述                             |
| ------------------------ | ------- | ---- | ------ | -------------------------------------------------------------- | -------------------------------- |
| **format**               | string  | 是   | –      | pdf、png、jpeg、bmp、svg、tiff、emf、csv、txt、…（见支持列表） | 目标输出格式。                   |
| **verticalResolution**   | integer | 否   | 96     | 72–600                                                         | 图像输出的垂直 DPI。             |
| **horizontalResolution** | integer | 否   | 96     | 72–600                                                         | 图像输出的水平 DPI。             |
| **password**             | string  | 否   | –      | –                                                              | 用于打开受密码保护的工作簿的密码。 |
| **folder**               | string  | 否   | –      | –                                                              | 存放源工作簿的云文件夹。         |
| **storage**              | string  | 否   | –      | –                                                              | 存储名称（例如 “Default”）。     |

### 响应

| 状态码 | 描述                                   | 返回类型                   |
| ------ | -------------------------------------- | -------------------------- |
| **200** | 转换成功；返回转换后文件的二进制流。    | `application/octet-stream` |
| **400** | 请求错误 — 缺少或无效的参数。          | JSON 错误对象              |
| **401** | 未授权 — 无效或缺失 JWT 令牌。         | JSON 错误对象              |
| **404** | 未找到 — 工作簿或工作表不存在。        | JSON 错误对象              |
| **500** | 服务器内部错误 — 意外失败。            | JSON 错误对象              |

#### 示例请求（cURL）

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 示例响应

```
已转换的图像（二进制流）
```

## 云 SDK 家族

使用 SDK 是开发速度最快的方式。SDK 处理底层细节，使您能专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 云服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}