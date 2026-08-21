---
title: "任务"
second_title: "文档"
type: docs
url: /zh/tasks/
aliases: [  /zh/working-with-tasks/ ]
keywords: "Aspose Cells, 云 API, Excel 任务, 转换任务, 导入数据任务, SmartMarker, 保存结果, REST API, 电子表格自动化"
description: "探索 Aspose.Cells Cloud 任务 API 的完整功能集：转换、导入数据、保存结果、SmartMarker 等。了解用法、参数及 Excel 自动化的代码示例。"
weight: 100
ArticleTitle: "Aspose.Cells Cloud 任务 API"
---

## 使用任务

Aspose.Cells Cloud 提供了一个**任务 API**，使开发者能够在 Excel 工作簿上执行多种操作，例如转换格式、导入数据、执行 SmartMarker 模板以及保存结果。任务以异步方式执行：您先创建任务，再运行任务，最后获取执行结果。

**前置条件**：一个拥有有效 API 密钥的 Aspose Cloud 账户、支持的 Excel 文件格式，以及最新版本的 Cells API（v3.0 或更高版本）。

- [在任务 API 中支持上传请求文件](/zh/cells/support-request-file-in-task-api/) – 允许您将文件上传至云存储，并在后续任务中引用该文件，从而确保文件可用于处理。
- [使用 CellsObjectOperate 任务](/zh/cells/working-with-cellsobjectoperate-task/) – 在工作簿内对单元格对象（例如行、列）执行操作，例如添加、删除或更新单元格值。
- [使用转换任务](/zh/cells/working-with-convert-task/) – 将工作簿转换为 PDF、HTML、CSV 或 JSON 格式，支持指定页面范围、密码保护及自定义转换设置。
- [使用导入数据任务](/zh/cells/working-with-importdata-task/) – 从 CSV、JSON 或 XML 文件中导入数据到工作表中，可映射列到单元格，并可选指定起始行和列。
- [使用保存结果任务](/zh/cells/working-with-saveresult-task/) – 将先前执行任务的结果（例如已转换的文件）保存回云存储，或在响应中直接返回结果。
- [使用 SmartMarker 任务](/zh/cells/working-with-smartmarker-task/) – 使用 JSON 数据源处理包含 SmartMarker 标记（例如 `{{Customer.Name}}`）的工作簿，生成填充后的报告。
- [在任务 API 中使用工作表操作](/zh/cells/working-with-worksheetoperates-in-task-api/) – 作为任务工作流的一部分，执行工作表级别的操作，例如添加、删除或重命名工作表。

如需获取完整的方法规范（包括 HTTP 动词、端点 URL、请求/响应架构、参数表格及示例负载），请参阅上述链接指向的各任务页面。该详细 API 参考文档可帮助开发者快速、可靠地集成任务 API。