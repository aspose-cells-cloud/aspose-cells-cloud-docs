---
title: "Aspose.Cells Cloud 中本地文件处理与云端文件处理有何区别？"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud 中本地文件处理与云端文件处理有何区别？"
linktype: "本地文件处理与云端文件处理"
type: docs
url: /zh/learn/local-file-processing-vs-cloud-file-processing/
description: "对比 Aspose.Cells Cloud 的本地文件与云端文件处理方式：存储、成本、安全性及典型应用场景，助您了解哪种方案更契合您的工作流。"
keywords: "Aspose.Cells Cloud, 本地文件处理, 云端文件处理, 电子表格转换, API"
weight: 10
---

本地文件处理与云端文件处理是两种不同的数据管理范式，在文件存储基础设施、业务处理流程、访问方式、成本结构、安全性以及适用场景等方面存在显著差异。两者的主要区别如下：

**前置条件：** 使用以下示例前，请确保您已拥有有效的 Aspose.Cells Cloud 账户、已安装最新版 SDK，并准备好用于身份验证的 Client Id 和 Client Secret。

## 1. 文件存储位置与基础设施

- **本地文件：**

  - 文件存储在用户自有或管理的物理设备上，例如个人电脑硬盘、内部服务器或外接硬盘。**您可直接将 Cells Cloud 客户端指向任一本地存储设备上的文件。**
  - 客户完全掌控硬件设备的物理所有权。
  - 基础设施的采购、维护、升级及退役由用户或其组织自行负责。

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# 初始化 CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# 将本地 Excel 文件转换为 PDF
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**API 参考 —— Convert Spreadsheet（转换电子表格）**

| 方法                  | HTTP 谓词 | 端点                | 参数（键）                                         | 响应                          |
|-----------------------|-----------|---------------------|----------------------------------------------------|-------------------------------|
| `convert_spreadsheet` | POST      | `/cells/convert`    | `inputFile` – 源文件路径<br>`format` – 目标格式（如 `pdf`） | `200 OK` – 转换成功<br>`400 Bad Request` – 参数无效<br>`401 Unauthorized` – 身份验证失败 |

- **云端文件：**

  - 文件存储在第三方云服务提供商（如 Aspose 云存储、Dropbox、AWS、Google Cloud、Microsoft Azure）运营的远程数据中心中。**AWS、Dropbox、Google Cloud 和 Microsoft Azure 均可接入 Aspose 云存储。**
  - 用户通过互联网访问文件，无需关心底层硬件的物理位置与维护。
  - 基础设施由云服务提供商负责维护，用户按需使用。

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# 初始化 CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# 将本地文件上传至云端存储
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# 将云端文件导出为指定格式并保存至本地存储
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# 定义远程文件夹（若实际文件夹名称不同，请替换）
RemoteFolder = "PythonSDK"

# 将 Aspose.Cells Cloud 中的 Excel 文件另存为同平台的其他格式文件
api.save_spreadsheet_as(
    SaveSpreadsheet_asRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**API 参考 —— 云端文件操作**

| 方法                       | HTTP 谓词 | 端点                         | 参数（键）                                                                                     | 响应                                      |
|----------------------------|-----------|------------------------------|------------------------------------------------------------------------------------------------|-------------------------------------------|
| `upload_file`              | PUT       | `/cells/storage/file`        | `localPath` – 本地文件路径<br>`remotePath` – 云端存储中的目标路径                             | `200 OK` – 上传成功<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST      | `/cells/{name}/export`       | `name` – 云端文件名<br>`format` – 目标格式（如 `pdf`）<br>`folder` – 可选文件夹               | `200 OK` – 导出成功<br>`400 Bad Request` |
| `save_spreadsheet_as`      | POST      | `/cells/{name}/saveas`       | `name` – 云端文件名<br>`format` – 目标格式<br>`folder` – 目标文件夹                           | `200 OK` – 保存成功<br>`401 Unauthorized` |

## 2. 业务处理

无论是本地文件处理还是云端文件处理，所有业务处理均在 Cells Cloud 服务器端完成，**因此均需依赖互联网连接**。

## 3. 数据访问

- **本地文件处理：**

  - 访问通常仅限于本机设备。
  - 多人协作困难。
  - 更换设备或办公地点时操作不便。

- **云端文件处理：**

  - 只要具备互联网连接，即可随时随地通过任意设备（电脑、手机、平板）访问文件。
  - 天然支持多人实时协作；多个用户可同时编辑同一文档，系统自动处理版本控制。
  - 移动性强，支持灵活办公与远程办公。

## 4. 成本结构与安全性

- **本地文件：**

  - 初期需投入较高资本支出，后续还将产生运维支持等额外费用。
  - 物理安全与网络安全均由用户自行管理与保障。

- **云端文件：**

  - 初期投入低，主要为运营支出，按需付费。
  - 安全性与数据完整性由云服务提供商负责。

## 5. 适用场景

- **本地文件：** 仅支持在本地执行文件操作。
- **云端文件：** 支持本地与云端均可执行文件操作。

**注意事项 / 限制：** API 仅支持最大 200 MB 的文件用于云端处理，且仅支持文档中列出的格式转换。大体积电子表格的处理时间可能受网络延迟影响。

_最后更新时间：2026 年 7 月 30 日_