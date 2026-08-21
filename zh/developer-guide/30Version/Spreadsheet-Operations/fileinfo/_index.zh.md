---
title: "文件信息"
second_title: "文档"
linktitle: "文件信息"
type: docs
url: /zh/file-info/
keywords: "文件, 信息, Excel, Aspose.Cells, 云 API, 元数据, Base64"
description: "通过 Aspose.Cells 云 API 获取 Excel 文件名、大小及 Base64 编码内容。包含请求语法、示例代码及错误处理说明。"
weight: 79
ArticleTitle: "文件信息 – Excel 文件元数据与 Base64 内容（Aspose.Cells 云 API）"
---

## FileInfo 属性


| 名称            | 类型   | 描述                                             |
| --------------- | ------ | ------------------------------------------------ |
| **FileName**    | string | 文件名（含扩展名）。                              |
| **FileSize**    | long   | 文件大小（单位：字节）。                          |
| **FileContent** | string | 包含以 Base64 编码的原始 Excel 文件数据。         |

响应将以 JSON 格式返回，包含上述表格中的三个字段，例如：

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### 错误码

| HTTP 状态码 | 含义         | 触发条件                           |
| ----------- | ------------ | ---------------------------------- |
| 200         | 成功 – 请求成功。 | 正常响应。                         |
| 401         | 未授权       | 缺失或无效的身份认证令牌。         |
| 404         | 未找到       | 指定的文件不存在。                 |
| 500         | 服务器内部错误 | 服务端发生意外错误。               |

针对每种错误，请确保身份认证令牌有效（401）、验证文件路径是否正确（404），或参考通用错误处理指南了解重试策略（500）。

## 参见

- [获取工作簿](https://docs.aspose.cloud/cells/get-workbook) – 获取工作簿对象及其工作表。  
- [下载文件](https://docs.aspose.cloud/cells/download-file) – 以原始字节形式下载文件，不进行 Base64 编码。  
- [身份认证概述](https://docs.aspose.cloud/cells/authentication) – 如何获取并使用访问令牌。  
---