---
title: "开始使用 Aspose.Cells Cloud API——三步轻松处理 Excel 文件"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud 入门指南"
linktitle: "入门指南"
type: docs
url: /zh/getting-started/
description: "了解如何通过 Aspose.Cells Cloud REST API 在三个简单步骤中上传、转换和下载 Excel 文件。包含 cURL 代码示例。"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, 电子表格转换, Excel 转 PDF, 云电子表格, Aspose.Cells Cloud API"
---

- [概述](/zh/cells/overview/)
- [快速入门](/zh/cells/quickstart/)
- [可用 SDK](/zh/cells/available-sdks/)
- [支持的平台](/zh/cells/supported-platforms/)
- [支持的文件格式](/zh/cells/supported-file-formats/)
- [试用 Aspose.Cells Cloud](/zh/cells/evaluate-aspose-cells/)
- [定价方案](/zh/cells/pricing-plan/)
- [技术支持](/zh/cells/technical-support/)
- [如何运行 Docker 容器](/zh/cells/how-to-run-docker-container/)

**入门指南**

开始前，请确保您已获取有效的 **Aspose Cloud API 密钥** 和 **存储名称**。这些凭据是后续所有 API 调用的必要条件。

**步骤 1：上传 Excel 文件**  
将您的源工作簿上传至 Aspose Cloud 存储。

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*请求体*：文件以二进制流（`application/octet‑stream`）形式发送。  
*必填参数*：

- `path` – 文件在存储中的保存路径（例如：`folder/sample.xlsx`）。

**步骤 2：将工作簿转换为 PDF**  
文件上传完成后，发送转换请求。

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*必填参数*：

- `name` – 已上传工作簿的文件名（例如：`sample.xlsx`）。
- `format` – 目标格式（`pdf`）。
- `outputPath` – 转换后文件在存储中的路径（例如：`folder/result.pdf`）。

*示例响应体*（JSON）：

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**步骤 3：下载已转换的 PDF**  
从存储中获取生成的 PDF 文件。

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*必填参数*：

- `outputPath` – 上一步生成的 PDF 文件路径。

**请求/响应示例汇总**

| 操作 | HTTP 方法 | 端点（示例） | 参数 | 成功状态 |
|------|-----------|--------------|------|-----------|
| 上传 | PUT | /cells/storage/file/{path} | `path`（存储位置） | 200 OK |
| 转换 | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| 下载 | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**常见错误码**

- **400 Bad Request（错误请求）** – 缺失或无效的参数。  
- **401 Unauthorized（未授权）** – 无效或缺失访问令牌。  
- **404 Not Found（未找到）** – 指定的文件或路径不存在。  
- **500 Internal Server Error（内部服务器错误）** – 服务器意外错误；请重试或联系技术支持。