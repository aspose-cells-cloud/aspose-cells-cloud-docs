---
title: 使用 Aspose.Cells Cloud API 在 Excel 工作表中添加动态筛选器
description: 学习如何使用 Aspose.Cells Cloud REST API 向 Excel 工作表应用动态筛选器（例如：BelowAverage、Tomorrow、LastMonth）。内容包括身份验证、请求语法、参数说明、响应处理以及多种编程语言的 SDK 示例。
keywords: Aspose.Cells, 动态筛选器, Excel API, REST, 自动筛选, 云 SDK
slug: add-dynamic-filter
api_version: v3.0
---

## 概述

**PutWorksheetDynamicFilter** 操作可在 Excel 工作表的指定范围内添加动态筛选器。  
动态筛选器可自动评估日期、平均值或空白单元格等值，从而无需编写自定义公式即可创建“智能”视图。

## 前提条件

| 要求项 | 详情 |
|-------|------|
| **身份验证** | 需从 `/connect/token` 端点获取有效的 JWT 令牌，并在 `Authorization: Bearer <token>` 请求头中包含该令牌。 |
| **存储** | 工作簿必须位于 Aspose Cloud 存储位置（默认或自定义存储）。 |
| **支持的文件格式** | `.xlsx`、`.xls`、`.xlsm`、`.xlsb`、`.csv` 等。 |
| **权限** | 需具备对目标文件夹/文件的读写权限。 |

## HTTP 请求

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### 路径参数

| 参数 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `name` | string | ✅ | Excel 工作簿的名称（例如：`Book1.xlsx`）。 |
| `sheetName` | string | ✅ | 包含待筛选范围的工作表名称。 |

### 查询参数

| 参数 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `range` | string | ✅ | 应用筛选器的单元格范围（例如：`A1:B1`）。 |
| `fieldIndex` | integer | ✅ | 动态筛选器所作用列在该范围内的从零开始的索引。 |
| `dynamicFilterType` | string | ✅ | 要应用的动态筛选器类型（参见 **支持的动态筛选器类型**）。 |
| `matchBlanks` | boolean | ❌ | 若为 `true`，则筛选结果包含空白单元格；默认值为 `false`。 |
| `refresh` | boolean | ❌ | 若为 `true`，则应用筛选器后自动刷新筛选器。 |
| `folder` | string | ❌ | 工作簿所在存储中的文件夹路径。 |
| `storageName` | string | ❌ | 要使用的 Aspose Cloud 存储名称。 |

### 请求体

请求体为一个空的 JSON 对象：

```json
{}
```

## 支持的动态筛选器类型

| 值 | 含义 |
|----|------|
| `BelowAverage` | 值低于该列平均值的行。 |
| `AboveAverage` | 值高于该列平均值的行。 |
| `Tomorrow` | 日期等于明天的行。 |
| `Yesterday` | 日期等于昨天的行。 |
| `NextWeek` | 日期处于下一个自然周的行。 |
| `LastMonth` | 日期属于上个月的行。 |
| `ThisYear` | 日期属于当前年份的行。 |

## 示例请求（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT 请求的 JSON 请求体为空
```

## 示例响应

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "动态筛选器已成功应用。"
}
```

**HTTP 状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 筛选器已成功应用；响应包含操作详情。 |
| 400 | Bad Request（错误请求） | 缺少或无效的参数（例如：不支持的文件类型）。 |
| 401 | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413 | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。 |
| 500 | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

## SDK 示例

以下为最常用 SDK 的可直接运行代码片段。请将 `YOUR_JWT_TOKEN`、`YOUR_FILE_NAME` 等占位符替换为实际值。

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | 工作簿名称。
var sheetName = "Sheet1"; // string | 工作表名称。
var range = "A1:B1"; // string | 待筛选范围。
var fieldIndex = 0; // int? | 从零开始的列索引。
var dynamicFilterType = "BelowAverage"; // string | 动态筛选器类型。
var matchBlanks = true; // bool? | 是否包含空白单元格。
var refresh = true; // bool? | 应用后是否刷新。
var folder = "myFolder"; // string（可选）
var storageName = null; // string（可选）

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("调用 AutoFilterApi.PutWorksheetDynamicFilter 时发生异常：" + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder（可选）
            undefined              // storageName（可选）
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

（Ruby、PHP、Go 和 Perl 的类似代码片段可在官方 SDK 仓库中获取。）

## 相关主题

- **添加标准自动筛选器** – [添加标准筛选器](/autofilter/add-filter)  
- **添加日期筛选器** – [添加日期筛选器](/autofilter/add-date-filter)  
- **删除自动筛选器** – [删除自动筛选器](/autofilter/delete-filter)  
- **工作表操作** – [工作表 API 概述](/worksheets/)

## 备注

* 原始文档中使用的所有图片均已进行可访问性审查；装饰性图标已设置 `alt=""` 和 `role="presentation"`；功能性图标仍保留描述性 `alt` 文本。  
* 元关键词已清理，移除了空值和重复项。  
* 本页面现在采用清晰的标题层级结构（front matter 中单个 H1，主章节为 H2，子章节为 H3/H4），以提升 SEO 效果与屏幕阅读器导航体验。