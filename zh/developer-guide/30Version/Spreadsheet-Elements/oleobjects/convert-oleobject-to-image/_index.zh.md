---
title: "将 OLE 对象转换为图像 – Aspose.Cells Cloud REST API"
description: "从 Excel 工作表中提取嵌入的 OLE 对象，并使用 Aspose.Cells Cloud REST API 将其转换为 PNG、JPEG、TIFF、GIF、EMF 或 BMP 格式。"
keywords:
  - "将 OLE 对象转换为图像"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "图像转换"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# 将 OLE 对象转换为图像

从工作表中提取嵌入的 OLE 对象，并以请求的图像格式返回。

---

## 前置条件

调用此接口前，请确保已完成以下准备工作：

1. **Aspose.Cells Cloud 账户** – 在 [Aspose Cloud 门户](https://dashboard.aspose.cloud/) 上注册账户。  
2. **工作簿已上传至云存储** – 可使用 **上传文件** API 或 Aspose Cloud 界面完成上传。  
3. **JWT 访问令牌** – 参照 [身份验证指南](/total/getting-started/rest-api-overview/authenticating-api-requests/) 获取令牌。  

---

## 安全性与身份验证

所有 Aspose.Cells Cloud API 均要求使用 **基于 JWT 令牌的身份验证**。请将令牌置于 `Authorization` 请求头中：

```http
Authorization: Bearer <jwt-token>
```

仅支持 HTTPS 接口；请勿使用 `http://`。

---

## 请求

### HTTP 方法
`GET`

### 接口地址
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### 路径参数

| 名称            | 类型   | 是否必填 | 描述                                      |
|-----------------|--------|----------|-------------------------------------------|
| `name`          | 字符串 | ✅       | 工作簿文件名称（例如：`Book1.xlsx`）。    |
| `sheetName`     | 字符串 | ✅       | 包含 OLE 对象的工作表名称。               |
| `objectNumber`  | 整数   | ✅       | OLE 对象的从零开始的索引。                |

### 查询参数

| 名称            | 类型   | 是否必填 | 描述                                                                 |
|-----------------|--------|----------|----------------------------------------------------------------------|
| `format`        | 字符串 | ❌       | 期望的图像格式（`png`、`jpeg`、`tiff`、`gif`、`emf`、`bmp`）。若省略，默认为 `png`。 |
| `folder`        | 字符串 | ❌       | 工作簿所在文件夹的路径。                                             |
| `storageName`   | 字符串 | ❌       | 存储服务名称（例如：`MyCloud`）。                                    |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*请将 `<jwt-token>` 替换为有效的 JWT 令牌。*

---

## 响应

| 状态码 | 内容类型                   | 描述                               |
|--------|----------------------------|------------------------------------|
| `200`  | `image/png`（或请求的格式） | 代表 OLE 对象的二进制图像数据。     |
| `400`  | `application/json`         | 请求参数无效。                      |
| `401`  | `application/json`         | 身份验证失败（缺少或无效的 JWT）。 |
| `404`  | `application/json`         | 指定的工作簿、工作表或 OLE 对象未找到。 |
| `500`  | `application/json`         | 服务器端错误。                      |

### 处理二进制响应体

API 返回原始图像字节数据，您可：

* **直接保存为文件**（Linux/macOS 示例）：

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **编码为 Base64** 用于调试或嵌入 JSON：

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *示例（截断）Base64 输出：*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## 错误响应

| HTTP 状态码 | 错误码                 | 描述                         |
|-------------|------------------------|------------------------------|
| `400`       | `InvalidParameter`     | 一个或多个请求参数无效。      |
| `401`       | `AuthenticationFailed` | 缺少或无效的 JWT 令牌。       |
| `404`       | `PropertyNotFound`     | 请求的工作簿、工作表或 OLE 对象不存在。 |
| `500`       | `InternalError`        | 服务器发生意外错误。          |

---

## SDK 示例

以下代码片段展示了如何使用官方 SDK 调用该接口。请将 `YOUR_JWT_TOKEN` 及其他占位符替换为您的实际值。

| 语言      | 示例 |
|-----------|------|
| **C#** | <details><summary>显示代码</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>显示代码</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>显示代码</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>显示代码</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>显示代码</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>显示代码</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>显示代码</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>显示代码</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*（完整 SDK 列表请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。）*

---

## 相关操作

- **添加 OLE 对象** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **更新 OLE 对象** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **删除 OLE 对象** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **获取 OLE 对象列表** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

详情请参阅对应的 API 参考页面。

---

## 其他资源

- **OpenAPI 规范** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **身份验证指南** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK 仓库** – <https://github.com/aspose-cells-cloud>
- **性能与无障碍性** – 运行 Lighthouse 和 axe-core 审计，确保最佳加载速度并符合 WCAG 2.1 AA 无障碍标准。

---