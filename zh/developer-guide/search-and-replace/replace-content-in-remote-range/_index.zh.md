---
title: "Aspose.Cells Cloud 替换 Web API — 更新远程电子表格范围内的文本"
second_title: "文档"
ArticleTitle: "云 Excel 文件中的批量范围文本替换 — 查找与替换 API"
linktype: "replace-content-in-remote-range"
type: docs
url: /zh/replace-content-in-remote-range/
keywords: "远程 Excel 范围内替换文本、Aspose.Cells Cloud API、查找与替换 Excel、云电子表格编辑、远程 Excel 文件更新"
description: "使用 Aspose.Cells Cloud 在远程 Excel 文件的特定范围内查找并替换文本。支持身份验证、错误处理及多语言 SDK。"
weight: 100
---

在云中存储的 Excel 文件中执行批量文本替换。利用 Aspose.Cells 查找与替换 API，高效地在选定范围内查找并更新特定文本字符串。

## **远程范围内容替换 API**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **安全性与身份验证**

Aspose.Cells Cloud API 具备安全性，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名称      | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                 |
| :------------ | :----- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Path                        | 待修改的、存储于云存储中的工作簿文件名称（例如 `"report.xlsx"`）。                                                                                         |
| searchText    | String | Query                       | 在指定工作表和单元格区域内搜索的文本字符串。支持精确文本匹配。                                                                                             |
| replaceText   | String | Query                       | 将替换指定范围内所有 `searchText` 出现位置的文本字符串。                                                                                                   |
| worksheet     | String | Path                        | 执行查找与替换操作的工作表名称。                                                                                                                            |
| cellArea      | String | Path                        | 将执行文本搜索与替换的具体单元格范围（例如 `"A1:D20"`）。                                                                                                  |
| folder        | String | Query                       | 源工作簿所在的云存储文件夹路径。                                                                                                                            |
| storageName   | String | Query                       | （可选）工作簿所在的云存储名称。若省略，则使用默认云存储。                                                                                                  |
| region        | String | Query                       | （可选）设置文本处理的区域设置，可能影响搜索操作中的大小写敏感性及字符编码（例如 `"zh-CN"`、`"en-US"`、`"tr-TR"`）。                                         |
| password      | String | Query                       | （可选）若工作簿受密码保护，请提供密码以打开并修改文件。                                                                                                    |

### **响应**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

成功调用将返回如下具体 JSON 负载：

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### 错误代码

| 代码 | 消息            | 出现情形                                         |
| ---- | --------------- | ------------------------------------------------ |
| 400  | Bad Request     | 请求 URI 或参数格式错误。                         |
| 401  | Unauthorized    | 缺少或无效的身份验证令牌。                        |
| 404  | Not Found       | 无法找到或访问指定的工作簿。                      |
| 500  | Server Error    | 处理工作簿时发生内部服务器错误。                  |

## 应在何处使用远程电子表格范围内容替换 API？

- **批量云文件更新**：修改存储于 AWS S3、Azure Blob 等云存储中的多个 Excel 文件内容。
- **动态填充云模板**：批量为存储于云端的报表模板填充动态数据。
- **跨区域文件同步**：同步不同地理区域云存储中 Excel 文件的内容一致性。

## 为何应使用远程电子表格范围内容替换 API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，可实现快速开发，并配有详尽文档。相比自行构建解决方案，可大幅减少开发工作量。
- **降低人力成本**：减少专职处理文档整合的岗位需求。
- **按需付费**：无需前期投入，仅需为实际使用的 API 调用付费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。
- **保留复杂 Excel 格式**：以通用可访问的 PDF 格式保留复杂的 Excel 格式。

## 如何通过 SDK 使用远程电子表格范围内容替换 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange)定义了公开可用的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您仅需少量代码即可实现单元格电子表格的范围内容替换。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}