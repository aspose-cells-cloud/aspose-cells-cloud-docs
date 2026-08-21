---
title: "运行 Aspose.Cells Cloud Docker 容器——拉取、配置与启动"
second_title: "文档"
ArticleTitle: "如何运行 Aspose.Cells Cloud Docker 容器"
LinkTitle: "Docker 容器"
type: docs
url: /zh/getting-started/how-to-run-docker-container/
aliases: [  /zh/how-to-run-docker-container/ ]
description: "了解如何在 Windows 或 Linux 上拉取、配置并运行 Aspose.Cells Cloud Docker 容器。包含 Docker‑Compose YAML 配置、许可证设置、端口映射及故障排除建议。"
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker 容器"
  - "Docker Compose"
  - "许可证密钥"
  - "Excel"
  - "电子表格"
  - "云 API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Docker 技术旨在通过轻量级容器自动化应用程序的部署流程。开发者可利用 Docker 容器将应用程序及其所有依赖库和组件打包为单一部署单元。

Aspose.Cells Cloud 团队已在 <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> 上发布了 Docker 容器，以方便 Docker 用户使用。

**前置条件** —— 确保已安装 Docker Engine ≥ 20.x，且操作系统（Windows 10 / Server 2019 / 2022 或受支持的 Linux 发行版）满足相关要求。可选提供许可证密钥以启用授权模式。

- 已安装 Docker Engine ≥ 20.x  
- 支持的操作系统（Windows 10 / Server 2019 / 2022 或 Linux 发行版）  
- 可选许可证密钥（用于授权模式）

## 容器配置

### 必需挂载卷

| 容器内挂载路径 | 说明 |
| :--- | :--- |
| C:\fonts | 用于文档渲染的字体文件夹 |
| C:\data | 文件存储目录 |

**Linux/macOS 替代方案** —— 在容器中使用 `/fonts` 和 `/data` 路径，并在运行容器时将其映射到主机目录，例如 `/home/user/fonts` 和 `/home/user/data`。

### 参数说明

| 参数名 | 说明 |
| :--- | :--- |
| LicensePublicKey | 许可证公钥 |
| LicensePrivateKey | 许可证私钥 |

若省略 **License** 参数，应用将以试用模式运行。

### 1. 拉取 Aspose.Cells Cloud 镜像

```bash
# 拉取指定版本的 Aspose.Cells Cloud 镜像
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# 拉取适用于 Windows Server 2019 的 Aspose.Cells Cloud 镜像
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# 拉取适用于 Windows Server 2022 的 Aspose.Cells Cloud 镜像
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# 拉取适用于 Windows 11 的 Aspose.Cells Cloud 镜像
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **注意：** 为始终获取最新版本，也可拉取 `latest` 标签：`docker pull aspose/cells-cloud:latest`。

### 2. Docker‑Compose 工具配置文件

可在 **docker‑compose.yml** 文件中写入以下配置：

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # 主机端口 5000 → 容器端口 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **注意：** 端口映射 `5000:80` 表示 API 将可通过 `http://localhost:5000` 访问。

### 3. 使用命令行运行 Docker 容器

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**故障排除：**  
- **端口冲突：** 确保主机上的 5000 端口未被占用，或将其映射至其他空闲端口。  
- **许可证加载失败：** 检查公钥与私钥是否已正确作为环境变量传入，或是否已挂载为文件。  
- **字体缺失：** 若文档渲染时字体显示异常，请确认字体目录已正确挂载并包含所需字体文件。

**相关资源：**  
- <a href="/cells/api/">API 参考文档</a> | <a href="/cells/license/">许可证激活指南</a> | <a href="/cells/getting-started/">入门概述</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "拉取 Docker 镜像",
      "text": "运行 `docker pull aspose/cells-cloud:<version>` 下载所需镜像。"
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "创建 docker‑compose 文件",
      "text": "在 `docker‑compose.yml` 中定义镜像、端口、挂载卷及许可证环境变量。"
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "运行容器",
      "text": "执行 `docker run`，并传入合适的环境变量、卷挂载和端口映射参数。"
    }
  ]
}
```