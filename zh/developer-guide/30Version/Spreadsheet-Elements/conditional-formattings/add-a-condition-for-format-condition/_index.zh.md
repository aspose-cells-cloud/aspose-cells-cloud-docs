---
title: 为条件格式添加条件
description: 了解如何使用 Aspose.Cells Cloud REST API（v3.0）为工作表的条件格式添加条件。内容包括端点、参数、身份验证、cURL 示例、SDK 代码片段及错误处理。
keywords: "Aspose.Cells Cloud, 条件格式, 添加条件, REST API, Excel, 工作表"
type: docs
url: /zh/conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# 为条件格式添加条件

使用 Aspose.Cells Cloud REST API（v3.0），向工作表中已有的条件格式规则添加条件。

---

## 前置条件

| 要求 | 详细说明 |
|------|----------|
| **身份验证** | 通过 OAuth 2.0 流程获取的有效 JWT 访问令牌（Bearer 类型）。 |
| **API 版本** | v3.0 —— 端点 URL 中包含 `/v3.0/`。 |
| **存储位置** | 工作簿必须位于 Aspose.Cells Cloud 可访问的存储位置（默认为 `Default`）。 |
| **权限** | 对目标工作簿具有读/写权限。 |
| **支持的格式** | Aspose.Cells 支持的任何工作簿格式（例如 `.xlsx`、`.xls`、`.xlsm`）。 |

---

## 端点

**HTTP 方法：** `PUT`  
**URL：**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| 参数 | 位置 | 类型 | 必填 | 描述 |
|------|------|------|------|------|
| `name` | 路径参数 | string | **是** | 工作簿文件名（包含扩展名）。 |
| `sheetName` | 路径参数 | string | **是** | 包含条件格式的工作表名称。 |
| `index` | 路径参数 | integer | **是** | 要修改的条件格式集合的从零开始的索引。 |
| `type` | 查询参数 | string | **是** | 条件类型。允许值包括：`CellValue`、`Expression`、`ColorScale`、`DataBar`、`IconSet`、`Top10`、`UniqueValues`、`DuplicateValues`、`ContainsText`、`NotContainsText`、`BeginsWith`、`EndsWith`、`ContainsBlanks`、`NotContainsBlanks`、`ContainsErrors`、`NotContainsErrors`、`TimePeriod`、`AboveAverage`。 |
| `operatorType` | 查询参数 | string | **是** | 条件运算符。允许值包括：`Between`、`Equal`、`GreaterThan`、`GreaterOrEqual`、`LessThan`、`None`、`NotBetween`、`NotEqual`。 |
| `formula1` | 查询参数 | string | **是** | 与条件关联的第一个公式或值。 |
| `formula2` | 查询参数 | string | 否 | 第二个公式或值（仅当运算符需要两个值时才需提供，例如 `Between`）。 |
| `folder` | 查询参数 | string | 否 | 工作簿所在的存储文件夹。 |
| `storageName` | 查询参数 | string | 否 | 存储服务的名称。 |

> **注意：** 所有路径参数（`name`、`sheetName`、`index`）以及查询参数 `type`、`operatorType`、`formula1` 均为必填项；`formula2`、`folder` 和 `storageName` 为可选项。

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*请将 `<jwt_token>` 替换为有效的访问令牌，并根据需要调整 `name`、`sheetName`、`index` 及查询参数值。*

---

## 成功响应

```json
{
  "Code": "200",
  "Status": "OK"
}
```

该响应表示条件已成功添加。操作返回一个通用的 `CellsCloudResponse` 对象，其中包含 HTTP 状态码及简短状态信息。

---

## 错误响应

| HTTP 状态码 | 原因 | 示例响应体 |
|-------------|------|-------------|
| **400** | 请求无效 —— 缺少或参数值无效。 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 未授权 —— 缺少或 JWT 令牌无效。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 未找到 —— 工作簿、工作表或条件格式索引不存在。 | `{ "Code":"404", "Message":"File not found." }` |
| **500** | 内部服务器错误 —— 服务器意外失败。 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## 注意事项与常见问题

* **参数编码** —— 对 `formula1` / `formula2` 中的特殊字符进行 URL 编码（例如空格 → `%20`）。  
* **运算符兼容性** —— 某些运算符（如 `Between`）需要同时提供 `formula1` 和 `formula2`；对于仅需单值的运算符，请省略 `formula2`。  
* **条件格式索引** —— 索引为从零开始。如不确定，请使用 **获取条件格式** 端点查询正确索引。  
* **存储文件夹** —— 若工作簿位于非默认文件夹中，请提供 `folder` 查询参数；否则 API 将默认其位于根目录下。  
* **速率限制** —— Aspose.Cells Cloud 对每个账户设定了请求频率限制。若收到 429 响应，请退避并稍后重试。

---

## SDK 示例

以下为最常用 SDK 的可直接运行代码片段。请将占位符值（如 `YOUR_FILE`、`YOUR_SHEET` 等）替换为您的实际数据。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // 可选
        string storageName = null;     // 可选

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("调用 ConditionalFormattingsApi.PutWorksheetFormatConditionCondition 时发生异常：" + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("响应: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('状态:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "状态: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "调用 ConditionalFormattingsApi->put_worksheet_format_condition_condition 时发生异常：#{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "状态: " . $result->{status} . "\n";
};
if ($@) {
    warn "调用 ConditionalFormattingsApi->put_worksheet_format_condition_condition 时发生异常: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("错误：%v\n", err)
        return
    }
    fmt.Printf("状态：%s\n", resp.Status)
}
```

> **缺少 SDK** —— 若所需语言未列出，请参考通用 **API 参考文档** 并手动构造 HTTP 请求。

---

## 参考链接

- **[获取条件格式](https://docs.aspose.cloud/cells/zh/conditional-formattings/get-conditional-formattings/)** —— 获取工作表的条件格式规则列表。  
- **[删除条件格式](https://docs.aspose.cloud/cells/zh/conditional-formattings/delete-a-conditional-formatting/)** —— 删除已有的条件格式规则。  
- **[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** —— 此操作的完整机器可读定义。  

---