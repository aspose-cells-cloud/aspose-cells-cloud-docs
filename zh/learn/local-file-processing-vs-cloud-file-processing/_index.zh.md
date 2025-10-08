---
title: Aspose.Cells 云中的本地文件处理和云文件处理有什么区别
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: 本地文件处理与云文件处理
type: docs
url: /zh/learn/local-file-processing-vs-cloud-file-processing/
description: 本地文件处理和云端文件处理有什么区别？本地文件处理和云端文件处理是两种根本不同的数据管理范式，在存储基础设施、业务处理、访问方式、成本结构、安全性和适用场景等方面存在显著差异。
weight: 10
kwords: Excel 云 API、REST、电子表格、PDF、CSV、Json、Markdown、本地文件处理与云文件处理
---
本地文件处理和云端文件处理是不同的数据管理范式，在文件存储基础设施、业务处理、访问方式、成本结构、安全性、适用场景等方面存在显著差异。两者主要区别在于：

## 1. 文件存储位置和基础设施

- 本地文件：

 文件存储在用户拥有或管理的物理设备上，例如个人电脑硬盘、内部服务器或外部移动硬盘。Cells 云客户端可以直接访问这些设备。
 - 客户对硬件拥有完全的物理控制权。
 - 基础设施的购买、维护、升级和退役是用户或其组织的责任。

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- 云文件：

 - 文件存储在由第三方云服务提供商（Aspose 云存储、Dropbox、AWS、Google Cloud、Microsoft Azure）运营的远程数据中心。AWS、Dropbox、Google Cloud 和 Microsoft Azure 均可将人们连接到 Aspose 云存储。
 - 客户可以通过互联网访问这些文件，而无需考虑底层硬件的位置和维护。
 - 基础设施由云服务提供商负责，用户按需使用。

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2.业务处理

无论本地文件处理还是云端文件处理，所有业务处理均在Cells云服务器中完成，**因此需要互联网支持**.

## 3. 数据访问

- 本地文件处理：

 - 访问通常仅限于设备本身。
 - 多人协作困难。
 - 更换设备或位置不便。

- 云文件处理：

 - 只要您有互联网连接，即可随时随地从任何设备（计算机、手机、平板电脑）访问文件。
 - 天然支持多人实时协作，多个用户可以同时编辑同一篇文档，系统自动处理版本控制。
 - 强大的移动性、灵活的 office 支持和远程工作。
  
## 4. 成本结构与安全性

- 本地文件：
  
 前期资本支出较高，后期需要一定的成本来支撑运营。
 物理安全和网络安全均由用户自己控制。

- 云文件：

 - 前期投资低，主要是运营费用，按需付费。
 - 安全性和完整性是云服务提供商的责任。

## 5.适用场景

- 本地文件：文件操作只能在本地进行。
- 云端文件：文件操作可以在本地进行，也可以在云端进行。
