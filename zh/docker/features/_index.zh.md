---
title: "Aspose.Cells Cloud Docker 核心功能：电子表格转换、合并、拆分、保护、数据处理等"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud Docker 核心功能"
linktitle: "功能特性"
type: docs
url: /zh/docker-container-features/
description: "通过 Aspose.Cells Cloud Docker 容器在本地运行 Aspose.Cells Cloud API——一种基于 Docker 的容器化服务，提供完整的电子表格处理能力、数据隐私保障及离线处理功能，无需依赖 Aspose 的公共云服务。"
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - 电子表格转换
  - Excel 处理
  - PDF 导出
  - CSV 处理
  - REST API
  - 容器化服务
  - 私有云
  - 离线处理
---

## 什么是 Aspose.Cells Cloud Docker 容器？

Aspose.Cells Cloud Docker 容器是由 Aspose 提供的一种容器化服务，基于 Docker 构建，允许您在本地或私有云环境中部署 Aspose.Cells Cloud API 的各项功能，而无需依赖 Aspose 的公共云服务。

## 为何选择 Aspose.Cells Cloud Docker 容器？

Aspose.Cells Cloud Docker 容器是一款强大的电子表格处理服务容器，支持以下功能：

### 核心功能

- 读取和写入 Excel 文件（XLS、XLSX、CSV、ODS 等）
- 公式计算、图表、条件格式、数据透视表等
- 格式转换（例如：Excel 转 PDF、HTML、图像等）
- 单元格操作、样式设置、工作表管理等

Aspose.Cells Cloud Docker 容器将上述功能封装为 RESTful API，并打包为 Docker 镜像，使您能够在自有基础设施上运行该服务。

### 主要优势

| 优势项             | 描述                                                                 |
| ------------------ | -------------------------------------------------------------------- |
| 数据隐私与安全     | 所有文件处理均在您的私有网络内完成，无需上传至第三方云平台。         |
| 离线可用性         | 不依赖 Aspose 公共云服务，适用于内网或隔离环境。                     |
| 可扩展性           | 可通过 Docker/Kubernetes 轻松横向扩展服务实例。                     |
| API 统一性         | 完全兼容 Aspose.Cells Cloud 公共 API，无需修改现有代码。             |
| 授权控制           | 支持两种授权方式，您可根据自身需求选择合适方案。                     |

## 如何使用 Aspose.Cells Cloud Docker 容器

请参阅用户手册——[《如何使用 Aspose.Cells Cloud Docker 容器》](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container)。

**前提条件**

- 主机上已安装 Docker Engine 20.10 或更高版本。  
- 为容器分配最低 2 GB 内存和 2 个 CPU 核心，以满足典型工作负载需求。  
- 将有效的 Aspose.Cells Cloud 授权文件（或访问令牌）放置于将被挂载进容器的目录中。

**快速入门**

1. 拉取 Docker 镜像：`docker pull aspose/cells-cloud`  
2. 启动容器并挂载授权文件及数据目录，例如：  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. 通过 `http://localhost:8080/v3.0/` 访问 REST API。更多 API 使用详情，请参阅 [Aspose.Cells Cloud API 参考文档](https://docs.aspose.cloud/cells/api-reference/)。

## 参考文档

- [《如何配置 Aspose.Cells Cloud Docker 容器存储》](https://docs.aspose.cloud/cells/docker/storage/)