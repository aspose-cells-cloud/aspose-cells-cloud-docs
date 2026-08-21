---
title: "保存选项"
second_title: "文档"
linktype: "保存选项"
type: docs
url: /zh/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, 工作簿, REST API, 文件格式, PDF, CSV, JSON, HTTP 压缩, 图表缓存, 命名区域, 目录创建"
description: "介绍 Aspose.Cells Cloud REST API 的 SaveOptions 属性，帮助开发者在多种文件格式及选项（如 HTTP 压缩、图表缓存刷新、自动创建目录等）中配置工作簿保存行为。"
weight: 79
ArticleTitle: "SaveOptions 保存选项 – Aspose.Cells Cloud REST API 文档"
---

# SaveOptions 属性

SaveOptions（保存选项）允许您在使用 Aspose.Cells Cloud REST API 时控制工作簿的保存方式。通过配置这些选项，您可以启用 HTTP 压缩、指定输出格式、管理临时存储空间，并控制其他行为，例如图表缓存刷新和自动创建目录。

**前置条件**  
- 已通过身份验证的 Aspose.Cells Cloud 会话（OAuth 2.0 或 JWT）。  
- 目标工作簿必须在保存前通过 API 加载或创建。

| 名称                      | 类型       | 描述                                                                                      | 说明       |
| ------------------------- | ---------- | ----------------------------------------------------------------------------------------- | ---------- |
| **EnableHTTPCompression** | **bool?**  | 启用响应的 HTTP 压缩。                                                                   | [可选]     |
| **SaveFormat**            | **string** | 指定工作簿保存的目标文件格式。                                                            | [可选]     |
| **ClearData**             | **bool?**  | 在保存文件后清空工作簿数据。                                                              | [可选]     |
| **CachedFileFolder**      | **string** | 用于临时存储大量数据的缓存文件夹路径。                                                    | [可选]     |
| **ValidateMergedAreas**   | **bool?**  | 指示在保存文件前是否验证合并区域。默认值为 false。                                        | [可选]     |
| **RefreshChartCache**     | **bool?**  | 在保存前刷新图表缓存数据。                                                                | [可选]     |
| **CreateDirectory**       | **bool?**  | 若为 true 且目录不存在，则在保存文件前自动创建该目录。                                    | [可选]     |
| **SortNames**             | **bool?**  | 在保存时按字母顺序对命名区域进行排序。                                                    | [可选]     |

**请求**  
- **方法：** `POST`（或根据操作使用 `PUT`）  
- **端点：** `/cells/workbook/save`  
- **请求头：**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **请求体：** JSON 格式的 `SaveOptions` 模型（见上表）与工作簿数据或引用组合。

**响应示例**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "工作簿已成功保存。"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
|--------|----------------|--------------------------------------------|
| 200    | OK（成功）     | 过滤器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                    |

**说明 / 注意事项**  
- 当 **CreateDirectory** 设置为 `true` 时，若目标文件夹不存在，API 将自动创建该文件夹。  
- 启用 **EnableHTTPCompression** 可减小大型工作簿的响应体体积，但客户端必须支持 gzip/deflate 解码。  
- 若图表依赖于自工作簿生成以来可能已更改的动态数据，应使用 **RefreshChartCache**。