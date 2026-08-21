---
title: "Aspose.Cells Cloud Docker 操作手册：在您自己的私有基础设施上部署 Aspose.Cells Cloud 应用程序"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud Docker 操作手册"
linktype: "docs"
url: "/docker-developer-guide/"
aliases: ["/docker/", "/docker/run/"]
description: "将 Aspose.Cells Cloud 作为 Docker 容器部署在私有或本地基础设施上，实现电子表格处理（Excel、PDF、CSV、JSON、Markdown），而无需使用 Aspose 的公有云。"
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker 镜像",
    "电子表格 API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "私有云",
    "部署",
  ]
weight: 30
---

Aspose.Cells Cloud 是一种基于云的电子表格处理服务，支持创建、编辑、转换及操作 Excel 等格式的文件。通过 Docker 部署，可快速构建独立的服务环境，简化依赖管理与跨平台部署流程。

本手册将详细介绍从环境准备到服务验证的完整操作步骤。

## 环境准备

在部署 Aspose.Cells Cloud Docker 容器之前，请确保本地环境满足以下依赖要求，以避免因缺少组件导致部署失败。

### 基础依赖组件

- **Docker Engine：** 容器运行时核心引擎，负责创建与管理容器。最低版本要求为 **18.09.0**。
- **操作系统：** 支持 Docker 的主流操作系统如下：

  | 操作系统类型 | 版本                      |
  | :----------- | :------------------------ |
  | Windows      | Windows 10/11             |
  | Windows Server | 2016 / 2019 / 2022      |
  | Linux        | CentOS 7+ / Ubuntu 20.04+ |

- **硬件资源：** 确保服务稳定运行，避免因资源不足导致崩溃。
  - CPU：2 核或以上。
  - 内存：4 GB 或以上。
  - 磁盘：至少 10 GB 可用空间。

### 关键前置条件

- **Aspose 许可证：** 注册 Aspose 官方账户以获取有效许可证（可申请试用版或购买商业版）。未配置许可证可能导致功能受限。详情请参阅 [许可证](https://purchase.aspose.com/buy) 页面。
- **网络连通性：** 确保部署环境可访问 Docker Hub（用于拉取镜像）。

## 获取 Aspose.Cells Cloud Docker 镜像

Aspose.Cells Cloud 镜像托管于 Docker Hub，可直接通过 `docker pull` 命令拉取，无需手动构建。

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## 运行 Aspose.Cells Cloud Docker 容器

### 运行参数说明

| 名称                      | 描述                                                         | 备注                                 |
| ------------------------- | ------------------------------------------------------------ | ------------------------------------ |
| LicensePublicKey          | 使用计费（Metered）模式时设置许可证公钥。                   | 仅在采用计费模式时生效。             |
| LicensePrivateKey         | 使用计费（Metered）模式时设置许可证私钥。                   | 仅在采用计费模式时生效。             |
| storagesCredentialsFilePath | 存储配置文件路径，默认为 `./storageResource.json`。         |                                      |
| LicenseFile               | 使用许可证文件（LicenseFile）模式时设置许可证文件路径。     | 仅在采用许可证文件模式时生效。       |
| AccessToken               | 访问 API 所需的令牌。                                        | 若为空，则无需令牌验证。             |

### 运行命令

以试用模式运行容器非常简单：

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

若需完整功能，请获取 [计费模式许可证（Metered License）](https://purchase.aspose.com/faqs/licensing/metered/) 并挂载主机目录用于文件存储。此时运行命令如下所示：

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### API 参考地址 – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### 端口暴露说明

| 端口 | 描述                               | 是否必需 |
| ---- | ---------------------------------- | -------- |
| 5000 | 用于渲染文档的字体所在文件夹       | 是       |

### 必需挂载卷说明

| 容器内挂载路径 | 描述                               | 是否必需 | 备注                                       |
| -------------- | ---------------------------------- | -------- | ------------------------------------------ |
| C:\fonts       | 用于渲染文档的字体所在文件夹       | 否       | 解决因缺少字体导致的电子表格/Excel 渲染问题。 |
| C:\data        | 文件存储目录                       | 否       | 扩展存储空间，便于文件管理与访问。         |

## 参考文档

- [Aspose.Cells Cloud Docker 容器核心功能](https://docs.aspose.cloud/cells/docker-container-features/)
- [如何配置 Aspose.Cells Cloud Docker 容器存储](https://docs.aspose.cloud/cells/docker/storage/)
- [如何运行 Aspose.Cells Cloud Docker 容器](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)