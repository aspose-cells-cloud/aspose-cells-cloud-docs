---
title: "设置工作表的页面设置"
second_title: "Document"
linktitle: "设置页面设置"
type: docs
url: /zh/set-page-setup/
keywords: "Aspose.Cells, Excel, 页面设置, REST API, 工作表, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 设置 Excel 工作表的页面设置。包含请求详情、安全的 HTTPS cURL 示例、响应状态码以及多种编程语言的 SDK 代码片段。"
weight: 20
ArticleTitle: "设置工作表的页面设置 – Aspose.Cells Cloud API 指南"
---

前置条件：调用此 API 前，您必须拥有有效的 JWT（OAuth）令牌，并且工作簿必须位于您具有读/写权限的 Aspose Cloud 存储位置。请确保令牌已包含在 **Authorization** 请求头中，且您的账户具备必要的 API 配额。

此 REST API 用于设置 Excel 工作表的页面设置。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称       | 类型   | 位置 | 描述                 |
| -------------- | ------ | ---- | -------------------- |
| name           | string | path | 文档名称。           |
| sheetName      | string | path | 工作表名称。         |
| pageSetup      | object | body | 页面设置描述对象。   |
| folder         | string | query| 文档所在文件夹。     |
| storageName    | string | query| 存储空间名称。       |

**`pageSetup` 对象的示例 JSON 载荷**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API 将返回一个 JSON 对象，指示操作结果：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**可能的响应状态码**

| 状态码 | 含义             | 触发条件                                               |
|--------|------------------|--------------------------------------------------------|
| 200    | OK（成功）       | 页面设置更新成功                                       |
| 400    | Bad Request      | JSON 载荷无效或缺少必需字段                            |
| 401    | Unauthorized     | 缺少或 JWT 令牌无效                                    |
| 404    | Not Found        | 工作簿或工作表名称不存在                               |
| 500    | Internal Server Error | 服务器内部发生意外错误                            |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}