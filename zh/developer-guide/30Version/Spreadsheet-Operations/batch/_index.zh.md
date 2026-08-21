---
title: "Excel 文件批量处理：转换、锁定、保护、拆分和解锁"
second_title: "文档"
linktype: "docs"
url: /zh/batch/
keywords: "批量处理, Excel, 转换, 锁定, 保护, 拆分, 解锁, Aspose.Cells Cloud API, API 参考, 批量操作"
description: "Aspose.Cells Cloud API 支持对多个 Excel 文件进行批量处理，包括转换、锁定、保护、拆分和解锁操作。提供详细的 API 规范，并支持 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift 等多种 SDK。"
weight: 35
ArticleTitle: "Excel 文件批量处理 – 使用 Aspose.Cells Cloud API 进行转换、锁定、保护、拆分和解锁"
---

Aspose.Cells Cloud API 提供了批量处理端点，允许您在单次请求中对多个 Excel 文件执行常见操作。以下是可用批量操作的快速概览，以及每项操作的简明 API 规范。

- **["批量转换 Excel 文件"](https://docs.aspose.cloud/cells/batch/convert "Batch Convert Excel Files")**  
  *在一次请求中将多个 Excel 文件转换为所选输出格式。*  

  **API 详情**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **参数**  

  | 名称           | 类型     | 描述                                      |
  |----------------|----------|-------------------------------------------|
  | files          | file[]   | 待转换的一个或多个 Excel 文件。            |
  | outputFormat   | string   | 目标输出格式（例如：pdf、csv、html）。     |
  | storage        | string   | （可选）云存储名称。                       |

  **响应**  

  | 状态码 | 描述                             |
  |--------|----------------------------------|
  | 200    | 转换成功；返回处理后的文件。      |
  | 400    | 提供的参数无效。                  |
  | 401    | 未授权 — 缺少或无效的令牌。       |
  | 500    | 服务器内部错误。                  |

- **["批量锁定 Excel 文件"](https://docs.aspose.cloud/cells/batch/lock "Batch Lock Excel Files")**  
  *同时为多个 Excel 文件应用密码锁定。*  

  **API 详情**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **参数**  

  | 名称     | 类型   | 描述                           |
  |----------|--------|--------------------------------|
  | files    | array  | 文件标识符或 URL 的列表。       |
  | password | string | 用于锁定工作簿的密码。          |
  | storage  | string | （可选）云存储名称。            |

  **响应**  

  | 状态码 | 描述                     |
  |--------|--------------------------|
  | 200    | 文件锁定成功。            |
  | 400    | 参数缺失或无效。          |
  | 401    | 未授权访问。              |
  | 500    | 服务器错误。              |

- **["批量保护 Excel 文件"](https://docs.aspose.cloud/cells/batch/protect "Batch Protect Excel Files")**  
  *为多个工作簿添加保护设置（例如：只读、结构保护）。*  

  **API 详情**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **参数**  

  | 名称          | 类型   | 描述                             |
  |---------------|--------|----------------------------------|
  | files         | array  | 文件标识符或 URL 的列表。         |
  | protection    | object | 保护选项（例如：readOnly、structure）。 |
  | storage       | string | （可选）云存储名称。              |

  **响应**  

  | 状态码 | 描述                       |
  |--------|----------------------------|
  | 200    | 保护设置应用成功。          |
  | 400    | 请求数据无效。              |
  | 401    | 身份验证失败。              |
  | 500    | 意外服务器错误。            |

- **["批量拆分"](https://docs.aspose.cloud/cells/batch/split "Batch Split")**  
  *根据工作表或行范围将大型 Excel 工作簿拆分为多个较小的文件。*  

  **API 详情**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **参数**  

  | 名称        | 类型   | 描述                             |
  |-------------|--------|----------------------------------|
  | files       | array  | 待拆分的文件列表。                |
  | splitBy     | string | 拆分依据："worksheet" 或 "rowRange"。 |
  | criteria    | object | 所选拆分方法的具体参数。          |
  | storage     | string | （可选）云存储名称。              |

  **响应**  

  | 状态码 | 描述                             |
  |--------|----------------------------------|
  | 200    | 拆分操作完成；返回拆分后的文件部分。 |
  | 400    | 拆分参数不正确。                  |
  | 401    | 未授权请求。                      |
  | 500    | 处理错误。                        |

- **["批量解锁"](https://docs.aspose.cloud/cells/batch/unlock "Batch Unlock")**  
  *在一次调用中移除多个 Excel 文件的密码保护。*  

  **API 详情**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **参数**  

  | 名称     | 类型   | 描述                           |
  |----------|--------|--------------------------------|
  | files    | array  | 已锁定文件的标识符或 URL 的列表。|
  | password | string | 文件当前的密码。                |
  | storage  | string | （可选）云存储名称。            |

  **响应**  

  | 状态码 | 描述                       |
  |--------|----------------------------|
  | 200    | 文件解锁成功。              |
  | 400    | 密码错误或文件缺失。        |
  | 401    | 未授权访问。                |
  | 500    | 服务器端故障。              |
---