---
title: "压缩和修复 Excel 文件"
second_title: "文档"
type: docs
url: /compress-and-repair-excel-files/
linktitle: "压缩和修复"
keywords: "Aspose.Cells, Excel 压缩, Excel 修复, 云 API, 减小 Excel 文件大小, 恢复损坏的工作簿, 压缩 Excel 文件, 修复 Excel 工作簿"
description: "了解如何使用 Aspose.Cells Cloud API 压缩大型 Excel 工作簿以及修复损坏的文件。包含分步示例、支持的语言和最佳实践。"
weight: 100
ArticleTitle: "压缩和修复 Excel 文件 – Aspose.Cells Cloud API"
---

压缩 Excel 工作簿可通过移除未使用的样式、图像和共享字符串来减小文件体积，而修复则用于恢复损坏工作簿的完整性。Aspose.Cells Cloud API 为上述两种操作分别提供了专用的端点。

- **[压缩 Excel 文件中的数据](https://docs.aspose.cloud/cells/compress-excel-files/)**
- **[修复 Excel 文件](https://docs.aspose.cloud/cells/repair-excel-files/)**

**压缩工作簿 API**  
**压缩** 操作使用简单的 POST 请求。以下是完整的请求/响应规范：

| 方法 | 端点 | 必需参数 | 请求体 | 示例响应 | 常见状态码 |
|------|------|---------|--------|----------|-----------|
| POST | `/cells/compress` | `file`（二进制）— 待压缩的工作簿；可选 `outPath`（字符串）— 输出路径 | *无*（文件以 multipart/form‑data 形式发送） | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`、`400 Bad Request`、`401 Unauthorized` |

**修复工作簿 API**  
**修复** 操作同样使用 POST 请求。其规范如下：

| 方法 | 端点 | 必需参数 | 请求体 | 示例响应 | 常见状态码 |
|------|------|---------|--------|----------|-----------|
| POST | `/cells/repair` | `file`（二进制）— 损坏的工作簿；可选 `outPath`（字符串）— 保存修复后文件的路径 | *无*（文件以 multipart/form‑data 形式发送） | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`、`400 Bad Request`、`415 Unsupported Media Type` |

上述表格为开发者提供了调用 API 所需的关键信息，无需跳转其他页面即可直接使用。

**更多资源**  
- 查阅完整的 **[压缩 Excel 文件](/compress-excel-files/)** 指南，了解移除未使用行/列等高级选项。  
- 阅读 **[修复 Excel 文件](/repair-excel-files/)** 文档，获取故障排查技巧及错误码说明。  
- 探索其他相关操作，例如 **[获取文件信息](/file-info/)** 和 **[电子表格操作](/spreadsheet-operations/)**，以更全面地理解 Aspose.Cells Cloud API。