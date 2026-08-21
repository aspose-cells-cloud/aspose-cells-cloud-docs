---
title: "Aspose.Cells Cloud Web API——将电子表格翻译为目标语言"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud AI 翻译 API 翻译整个电子表格"
linktitle: "翻译电子表格"
type: docs
url: /translate-spreadsheet/
keywords: "Aspose.Cells Cloud、翻译电子表格 API、AI 翻译、电子表格翻译、targetLanguage、多工作表翻译、云电子表格处理、Aspose.Cells Cloud 翻译"
description: "使用 Aspose.Cells Cloud AI 翻译整个 Excel 工作簿。在将文本转换为任何支持的语言时，保留公式、图表和格式。了解端点、参数、SDK 示例、限制和错误处理。"
weight: 100
---

**TranslateSpreadsheet** 端点属于 **Translate Spreadsheet API**，它会读取工作簿中的每个文本元素，将内容发送至由人工智能驱动的翻译服务，并返回一个新的电子表格文件，其中所有文本数据均以指定的 **targetLanguage**（目标语言）呈现。该操作保持原始布局、单元格样式、公式以及**多工作表结构**不变，非常适合用于全球化报告、仪表板和数据驱动型文档。支持的文件格式包括 XLS、XLSX、XLSM、CSV 和 ODS。若语言代码无效、身份验证失败或翻译服务中断，系统将返回错误。

## **Translate Spreadsheet API（翻译电子表格 API）**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **请求参数：**

| 参数名称 | 类型   | 位置   | 必填/可选 | 描述                                                                                                                                                                                                 |
| :------- | :----- | :----- | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet（电子表格） | 文件   | 必填   | FormData  | 待翻译的 Excel 工作簿。可接受的扩展名：.xls、.xlsx、.xlsm、.csv、.ods。文件最大尺寸：50 MB。示例：`budget.xlsx`。                                                                                   |
| targetLanguage（目标语言） | 字符串 | 必填   | 查询参数  | 所需输出语言的 ISO 639-1 语言代码（例如："es" 表示西班牙语，"fr" 表示法语，"de" 表示德语）。必须为底层人工智能服务所支持的语言。                                                                     |
| region（区域） | 字符串 | 可选   | 查询参数  | 电子表格区域标识符，影响区域特定格式（如日期、数字和货币）。常见取值："US"、"EU"、"CN"。若省略，则使用工作簿的原始区域设置。                                                                       |
| password（密码） | 字符串 | 可选   | 查询参数  | 打开受保护工作簿所需的密码。若文件未设置密码，请留空。                                                                                                                                             |

### **响应**

成功响应（200 OK）  
响应头：  
Content-Type: application/octet-stream // 若请求 CSV 输出则为 text/csv  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <字节数>

响应体：  
<包含翻译后电子表格文件的二进制流>

错误响应遵循标准 Aspose.Cells Cloud 错误模型（application/json），包含字段 `code`（错误代码）、`message`（错误信息）及可选字段 `details`（详细信息）。

**HTTP 状态码**

| 代码 | 含义         | 描述                           |
| ---- | ------------ | ------------------------------ |
| 200  | OK（成功）   | 翻译操作成功；响应包含操作详情。 |
| 400  | Bad Request（请求错误） | 缺少或无效参数（例如：不支持的文件类型）。 |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。           |
| 413  | Payload Too Large（负载过大） | 上传文件超过大小限制。         |
| 500  | Internal Server Error（内部服务器错误） | 服务器发生意外错误。           |

## **应在哪里使用 Translate Spreadsheet API？**

- **国际财务报告**——将季度 Excel 报告转换为多种语言，供各地区办公室使用，同时保留公式和图表布局。
- **多语言营销仪表板**——自动为全球团队生成销售业绩仪表板的本地化版本。
- **教育内容分发**——将成绩册、作业表或课程电子表格翻译成不同国家学生所需的语言，无需手动复制粘贴。
- **合规性监管**——生成符合语言要求的合规性电子表格，保留验证规则和数据验证列表。

## **为何应使用 Translate Spreadsheet API？**

- **人工智能驱动的高准确度**——利用先进的神经网络翻译模型，实现上下文感知的高质量语言转换。
- **零布局破坏**——保持单元格公式、条件格式、图表及工作表顺序与源文件完全一致。
- **单次调用处理多工作表**——在一次请求中完成所有工作表的翻译，无需逐个工作表循环操作。
- **无缝云集成**——与 Aspose.Cells Cloud 身份验证兼容，便于在 CI/CD、无服务器函数或企业后端中构建自动化流程。

## **如何使用 SDK 调用 Translate Spreadsheet API**

### Translate Spreadsheet API 规范

[Translate Spreadsheet API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) 提供了公开可访问的编程接口，可直接从网页浏览器执行 REST 交互。

## Excel API SDK

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的途径，它抽象了底层细节，使您能用简短代码实现电子表格合并等操作。  
请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}