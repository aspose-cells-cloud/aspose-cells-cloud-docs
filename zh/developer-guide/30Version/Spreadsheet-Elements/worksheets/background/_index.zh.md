---
title: "使用 Aspose.Cells Cloud API 添加或删除工作表背景图片"
second_title: "文档"
linktitle: "背景"
type: docs
url: /zh/worksheets/background/
keywords: "Aspose.Cells Cloud, 工作表背景, Excel API, 添加背景图片, 删除工作表背景, SDK 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表添加或移除背景图片。包含请求语法、Java、.NET、Python、PHP 的 SDK 示例以及错误处理方法。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 添加或删除工作表背景图片"
---

## 在 Excel 工作表中处理背景

**概述：** 工作表背景是显示在工作表单元格后方的图片，常用于品牌标识或视觉提示。Aspose.Cells Cloud API 可让您以编程方式添加或删除该背景图片。

**前置条件：**  
- 有效的 Aspose.Cells Cloud 访问令牌（OAuth 2.0）。  
- 已存储在云端的 Excel 工作簿。  
- 用于背景的图片文件（PNG、JPEG、BMP 格式）。

- **添加背景** —— 为工作表设置背景图片。详见详细指南 [如何为 Excel 工作表设置背景](/cells/worksheets/background/add/)。  
- **删除背景** —— 从工作表中移除已存在的背景图片。详见详细指南 [如何删除 Excel 工作表背景](/cells/worksheets/background/delete/)。

使用工作表背景有助于增强品牌识别度、突出重要区域，或为终端用户提供视觉提示。Aspose.Cells Cloud API 可让您的应用程序轻松完成该背景图片的设置或清除操作。

### API 参考

| 操作 | HTTP 方法 | 端点 | 路径参数 | 请求体 | 成功响应 |
|------|-----------|------|----------|--------|----------|
| 添加背景 | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` —— 工作簿文件名<br>`sheetName` —— 目标工作表名称 | 图片文件（PNG、JPEG、BMP），以 multipart/form‑data 形式上传 | `200 OK` —— 背景已应用 |
| 删除背景 | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` —— 工作簿文件名<br>`sheetName` —— 目标工作表名称 | *无* | `200 OK` —— 背景已移除 |

#### 示例（Java SDK）

```java
// 添加背景图片
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// 删除背景图片
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### 示例（Python SDK）

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# 添加背景
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# 删除背景
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

更多其他语言示例（C#、PHP、Ruby），请参阅 SDK 文档。

**相关主题**  
- 了解有关工作表管理的更多信息：[工作表概览](/cells/worksheets/)。  
- 掌握 Aspose.Cells Cloud 的身份验证方法：[API 身份验证指南](/cells/authentication/)。  
- 探索其他电子表格元素，例如图表、数据表和公式：[电子表格元素索引](/cells/elements/)。  
---