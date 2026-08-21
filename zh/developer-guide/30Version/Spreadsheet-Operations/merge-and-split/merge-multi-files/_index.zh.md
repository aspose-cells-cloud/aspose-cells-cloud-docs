---
title: "将多个 Excel 文件合并到单个工作簿中"
second_title: "文档"
linktitle: "合并多个 Excel 文件"
type: docs
url: /zh/merge-multi-files-into-excel/
aliases: [  /zh/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud, 合并多个 Excel 文件, REST API, 电子表格合并, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）将多个 Excel 工作簿合并为一个文件。内容包括 HTTPS 端点、cURL 命令、SDK 示例、所需参数及错误处理详情。"
weight: 32
---

## REST API

此 REST API 可将多个 Excel 文件合并为单个 Excel 工作簿。

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称        | 类型     | 位置     | 描述                                                                 | 是否必需 |
| --------------- | -------- | -------- | -------------------------------------------------------------------- | -------- |
| files[]         | file     | formData | 待合并的一个或多个 Excel 工作簿。请求中请使用 `file1`、`file2` 等命名。 | 是       |
| format          | string   | query    | 目标输出格式（例如 `xlsx`）。                                        | 是       |
| mergeToOneSheet | boolean  | query    | 设置为 `true` 表示将所有工作表合并为一张工作表；默认为 `false`。     | 否       |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64 字符串]"
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                   |
|--------|-------------------|----------------------------------------|
| 200    | OK（请求成功）    | 过滤操作成功；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                   |

## 如何使用 SDK 调用 PostMerge API

### PostMerge API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64字符串--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}