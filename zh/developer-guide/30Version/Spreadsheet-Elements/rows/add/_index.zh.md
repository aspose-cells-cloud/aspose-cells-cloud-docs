---
title: "如何向 Excel 工作表添加行"
second_title: "文档"
linktitle: "添加"
type: docs
url: /rows/add/
keywords: "Aspose.Cells, 添加行, Excel API, REST, C#, Java, Python, Node.js"
description: "分步指南，介绍如何使用 Aspose.Cells Cloud REST API 向 Excel 工作表添加单行或多行，并提供 C#、Java、Python 和 Node.js 的代码示例。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 向 Excel 工作表添加行——分步指南"
---

## 如何向 Excel 工作表添加行

本文介绍如何使用 Aspose.Cells Cloud REST API 向现有工作表插入单个空行或多行。请确保在开始操作前已获取有效的 API 密钥并安装了相应的 SDK。

**前置条件**  
- [ ] 拥有有效订阅的 Aspose.Cells Cloud 账户。  
- [ ] 从 Aspose Cloud 仪表板生成的 API 密钥/访问令牌。  
- [ ] 已安装并配置好受支持的 SDK（C#、Java、Python 或 Node.js）。  

**API 参考**  
- **HTTP 方法：** `POST`  
- **端点：** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **必需路径参数：**  
  - `fileName` – 存储在云端的 Excel 文件名。  
  - `sheetName` – 将添加行的工作表名称。  
- **查询参数：**  
  - `startrow` – 插入起始行的从零开始的索引。  
  - `totalRows` – 要插入的行数。  
  - `folder` – （可选）文件所在的云文件夹路径。  
  - `storage` – （可选）若使用非默认存储，则指定存储名称。  
- **请求体（JSON 示例）：**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURL 示例**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **成功响应（HTTP 200）：** 返回更新后的工作表信息，包括新的行数。  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **错误响应示例（HTTP 400）：**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "startrow 参数无效。必须为非负整数。"
  }
  ```

- **状态码说明：**  

  | 状态码 | 含义                         |
  |--------|------------------------------|
  | 200    | 行添加成功                   |
  | 400    | 参数无效或 JSON 格式错误     |
  | 401    | 身份验证失败                 |
  | 404    | 文件或工作表未找到           |
  | 500    | 服务器内部错误               |

以下是添加行的详细示例快速链接：

- [如何在 Excel 工作表中添加单个空行](/cells/rows/add/row/)
- [如何在 Excel 工作表中添加多个行](/cells/rows/add/rows/)
---