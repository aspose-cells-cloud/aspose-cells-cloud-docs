---
title: "电子表格操作"
second_title: "文档"
type: docs
url: /zh/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, 电子表格操作, 自动调整列宽, 批量处理, 文件保护, 转换, 导入导出, 文本处理"
description: "了解如何使用 Aspose.Cells Cloud REST API 执行自动调整列宽、批量转换、保护、合并以及查找替换等电子表格操作。包含简明使用说明与代码示例指导。"
weight: 100
ArticleTitle: "电子表格操作 – Aspose.Cells Cloud API 指南"
---

电子表格操作提供一份简明指南，介绍您可使用 **Aspose.Cells Cloud**（v3.0）对 Excel 工作簿执行的最常见操作。无论您需要自动调整列宽、批量处理文件、保护工作表，还是操作文本内容，REST API 均提供专用端点，支持 Python、C# 和 Java 等多种编程语言。下方列表链接至每项操作的详细文档，并附有简要使用说明，助您快速上手。

**前置条件**：调用这些端点前，您需拥有有效的 Aspose.Cells Cloud API 密钥，并在请求头中包含 `Authorization`（`Bearer <access-token>`）。以下示例均基于 API 版本 v3.0。

- **[自动调整选项](/zh/cells/auto-fitter-options/)** – 自动调整列宽和行高。`POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Excel 文件批量处理：转换、锁定、保护、拆分与解锁](/zh/cells/batch/)** – 单次请求可对最多 100 个文件执行批量操作（转换、锁定、保护、拆分、解锁）。`POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[压缩与修复 Excel 文件](/zh/cells/compress-and-repair-excel-files/)** – 减小文件体积并修复结构问题。`POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[将 Excel 文件转换为其他格式或另存为不同格式](/zh/cells/conversion-and-save-as/)** – 将 Excel 转换为 PDF、CSV、HTML 等格式，或更改输出格式。`GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[工作簿转换选项](/zh/cells/convert-workbook-options/)** – 精细调整转换设置，如页面尺寸、渲染选项及密码保护。`POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[创建 Excel 文件或生成 Excel 报表](/zh/cells/creating-files-and-reports/)** – 从零生成新工作簿，或基于模板创建。`PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 销售额", "value": 12345 }
  }
  ```
- **[向 Excel 文件导入数据及从 Excel 文件导出数据](/zh/cells/data-import-and-export/)** – 从 CSV、JSON 或数据库加载数据，导出工作表数据。`POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[加密、解密与数字签名 Excel 文件](/zh/cells/protect/)** – 应用密码保护、加密或数字签名。`POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[文件信息](/zh/cells/file-info/)** – 获取文件大小、格式、创建日期等元数据。`GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[合并与拆分 Excel 文件](/zh/cells/merge-and-split/)** – 合并多个工作簿为一个文件，或拆分工作簿为多个独立文件。`POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[在 Excel 文件中查找与替换文本内容](/zh/cells/search-and-replace/)** – 在工作表中查找并替换指定字符串。`POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "草稿",
    "newText": "终稿",
    "options": { "matchCase": false }
  }
  ```
- **[Excel 文本处理：添加文本、删除字符、文本截断、大小写转换等](/zh/cells/text-processing/)** – 对单元格值执行高级文本处理。`POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[在 Excel 文件中插入水印或设置背景](/zh/cells/watermark-and-background/)** – 添加图片或文本水印，设置工作表背景。`POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "机密",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Excel 文件操作：公式计算、自动调整列宽、清除对象等](/zh/cells/workbook/)** – 执行常见工作簿任务，如计算公式、清除对象、自动调整列宽等。`POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```