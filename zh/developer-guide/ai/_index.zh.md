---
title: "Aspose.Cells Cloud AI – 任务分解、电子表格与文本翻译"
second_title: "文档"
ArticleTitle: "提升您的 AI 技能：学习 Excel 翻译、任务拆分等"
linktype: "AI"
type: docs
url: /zh/ai/
keywords: "Aspose.Cells, 云 AI, Excel 翻译, 任务分解, REST API"
description: "探索 Aspose.Cells Cloud AI，实现任务分解、电子表格及纯文本文件翻译。包含 REST 接口、示例代码与最佳实践。"
weight: 20
---

Aspose.Cells Cloud AI 提供三种强大的 AI 驱动服务，简化 Excel 与文本数据的处理工作：**任务分解（Decompose User Task）**、**电子表格翻译（Translate Spreadsheet）** 和 **文本文件翻译（Translate Text File）**。这些 API 支持开发者以编程方式将复杂用户目标分解为可执行步骤、翻译整个工作簿或纯文本文件，并将结果集成到自定义应用程序中。请使用以下接口快速上手，并参考各服务提供的详细请求/响应规范。

- **[任务分解](https://docs.aspose.cloud/cells/decompose-user-task/)** – 使用 Aspose.Cells Cloud AI 将用户目标转换为顺序执行的操作计划。  
  - **请求方法：** `POST`  
  - **接口地址：** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **请求头：** `Authorization: Bearer <access_token>`，`Content-Type: application/json`  
  - **请求体（JSON）：**  
    ```json
    {
      "task": "生成包含图表和数据透视表的季度销售报告"
    }
    ```  
  - **响应：** 返回包含任务列表的电子表格文件，可下载。  
  - **状态码：** `200 OK`（成功），`400 Bad Request`（错误请求），`401 Unauthorized`（未授权），`500 Internal Server Error`（内部服务器错误）  
  - **前置条件：** 具备具有 **CellsAI** 作用域的有效访问令牌。  
  - **示例响应（JSON 片段）：**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **说明：** 生成的工作簿包含一个名为 **TaskList** 的工作表，其中列出了有序步骤。速率限制：每分钟 100 次请求。

- **[电子表格翻译](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – 使用 Aspose.Cells Cloud AI 翻译整个电子表格。  
  - **请求方法：** `POST`  
  - **接口地址：** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **请求头：** `Authorization: Bearer <access_token>`，`Content-Type: multipart/form-data`  
  - **请求参数：**  
    - `file` – 待翻译的 Excel 文件（二进制）。  
    - `targetLanguage` – 目标语言的 ISO 语言代码（例如 `fr`、`de`）。  
  - **响应：** 返回已翻译的工作簿文件，可下载。  
  - **状态码：** `200 OK`（成功），`400 Bad Request`（错误请求），`401 Unauthorized`（未授权），`415 Unsupported Media Type`（不支持的媒体类型），`500 Internal Server Error`（内部服务器错误）  
  - **前置条件：** 具备具有 **CellsAI** 作用域的访问令牌，且存储配额充足。  
  - **示例响应（JSON 片段）：**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **说明：** 所有单元格值、批注和工作表名称均被翻译。速率限制：每分钟 100 次请求。

- **[文本文件翻译](https://docs.aspose.cloud/cells/translate-text-file/)** – 使用 Aspose.Cells Cloud AI 翻译整个文本文件。  
  - **请求方法：** `POST`  
  - **接口地址：** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **请求头：** `Authorization: Bearer <access_token>`，`Content-Type: multipart/form-data`  
  - **请求参数：**  
    - `file` – 待翻译的文本文件（二进制）。  
    - `targetLanguage` – 目标语言的 ISO 语言代码（例如 `es`、`ja`）。  
  - **响应：** 返回已翻译的文本文件。  
  - **状态码：** `200 OK`（成功），`400 Bad Request`（错误请求），`401 Unauthorized`（未授权），`415 Unsupported Media Type`（不支持的媒体类型），`500 Internal Server Error`（内部服务器错误）  
  - **前置条件：** 具备具有 **CellsAI** 作用域的有效访问令牌。  
  - **示例响应（JSON 片段）：**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **说明：** 支持最大 5 MB 的 UTF-8 编码纯文本文件。速率限制：每分钟 100 次请求。