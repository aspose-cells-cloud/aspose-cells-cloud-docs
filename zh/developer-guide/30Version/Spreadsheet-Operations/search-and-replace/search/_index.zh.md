---
title: "在 Excel 文件中查找文本 – Aspose.Cells Cloud API"
description: "使用 Aspose.Cells Cloud API 在 Excel 文件（XLS、XLSX、XLSM、XLSB）和 ODS 文件中搜索特定文本。包含请求详情、cURL 与 SDK 示例及错误处理。"
keywords: "Aspose.Cells, Excel, 搜索, API, REST"
type: docs
url: /zh/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# 在 Excel 文件中查找文本 – Aspose.Cells Cloud API

## 概述
Aspose.Cells Cloud 提供了一个 **POST** 接口，用于在 Excel 工作簿（XLS、XLSX、XLSM、XLSB）和 OpenDocument 表格（ODS）文件中搜索指定文本字符串。API 将返回所有包含所请求文本的单元格，并附带指向匹配单元格所在工作表的链接。

> **使用场景**  
> - 在进一步处理前验证报告中是否存在特定值。  
> - 构建一个快速的“查找与替换”工具，首先列出所有匹配项。  
> - 为一批电子表格生成关键词索引。

---

## 前置条件
| 要求 | 详情 |
|------|------|
| **身份认证** | 通过 Aspose Cloud OAuth 流程获取的 JWT 令牌，该令牌必须包含 **Cells** 范围。 |
| **支持的格式** | XLS、XLSX、XLSM、XLSB、ODS |
| **最大文件大小** | 150 MB（压缩后）。超过该限制将返回 **413 Payload Too Large** 错误。 |
| **必需请求头** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **权限要求** | 若使用远程存储，令牌必须具有目标存储的 *读取* 权限；当文件以 `multipart/form-data` 形式上传时则无需此权限。 |

*提示：* 使用 **/connect/token** 接口生成 JWT 令牌。详情请参阅 [身份认证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

---

## 接口地址

| 项目 | 值 |
|------|-----|
| **HTTP 方法** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **用途** | 在已上传的 Excel 工作簿中搜索指定文本。 |
| **安全性** | JWT 令牌（Bearer）——详见上方 *前置条件*。 |

---

### **安全与身份认证**

Aspose.Cells Cloud 接口采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份认证</a>。

## 请求参数

| 名称 | 类型 | 位置 | 必填 | 描述 |
|------|------|------|------|------|
| `file` | **文件** | `formData`（multipart） | **是** | 要上传的电子表格文件。 |
| `text` | **字符串** | 查询字符串 | **是** | 要搜索的文本字符串。 |
| `password` | **字符串** | 查询字符串 | 否 | 打开受保护工作簿所需的密码（如适用）。 |
| `sheetname` | **字符串** | 查询字符串 | 否 | 限定搜索范围的工作表名称；若省略，则搜索所有工作表。 |
| `checkExcelRestriction` | **布尔值** | 查询字符串 | 否（默认值：`true`） | 当为 `true` 时，API 在搜索前会验证 Excel 特定限制（如只读单元格）。 |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*请将 `<jwt-token>` 替换为有效令牌，并根据需要调整查询参数。*

---

## 成功响应

**HTTP 200 – 搜索成功；响应中包含匹配文本项。**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### 响应字段说明

| 字段 | 类型 | 描述 |
|------|------|------|
| `Status` | string | 请求总体状态（成功时为 `OK`）。 |
| `Code` | integer | HTTP 状态码（200）。 |
| `TextItems.link` | object | 指向集合资源的超媒体链接。 |
| `TextItems.TextItemList` | array | 匹配项列表。每项包含： |
| `Text` | string | 与搜索文本匹配的单元格值。 |
| `link` | object | 指向匹配项所在工作表的超链接（`Href` 指向 `Workbook/worksheets/SheetName`）。 |

---

## 错误响应

| HTTP 状态码 | 含义 | 常见原因 | 示例响应体 |
|-------------|------|----------|------------|
| **400** | 请求错误 | 缺少必需参数、不支持的文件类型或无效查询值。 | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | 未授权 | 缺失或无效的 JWT 令牌。 | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | 载荷过大 | 上传文件超过 150 MB 限制。 | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | 服务器内部错误 | 服务器端发生意外问题。 | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## SDK 示例

以下为使用官方 Aspose.Cells Cloud SDK 执行 **PostSearch** 操作的最小化代码片段。请将 `YOUR_JWT_TOKEN` 与文件路径替换为您的实际值。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*（PHP、Ruby、Go 和 Perl 的 SDK 可在 [Aspose.Cells Cloud GitHub 仓库](https://github.com/aspose-cells-cloud) 获取。）*

---

## 附加说明

- **`checkExcelRestriction`** 默认为 `true`。仅当确认工作簿中不包含可能干扰搜索的受保护单元格时，才应将其设为 `false`。
- API 返回的 **超媒体链接**（`Href`）可与其他 Aspose.Cells 接口配合使用（例如下载工作表或获取单元格格式）。
- 搜索大型工作簿时，建议通过 `sheetname` 参数缩小搜索范围，以提升响应速度。

---

## 相关链接

- **身份认证指南** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **PostSearch 接口的 OpenAPI 规范** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>
- **速率限制与配额** – <https://docs.aspose.cloud/total/getting-started/limits/>