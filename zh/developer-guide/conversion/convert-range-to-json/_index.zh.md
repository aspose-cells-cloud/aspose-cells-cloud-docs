---
title: "Aspose.Cells Cloud Web API — 将本地 Excel 区域数据转换为 JSON 文件的免费在线工具"
second_title: "文档"
ArticleTitle: "如何将本地电子表格区域数据转换为 JSON 文件：分步指南"
linktype: "docs"
url: /zh/convert-range-to-json/
keywords: "区域转 JSON, Aspose.Cells Cloud, Excel 转 JSON, 电子表格转换, API"
description: "使用 Aspose.Cells Cloud API 将本地 Excel 电子表格中的特定区域转换为 JSON。"
weight: 100
---

使用 Cloud API 将本地 Excel 文件中的区域数据导出为 JSON 文件。

## **区域转 JSON API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名             | 类型   | 路径/查询字符串/HTTP 正文 | 描述                                                                 |
| ------------------ | ------ | ------------------------- | -------------------------------------------------------------------- |
| Spreadsheet        | 文件   | FormData                  | 上传电子表格文件。                                                   |
| worksheet          | 字符串 | 查询字符串                | 电子表格中工作表的名称。                                             |
| range              | 字符串 | 查询字符串                | 要转换的单元格区域，例如 A1:C10。                                    |
| outPath            | 字符串 | 查询字符串                | （可选）工作簿所在文件夹路径；默认为 null。                          |
| outStorageName     | 字符串 | 查询字符串                | 输出文件存储的名称。                                                 |
| fontsLocation      | 字符串 | 查询字符串                | 自定义字体的存储位置（用于家庭使用）。                               |
| region             | 字符串 | 查询字符串                | 电子表格区域设置。                                                   |
| password           | 字符串 | 查询字符串                | 打开电子表格文件所需的密码。                                         |

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

| 状态码 | 含义             | 描述                                         |
| ------ | ---------------- | -------------------------------------------- |
| 200    | 成功             | 成功应用筛选条件；响应包含操作详细信息。     |
| 400    | 请求错误         | 缺失或无效参数（例如不支持的文件类型）。     |
| 401    | 未授权           | JWT 令牌无效或缺失。                         |
| 413    | 请求实体过大     | 上传的文件超过大小限制。                     |
| 500    | 服务器内部错误   | 服务器发生意外错误。                         |

## **应在何处使用区域转 JSON API？**

- 实时仪表板：将实时 Excel 数据转换为 JSON，供 Chart.js 或 D3.js 等图表库使用。
- 电子表格即服务（Spreadsheet-as-a-Service）：将 Excel 区域作为 JSON 接口暴露给其他服务。
- Webhook 负载：将电子表格数据转换为 JSON，用于 Webhook 通知。
- 快速数据原型设计：快速将清洗后的 Excel 数据转换为 JSON，以便用于 Python 或 R 分析。
- 机器学习流水线：从业务维护的电子表格中预处理训练数据。
- 电商运营：通过 JSON 将产品目录或价格表同步到网站。
- 报告自动化：从财务模型中生成 JSON 数据源，实现自动化报告。
- 应用配置：在 Excel 中管理功能开关、设置或 A/B 测试参数 → 转换为 JSON。
- 多语言支持：将本地化电子表格转换为 JSON，供 i18n 库使用。
- 动态菜单/导航：将网站导航结构存储在 Excel 中，并以 JSON 形式部署。

_其他转换选项，请参阅 [区域转 CSV](/convert-range-to-csv/) 指南。_

## 为什么应使用区域转 JSON API？

- **SDK 支持**：Aspose.Cells Cloud 提供多种语言的库，显著减少自定义代码量。
- **降低存储成本**：无需先上传整个工作簿即可转换指定区域，节省存储空间。
- **兼容 Web 和移动应用**：JSON 是现代 JavaScript 框架（如 React、Vue 和 Angular）的原生数据格式。
- **广泛的语言支持**：几乎所有编程语言和数据库都支持 JSON。
- **结构化数据保留**
  - **智能结构识别**：自动将表格数据转换为正确的 JSON 数组或对象。
  - **标题映射**：使用第一行作为 JSON 键，生成清晰的对象结构。
  - **数据类型保留**：保留数字、日期和布尔类型，而非简单文本。

## 如何使用 SDK 调用区域转 JSON API？

### 区域转 JSON API 规范

[区域转 JSON API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式，因为它屏蔽了底层细节，让您能用简洁的代码将区域数据转换为 JSON 文件。  
请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}