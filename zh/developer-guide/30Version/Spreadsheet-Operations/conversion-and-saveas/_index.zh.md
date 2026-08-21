---
title: "将 Excel 文件转换为其他格式或以不同方式保存"
second_title: "文档"
linktitle: "转换与另存为"
type: docs
url: /zh/conversion-and-save-as/
aliases: [/zh/convert-excel/, /zh/convert/]
keywords: "Aspose.Cells, Excel 转换 API, Excel 转 PDF, Excel 转 CSV, Excel 转 JSON, 云端电子表格转换"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 工作簿转换为 PDF、CSV、JSON、HTML 以及超过 15 种其他格式。包含端点详情、示例 cURL 命令以及 Java、.NET、Python 等语言的 SDK 代码片段。"
weight: 30
ArticleTitle: "使用 Aspose.Cells Cloud 将 Excel 文件转换为 PDF、CSV、JSON 等格式"
---

如果您最初以某种格式创建了 Excel 文件——例如 [XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) 或 [CSV](https://docs.fileformat.com/spreadsheet/csv/)——那么将 Excel 文件转换为其他格式以利用特定功能可能非常有用。例如，将 Excel 文件转换为 [PDF](https://docs.fileformat.com/pdf/) 可防止其内容被未授权修改，并使其更易于阅读和共享。

**前置条件**  
在调用转换 API 之前，请从 Aspose Cloud 获取 OAuth 2.0 访问令牌，并确保工作簿已存储在您的 Aspose Cloud 存储中（或作为请求体包含在 PUT 转换端点中）。

文档转换是一个复杂的过程。许多因素会影响转换过程的复杂性，这些因素在转换过程中都应予以考虑。提供精确、专业级别的 Excel 格式间转换是 Aspose.Cells Cloud 的核心功能之一。

该服务可无缝支持任意文档格式的转换。您可以导入和导出以下格式的文档：

**支持的格式**  
- 支持导入/导出：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)
- 仅支持导出：[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)

### 转换 API

| API                         | 描述                                                                 |
| :-------------------------- | :------------------------------------------------------------------- |
| `GET /cells/{name}`         | 从云端存储获取 Excel 工作簿并将其转换为请求的格式。                 |
| `PUT /cells/convert`        | 将请求体中提供的 Excel 工作簿转换为指定的输出格式。                 |
| `POST /cells/{name}/saveAs` | 将现有 Excel 工作簿直接以其他格式保存到云端存储中。                  |

**API 详情**

- **GET /cells/{name}**  
  - **路径参数：** `name` – 工作簿文件名（必填）。  
  - **查询参数：** `format` – 目标格式（例如：pdf、csv、json）；`storage` – 云端存储名称（可选）；`folder` – 存储内文件夹路径（可选）。  
  - **响应：** 转换后工作簿的文件流；`Content‑Type` 与目标格式匹配。  
  - **状态码：** 200 OK、400 Bad Request、401 Unauthorized、404 Not Found、500 Internal Server Error。  

- **PUT /cells/convert**  
  - **请求体：** multipart/form‑data，包含源工作簿文件（`file`）和必填字段 `format`（指定所需输出格式）。  
  - **响应：** 转换后文件的二进制流。  
  - **状态码：** 200 OK、400 Bad Request、401 Unauthorized、500 Internal Server Error。  

- **POST /cells/{name}/saveAs**  
  - **路径参数：** `name` – 现有工作簿名称。  
  - **查询参数：** `format` – 目标格式；`outPath` – 云端存储中的目标路径（可选）；`storage` – 存储名称（可选）。  
  - **响应：** 包含操作结果和保存文件路径的 JSON 对象。示例响应如下：  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "文件保存成功。",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **状态码：** 200 OK、400 Bad Request、401 Unauthorized、404 Not Found、500 Internal Server Error。  

**转换为 PDF 的示例 cURL 命令**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK 代码片段（GET /cells/{name}）**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK 代码片段（PUT /cells/convert）**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK 代码片段（POST /cells/{name}/saveAs）**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

以下文章详细介绍了每个 API，并提供了额外的 cURL 和 SDK 示例：

- [将 Excel 文件转换为其他格式](/zh/cells/convert-an-excel-file-to-different-formats)
- [将 Excel 文件另存为其他格式](/zh/cells/save-an-excel-file-as-other-formats-files)
- [将 Excel 文件转换为 CSV 文件](/zh/cells/convert-excel-file-to-csv-file)
- [将 Excel 文件转换为 DOCX 文件](/zh/cells/convert-excel-file-to-docx-file)
- [将 Excel 文件转换为 HTML 文件](/zh/cells/convert-excel-file-to-html-file)
- [将 Excel 文件转换为 JSON 文件](/zh/cells/convert-excel-file-to-json-file)
- [将 Excel 文件转换为 Markdown 文件](/zh/cells/convert-excel-file-to-markdown-file)
- [将 Excel 文件转换为 PDF 文件](/zh/cells/convert-excel-file-to-pdf-file)
- [将 Excel 文件转换为 PNG 文件](/zh/cells/convert-excel-file-to-png-file)
- [将 Excel 文件转换为 PPTX 文件](/zh/cells/convert-excel-file-to-pptx-file)
- [将 Excel 文件转换为 SQL 文件](/zh/cells/convert-excel-file-to-sql-file)
- [将 Excel 文件转换为 TIFF 文件](/zh/cells/convert-excel-file-to-tiff-file)
---