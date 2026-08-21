---
title: "使用数据透视表筛选器"
second_title: "文档"
linktitle: 筛选器
type: docs
url: /zh/pivot-tables/add-filters/
aliases: [  /zh/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, 数据透视表, 筛选器, REST API, 云服务"
description: "了解如何使用 Aspose.Cells Cloud REST API 添加、获取和删除数据透视表筛选器。包含请求语法、必需参数、cURL 示例以及 C# 和 Go 的 SDK 代码片段。"
weight: 50
ArticleTitle: "使用数据透视表筛选器 – Aspose.Cells Cloud 文档"
---

此 REST API 将**数据透视表筛选器**添加到指定索引处的数据透视表中。

**前提条件**  
调用此接口前，您必须：

- 生成有效的 OAuth/JWT 访问令牌，并将其包含在 `Authorization` 请求头中。  
- 确保目标工作簿存储在您有访问权限的云文件夹中（指定 `folder`，可选指定 `storageName`）。  
- 使用 Aspose.Cells Cloud API 版本 3.0 或更高版本。

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称            | 类型    | 位置   | 描述                                                                                           |
| ------------------- | ------- | ------ | ---------------------------------------------------------------------------------------------- |
| **name**            | string  | 路径参数 | Excel 文件的名称。                                                                              |
| **sheetName**       | string  | 路径参数 | 包含数据透视表的工作表名称。                                                                    |
| **pivotTableIndex** | integer | 路径参数 | 数据透视表的零基索引，筛选器将应用于该数据透视表。                                               |
| **filter**          | object  | 请求体  | 定义筛选器设置的 JSON 对象。详见下方 **filter schema（筛选器模式）** 表格。                     |
| **needReCalculate** | boolean | 查询参数 | 当设置为 **true** 时，添加筛选器后强制工作簿重新计算。默认值为 **false**。                      |
| **folder**          | string  | 查询参数 | 文件所在的云存储文件夹。                                                                        |
| **storageName**     | string  | 查询参数 | 云存储的名称。                                                                                  |

**filter schema（筛选器模式）**

| 属性                         | 类型    | 描述                                                                                       |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------ |
| **AutoFilter**               | object  | 自动筛选器设置；如未使用可省略。                                                            |
| **EvaluationOrder**          | integer | 筛选器的评估顺序。                                                                          |
| **FieldIndex**               | integer | 筛选器所应用字段的零基索引。                                                                |
| **FilterType**               | string  | 筛选器类型（例如 `Value`、`Count`、`Label`）。                                             |
| **MeasureFldIndex**          | integer | 度量字段索引（如适用）。                                                                   |
| **MemberPropertyFieldIndex** | integer | 成员属性字段索引（如适用）。                                                                |
| **Name**                     | string  | 筛选器的可选名称。                                                                          |
| **Value1**                   | string  | 筛选器使用的第一值（例如范围的下限）。                                                     |
| **Value2**                   | string  | 筛选器使用的第二值（例如范围的上限）。                                                     |
| **CustomFilters**            | array   | 自定义筛选器对象集合（每个对象包含 `FilterOperatorType`、`Value1`、`Value2`）。            |
| **DynamicFilter**            | object  | 动态筛选器设置（例如 Top10、Bottom10）。                                                   |
| **IconFilter**               | object  | 基于图标的筛选器设置。                                                                      |
| **Top10Filter**              | object  | Top10/Bottom10 筛选器设置。                                                                |
| **ColorFilter**              | object  | 基于颜色的筛选器设置。                                                                      |
| **Visibledropdown**          | boolean | 指示筛选器下拉列表是否可见。                                                                |

> **注意：** 除非 API 参考中明确标注为可选，否则上述所有参数均为必需参数。

### 响应代码

| 代码 | 含义                                       |
| ---- | ------------------------------------------ |
| 200  | 筛选器添加成功。                           |
| 400  | 请求错误 – 参数无效。                      |
| 401  | 未授权 – 缺少或无效的令牌。                |
| 404  | 未找到 – 工作簿或数据透视表不存在。        |
| 500  | 服务器内部错误。                           |

**最佳实践**  
- 尽量保持筛选器对象尽可能精简；较大的筛选器定义可能增加请求延迟。  
- 调用具有幂等性：重复添加相同的筛选器不会产生重复项。  
- 每个账户的 API 请求频率限制为每分钟 100 次。  

*其他说明：*  
- 筛选器定义的最大大小为 1 MB；超过该大小的请求体将被拒绝，并返回 400 错误。  
- 若使用 `needReCalculate=true`，对大型工作簿的重新计算可能会增加响应时间。  

您可在此处查看完整的 OpenAPI 定义：  
[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### 示例 cURL 请求

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是开发 Aspose.Cells Cloud 应用的最快方式。SDK 负责处理底层细节，让您专注于业务逻辑。完整 SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务。

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // 初始化 API 客户端（请替换为您的凭据）
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // 构建筛选器对象
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // 准备请求
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // 执行请求
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

有关数据透视表的其他操作，请参阅 **添加**、**删除** 和 **清除** 筛选器的文档。