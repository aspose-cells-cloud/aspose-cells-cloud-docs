---
title: "Aspose.Cells Cloud Docker 镜像标签"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud Docker 镜像标签"
linktype: "镜像标签"
type: docs
url: /docker/tag-list/
description: "查找适用于 Windows Server（2016–2022）和 Linux 的最新 Aspose.Cells Cloud Docker 镜像标签。一站式获取拉取命令、架构详情及升级说明。"
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker 镜像标签"
  - "Docker 拉取命令"
  - "Windows Server Docker 标签"
  - "Linux Docker 标签"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud 提供适用于 Windows Server（2016、2019、2022）和 Linux 的即用型 Docker 镜像。  
每个镜像均通过**标签（tag）**进行版本标识，该标签指明了产品发布版本及目标操作系统。  
请使用下方标签拉取所需的确切镜像，并参考配套的拉取与运行示例快速启动服务。

*最后更新日期：2026-07-01*

**前置条件：** 确保已安装 Docker Engine 20.10 或更高版本，并拥有有效的 Aspose.Cells Cloud 授权密钥。镜像专为指定的 Windows Server 版本或 Linux x64 平台构建。

## Windows Server 2016 镜像 ##

标签 | 架构 | Dockerfile | 备注
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile 未公开发布 — 构建详情请参阅[发行说明](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016)。 | Windows Server 2016 不再计划发布新标签；此为最终发布版本。

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

附加资源：[Docker 下载](/cells/docker/downloads/)、[发行说明](/cells/release-notes/)、[前置条件](/cells/docker/prerequisites/)。  
更多详情请参阅[Docker 概述](/cells/docker/)。

## Windows Server 2019 镜像 ##

标签 | 架构 | Dockerfile | 备注
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile 未公开发布 — 构建详情请参阅[发行说明](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019)。 | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

附加资源：[Docker 下载](/cells/docker/downloads/)、[发行说明](/cells/release-notes/)、[前置条件](/cells/docker/prerequisites/)。  
更多详情请参阅[Docker 概述](/cells/docker/)。

## Windows Server 2022 镜像 ##

标签 | 架构 | Dockerfile | 备注
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile 未公开发布 — 构建详情请参阅[发行说明](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022)。 | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

附加资源：[Docker 下载](/cells/docker/downloads/)、[发行说明](/cells/release-notes/)、[前置条件](/cells/docker/prerequisites/)。  
更多详情请参阅[Docker 概述](/cells/docker/)。

## Linux 镜像 ##

标签 | 架构 | Dockerfile | 备注
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile 未公开发布 — 构建详情请参阅[发行说明](https://github.com/aspose-cells/dockerfiles/tree/main/linux)。 | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

附加资源：[Docker 下载](/cells/docker/downloads/)、[发行说明](/cells/release-notes/)、[前置条件](/cells/docker/prerequisites/)。  
更多详情请参阅[Docker 概述](/cells/docker/)。

**版本变更日志**

标签 | 变更内容
---|---
`ltsc2016.23.5.0` | Windows Server 2016 的最终发布版本；包含安全补丁与性能改进。
`ltsc2019.25.10.0` | 更新至 Aspose.Cells 25.10.0；新增公式支持及 bug 修复。
`ltsc2022.25.10.0` | 与 2019 标签版本相同，针对 Windows Server 2022 运行时进行了优化。
`linux.25.10.0` | 基于 Linux 的镜像，集成 Aspose.Cells 25.10.0；包含更新的依赖项及 Linux 特定优化。