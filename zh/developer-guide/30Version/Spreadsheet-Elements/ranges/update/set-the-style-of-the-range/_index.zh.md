---
title: "设置范围样式 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "设置范围样式"
type: docs
url: /zh/ranges/update/style/
aliases: [  /zh/set-the-style-of-the-range/ ]
keywords: "Aspose.Cells, 范围样式, API, Excel, 云"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表中的单元格范围设置样式。内容包括身份验证步骤、请求格式、响应详情，以及适用于 .NET、Java、Python、Go 等语言的 SDK 示例。"
weight: 70
---

## **简介**
本示例演示如何使用 Aspose.Cells Cloud API 设置范围的样式。您可以从多种编程语言调用该 API，例如 .NET、Java、PHP、Ruby、Python、JavaScript（jQuery）等。

## **API 信息**

| API                                                   | 类型 | 描述                         | 资源链接                                                                                                                                     |
| ----------------------------------------------------- | ---- | ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | 设置命名范围的单元格样式     | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL 示例**

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

**前置条件**  
1. 通过 OAuth2 客户端凭据流程获取访问令牌（`POST https://api.aspose.cloud/connect/token`）。  
2. 在每个请求中包含请求头 `Authorization: Bearer <access_token>`。  

**请求**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*`Range` 对象指定范围的左上角单元格及其大小；`Style` 对象包含要应用的格式设置选项。*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**响应**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**错误处理** – 对于失败的调用，API 会返回相应的 HTTP 状态码（例如 400、401、500），并附带一个包含 `Error` 和 `Message` 字段的 JSON 响应体。请检查 `Code` 值；任何非 200 的结果均应记录并根据您的错误处理策略进行处理。  

{{< /tab >}}

{{< /tabs >}}

## **SDK 源码**
Aspose.Cells Cloud SDK 可从此页面下载：[可用 SDK](/cells/available-sdks/)

### **SDK 示例**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}