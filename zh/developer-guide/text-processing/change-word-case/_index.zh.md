---
title: "Aspose.Cells Cloud – 修改单词大小写（全大写、全小写、首字母大写、句首大写）"
ArticleTitle: "Excel 大小写转换器 – 全大写、全小写、首字母大写与句首大写"
linktype: "Word Case"
type: docs
url: /change-word-case/
keywords: "修改单词大小写 API、Aspose.Cells、Excel 大小写转换、全大写、全小写、首字母大写、句首大写、文本格式化"
description: "使用 Aspose.Cells Cloud API 轻松转换 Excel 文件中的文本大小写。支持全大写、全小写、首字母大写和句首大写。提供 C#、Java、Python 等多种语言的代码示例。"
weight: 100
---

## **修改单词大小写**

使用 Aspose.Cells Cloud Web API 可即时转换电子表格中的文本大小写——在选定区域中切换全大写、全小写、首字母大写（每个单词首字母大写）或句首大写（每句首字母大写）。仅影响字符串单元格；数字、布尔值、错误和空白单元格将被忽略。公式、格式和数据验证保持不变。

- **UpperCase（全大写）** – 所有字符均转换为大写。
- **LowerCase（全小写）** – 所有字符均转换为小写。
- **ProperCase（首字母大写）** – 每个单词的首字母大写，其余字母小写。
- **SentenceCase（句首大写）** – 每句话的首字母大写，其余字母小写。

<img src="images/result.png" alt="大小写转换前后截图" width="800" height="450" />

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```
### **UpdateWordCase** API 请求参数

| 参数名称         | 类型   | 位置     | 描述                                                                                                                                                     |
| :--------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet      | 文件   | FormData | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                             |
| wordCaseType     | 字符串 | Query    | 指定文本大小写转换类型：`UpperCase`（全大写）、`LowerCase`（全小写）、`ProperCase`（首字母大写）或 `SentenceCase`（句首大写）。                         |
| worksheet        | 字符串 | Query    | _（可选）_ 应用大小写转换的工作表名称。若省略，则操作应用于工作簿的第一个工作表。                                                                       |
| range            | 字符串 | Query    | _（可选）_ 应用大小写转换的单元格区域（例如 `"A1:C10"`）。若省略，则操作应用于指定工作表中所有已用单元格。                                              |
| outPath          | 字符串 | Query    | _（可选）_ 保存处理后工作簿的云存储文件夹路径。若省略，则文件保存在源文件所在文件夹中。                                                                 |
| outStorageName   | 字符串 | Query    | 输出文件将被存储到的云存储名称。                                                                                                                         |
| region           | 字符串 | Query    | _（可选）_ 设置文本大小写转换规则的区域设置，尤其适用于特定语言的大小写规则（例如 `"en-US"`、`"tr-TR"`）。                                              |
| password         | 字符串 | Query    | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                   |

### 响应

成功时，服务返回 **200 OK**（或 **202 Accepted**），响应体为 JSON 格式，包含已处理工作簿的二进制流。

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

### 错误码

- **400 Bad Request（错误请求）** – Aspose.Cells Cloud API URI 无效。
- **401 Unauthorized（未授权）** – 访问令牌无效或客户端凭据不正确。
- **404 Not Found（未找到）** – 电子表格文件无法访问。
- **500 Server Error（服务器错误）** – 电子表格处理过程中发生内部异常。

## 在哪些场景下应使用修改单词大小写 API？

### 数据清洗与标准化

- **客户数据管理** – 标准化客户姓名及地址信息的大小写格式（例如：`john doe` → `John Doe`）。
- **产品目录处理** – 标准化产品标题及描述文本（例如：`IPHONE 15 PRO` → `iPhone 15 Pro`）。
- **财务报表生成** – 规范财务报表中的项目名称与描述字段。

### 多源数据集成

- **数据仓库 ETL** – 从多个系统加载数据时统一文本格式。
- **API 数据接收** – 处理由外部 API 返回的大小写不一致的数据。
- **跨部门数据合并** – 统一不同部门 Excel 报告中的文本格式。

### 内容管理系统

- **自动化新闻稿** – 自动生成新闻标题及内容（标题大小写规则）。
- **产品文档生成** – 确保技术文档术语格式的一致性。
- **知识库维护** – 标准化常见问题（FAQ）与帮助文档的文本格式。

### 企业应用集成

- **CRM 系统集成** – 在客户数据导入/导出过程中自动格式化姓名与公司信息。
- **ERP 数据处理** – 规范物料描述、供应商名称等关键字段。
- **人力资源管理系统** – 标准化员工信息与职位名称。

### 批量文档处理

- **法律文档准备** – 批量处理合同与协议中的条款格式。
- **营销材料生成** – 统一广告文案与邮件模板的文本格式。
- **学术论文排版** – 规范参考文献与标题的格式要求。

### 实时数据处理

- **用户输入校验** – 实时格式化用户提交的表单数据。
- **聊天机器人响应** – 规范自动生成响应的文本格式。
- **即时报表生成** – 动态创建格式统一的业务报表。

### 国际化与本地化

- **多语言数据处理** – 处理不同语言文本的大小写规则差异。
- **本地化内容准备** – 为不同地区准备格式化后的本地内容。
- **翻译项目管理** – 确保翻译前后文本格式的一致性。

## 为何应使用修改单词大小写 API？

- **开发者友好** – Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发并配有详尽文档。相比自行构建解决方案，可显著降低开发工作量。
- **成本效益高** – 可直接在云端修改单词大小写，无需预先上传工作簿，从而节省存储空间并降低成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) 定义了公开可访问的编程接口，允许您直接从网页浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您仅需少量代码即可为单元格实现 **UpdateWordCase** 功能。请访问 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---