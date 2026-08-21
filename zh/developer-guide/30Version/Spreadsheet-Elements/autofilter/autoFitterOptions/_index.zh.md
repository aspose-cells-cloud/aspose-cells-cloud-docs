---
title: "AutoFitterOptions – 属性与使用指南 | Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "AutoFitterOptions"
type: docs
url: /zh/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel 自动调整行高, 行高, 合并单元格, API"
description: "了解如何使用 Aspose.Cells Cloud API 中的 AutoFitterOptions 对象控制行高自动调整、合并单元格处理、隐藏行/列、语言设置以及渲染相关选项。"
weight: 79
ArticleTitle: "AutoFitterOptions – Aspose.Cells Cloud 属性与使用指南"
---

# AutoFitterOptions 属性

`AutoFitterOptions` 对象可让您精细调整 Aspose.Cells Cloud 所执行的自动行高调整行为。当您需要精确控制合并单元格处理方式、隐藏行/列、特定语言格式化规则，或与渲染行为相关的设置时，该对象非常有用。

**前置条件** – 使用这些选项前，您必须以有效的 OAuth 2.0 访问令牌进行身份验证，且该令牌需包含 **Cells.ReadWrite** 范围。此请求适用于支持 v3.0 API 的任一 SDK 版本。

| 名称                       | 类型        | 描述                                                                                     | 说明                                                                                                       |
| -------------------------- | ----------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | 指定合并单元格的自动调整方式。                                                           | 可选值：`All`（全部）、`First`（首行）、`None`（不调整）。默认值：`All`。示例 JSON：`"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**           | **boolean** | 若为 **true**，则在自动调整过程中忽略隐藏的行和列。                                        | 默认值：`false`。示例 JSON：`"IgnoreHidden":false`                                                         |
| **OnlyAuto**               | **boolean** | 指示是否仅对未手动设置行高的行执行自动调整。                                              | 默认值：`false`。示例 JSON：`"OnlyAuto":false`                                                             |
| **DefaultEditLanguage**    | **string**  | 设置工作簿的默认编辑语言。                                                                | 默认值：系统语言（例如 `"en-US"`）。示例 JSON：`"DefaultEditLanguage":"en-US"`                              |
| **MaxRowHeight**           | **double**  | 自动调整行高时应用的最大行高（单位：磅）。若值为 **0**，表示无限制。                      | 默认值：`0`。示例 JSON：`"MaxRowHeight":0`                                                                 |
| **AutoFitWrappedTextType** | **string**  | 控制单元格内换行文本的自动调整方式。                                                      | 可选值：`All`（全部）、`OnlyWrapped`（仅换行文本）、`None`（不调整）。默认值：`All`。示例 JSON：`"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | 指定自动调整操作期间使用的格式化策略。                                                    | 常用值：`AutoFit`（自动调整）、`PreserveExisting`（保留现有格式）。默认值：`AutoFit`。示例 JSON：`"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | 指示自动调整是否应为渲染目的执行（例如生成 PDF 或图像）。                                 | 可选值：`True`、`False`。默认值：`False`。示例 JSON：`"ForRendering":"False"`                               |

以下是一个典型的 JSON 载荷，可用于向 API 发送请求以配置 `AutoFitterOptions`：

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

一个应用这些选项至工作簿的 `cURL` 请求示例：

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**端点参考**

| 方法 | URL | 必需参数 | 描述 |
|------|-----|----------|------|
| PUT  | `/cells/workbook/autoFitter` | `autoFitterOptions`（JSON 正文） | 将指定的 `AutoFitterOptions` 应用于目标工作簿。 |
| GET  | `/cells/workbook/autoFitter` | *无* | 获取当前工作簿的 `AutoFitterOptions` 设置。 |

**PUT 端点请求参数**

| 参数                     | 类型    | 是否必需 | 描述 |
|--------------------------|---------|----------|------|
| AutoFitMergedCellsType   | string  | 是       | 合并单元格的自动调整方式（`All`、`First`、`None`）。 |
| IgnoreHidden             | boolean | 否       | 是否忽略隐藏的行/列。 |
| OnlyAuto                 | boolean | 否       | 仅调整未手动设置行高的行。 |
| DefaultEditLanguage      | string  | 否       | 编辑语言（例如 `en-US`）。 |
| MaxRowHeight             | double  | 否       | 最大行高（单位：磅）；`0` 表示无限制。 |
| AutoFitWrappedTextType   | string  | 否       | 换行文本的处理方式（`All`、`OnlyWrapped`、`None`）。 |
| FormatStrategy           | string  | 否       | 格式化策略（`AutoFit`、`PreserveExisting`）。 |
| ForRendering             | string  | 否       | 是否为渲染目的应用自动调整（`True`、`False`）。 |

典型响应状态码：

- **200 OK** – 操作成功完成。  
- **400 Bad Request** – JSON 载荷无效或包含不支持的值。  
- **401 Unauthorized** – 缺少或无效的身份验证令牌。  
- **500 Internal Server Error** – 服务器内部错误。

**GET 响应示例**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

上述示例展示了如何在 Aspose.Cells Cloud API 中配置并调用 `AutoFitterOptions` 模型。