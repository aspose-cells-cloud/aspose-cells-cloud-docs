---
title: "处理 Excel 区域"
second_title: "文档"
linktitle: "区域"
type: docs
url: /zh/ranges/
aliases: [  /zh/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel 区域, REST API, SDK, .NET, Java, Python, 合并单元格, 复制区域, 设置区域值"
description: "了解如何使用 Aspose.Cells Cloud REST API 获取、修改、设置样式、合并、移动和复制 Excel 区域。包含 .NET、Java、Python 等语言的 SDK 代码示例。"
weight: 100
ArticleTitle: "处理 Excel 区域 – Aspose.Cells Cloud 文档"
---

**区域**表示单个单元格、整行、整列、连续的单元格块，或跨越多个工作表的三维（3-D）区域。

## 在 Excel 文件中处理区域

Aspose.Cells Cloud REST API 为每种区域操作提供了专用端点。以下列表链接至详细使用示例，并包含对应的 HTTP 方法和端点，便于快速参考。

- [获取工作簿内的命名区域](/cells/get-named-ranges-inside-the-workbook/) – 获取工作簿中定义的所有命名区域，返回其地址和作用域。**API**：`GET /cells/{fileName}/worksheets/{sheetName}/namedranges`。
- [根据命名区域获取单元格数据](/cells/get-cells-data-based-on-named-range/) – 返回属于指定命名区域的单元格的值。**API**：`GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`。
- [修改区域内的行高](/cells/cells/change-heights-of-rows-inside-the-range/) – 调整给定范围内每行的行高。**API**：`PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`。
- [修改区域内的列宽](/cells/cells/change-widths-of-columns-inside-the-range/) – 修改与该区域相交的所有列的列宽。**API**：`PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`。
- [将区域内的单元格合并为单个单元格](/cells/combines-a-range-of-cells-into-a-single-cell/) – 将所选单元格合并为一个单元格，并保留左上角单元格的值。**API**：`POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`。
- [带粘贴选项在工作表内复制区域](/cells/copy-range-in-a-worksheet-with-paste-options/) – 将源区域复制到目标区域，并支持可选的粘贴类型（值、格式、公式等）。**API**：`POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`。
- [设置区域的样式](/cells/set-the-style-of-the-range/) – 将字体、填充、边框和对齐方式等样式应用于区域内的每个单元格。**API**：`PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`。
- [取消区域中已合并单元格的合并](/cells/unmerge-merged-cells-of-the-range/) – 撤销之前的合并操作，恢复原始的各个独立单元格。**API**：`POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`。
- [随 Excel 工作表移动命名区域](/cells/move-a-named-ranged-with-a-excel-worksheet/) – 将命名区域移动到同一工作表内的新地址，或移动到其他工作表。**API**：`PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`。
- [设置 Excel 工作表中的区域值](/cells/ranges/set-value/) – 向指定区域写入单个值或值数组。**API**：`PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`。

所有请求与响应均为 JSON 格式。请在请求头中包含 `Authorization` 字段，并附上您的访问令牌以完成身份验证。