---
title: "在 Excel 工作表中计算公式"
second_title: "文档"
linktitle: "计算"
type: docs
url: /zh/worksheets/calculate-formula/
aliases: [  /zh/calculate-formula-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 公式计算, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 工作表中计算公式。支持多种 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、Swift），并提供即用型示例。"
weight: 20
ArticleTitle: "在 Excel 工作表中计算公式 – Aspose.Cells Cloud 文档"
---

此 REST API 可返回工作表中**公式的计算结果值**，可用于**直接在应用程序中求值 Excel 公式**。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                                     |
| ------------- | ------ | ------ | ---------------------------------------- |
| name          | string | path   | Excel 文件名。                           |
| sheetName     | string | path   | 包含待计算公式的工作表名称。             |
| formula       | string | query  | 待求值的公式（例如：`SUM(A5:A10)`）。    |
| folder        | string | query  | 文档所在文件夹路径。                     |
| storageName   | string | query  | 存储服务名称（如适用）。                 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) 定义了一个公开可访问的编程接口，您可直接通过 Web 浏览器执行 REST 交互。

### 身份验证

所有请求必须在 `Authorization` 请求头中包含有效的 **Bearer JWT 令牌**：

```
Authorization: Bearer <your_jwt_token>
```

您可参考 Aspose.Cells Cloud 身份验证指南中描述的 OAuth 2.0 流程获取令牌。

### 可能的响应状态码

| 状态码 | 描述                                           |
|--------|------------------------------------------------|
| 200    | 请求成功；返回公式计算结果值。                 |
| 400    | 错误请求 — 缺少或参数无效。                    |
| 401    | 未授权 — 无效或缺少 JWT 令牌。                 |
| 404    | 未找到 — 指定的文件或工作表不存在。            |
| 500    | 服务器内部错误 — 服务器上发生意外情况。        |

您可使用 **cURL** 命令行工具轻松调用 Aspose.Cells Cloud Web 服务。以下示例展示了如何使用 cURL 请求公式计算结果。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是集成 API 的最快方式。SDK 负责处理底层细节，让您专注于业务逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**另请参阅：**  
- [获取工作表](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [更新工作表](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [计算所有公式](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---