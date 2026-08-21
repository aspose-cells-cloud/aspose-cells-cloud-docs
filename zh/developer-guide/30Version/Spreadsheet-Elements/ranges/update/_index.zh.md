---
title: "如何更新 Excel 工作表中的区域内容"
second_title: "文档"
linktitle: "更新"
type: docs
url: /zh/ranges/update/
keywords: "Excel, 区域更新, Aspose.Cells Cloud, REST API, 电子表格, 区域样式, 区域值, 行高, 列宽"
description: "使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中的区域内容。通过支持的 SDK 修改样式、值、行高和列宽。"
weight: 20
ArticleTitle: "如何更新 Excel 工作表中的区域内容 – Aspose.Cells Cloud 文档"
---

## 在 Excel 工作表中更新区域内容

在使用更新操作前，请确保您已获取有效的 Aspose.Cells Cloud API 令牌，并且目标工作簿已存储于您的云存储中。该 API 可通过适用于 Android、.NET、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift 的 SDK 调用。

下表简要总结了四项主要更新操作，为开发者提供快速参考，涵盖各操作对应的 HTTP 方法、端点格式、关键参数以及典型成功响应。

| 操作            | HTTP 方法 | 端点格式                                                                                             | 关键参数                      | 200‑OK 响应                 |
|-----------------|-----------|------------------------------------------------------------------------------------------------------|-------------------------------|-----------------------------|
| 设置样式        | PUT       | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style` 对象                  | 已更新的区域样式            |
| 设置值          | POST      | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values` 数组                 | 已更新的区域值              |
| 设置行高        | PUT       | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` 数值                 | 已更新的行高                |
| 设置列宽        | PUT       | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` 数值                  | 已更新的列宽                |

本页面快速链接至四项主要更新操作：设置 Excel 工作表中区域的样式、设置区域的值、调整行高以及调整列宽。

- [如何设置 Excel 工作表中区域的样式。](/cells/ranges/update/style/) 
- [如何设置 Excel 工作表中区域的值。](/cells/ranges/update/values/) 
- [如何设置 Excel 工作表中区域的行高。](/cells/ranges/update/row-height/) 
- [如何设置 Excel 工作表中区域的列宽。](/cells/ranges/update/column-width/) 
---