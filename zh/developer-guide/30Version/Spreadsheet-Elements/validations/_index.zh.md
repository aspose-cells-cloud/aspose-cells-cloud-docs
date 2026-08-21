---
title: "处理 Excel 数据验证"
second_title: "文档"
linktype: "数据验证"
type: docs
url: /zh/validations/
keywords: "Excel 数据验证、Aspose.Cells Cloud、REST API、电子表格、Office Cloud"
description: "了解如何使用 Aspose.Cells Cloud REST API 以编程方式添加、获取、更新、删除和清除 Excel 数据验证规则。包含 .NET、Java、Python 和 PHP 的示例。"
weight: 100
ArticleTitle: "处理 Excel 数据验证 - Aspose.Cells Cloud API 文档"
---

Excel 数据验证是 Microsoft Excel 中的一项功能，用于控制用户在工作表单元格中可输入的内容。它可以限制输入为特定日期范围、仅限整数，甚至可创建下拉列表，从而节省空间并在单个单元格中显示值。您还可以定义自定义消息，当用户输入错误值或无效格式时显示该消息。

例如，用户可以指定会议安排在上午 9:00 至下午 6:00 之间。

数据验证可用于确保值为正数、某月 15 日至 30 日之间的日期、未来 30 天内的日期，或少于 25 个字符的文本输入等。

### API 摘要

| 操作 | HTTP 方法 | 端点 | 描述 |
|------|-----------|------|------|
| 添加 | POST | `/cells/{file}/worksheets/{sheet}/validations` | 创建验证规则 |
| 获取 | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 获取特定规则 |
| 获取全部 | GET | `/cells/{file}/worksheets/{sheet}/validations` | 列出所有规则 |
| 更新 | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 修改规则 |
| 删除 | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 移除规则 |
| 清除 | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | 移除所有规则 |

## 处理 Excel 文件中的数据验证

- [如何向 Excel 工作表添加验证规则](/zh/cells/validations/add/)
- [如何从 Excel 工作表获取验证规则](/zh/cells/validations/get/)
- [如何从 Excel 工作表获取所有验证规则](/zh/cells/validations/get-all/)
- [如何从 Excel 工作表删除验证规则](/zh/cells/validations/delete/)
- [如何清除 Excel 工作表中的所有验证规则](/zh/cells/validations/clear/)
- [如何更新 Excel 工作表上的验证规则](/zh/cells/validations/update/)
---