---
title: "如何运行 Aspose.Cells Cloud Docker 容器"
second_title: "文档"
ArticleTitle: "如何运行 Aspose.Cells Cloud Docker 容器"
linktitle: "容器运行"
type: docs
url: /zh/run-aspose-cells-cloud-docker-container/
description: "了解如何在 Windows Server 2022 上启动 Aspose.Cells Cloud Docker 容器。提供试用模式、按量计费模式、许可证计费模式、存储配置及健康检查的分步命令。"
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, 试用模式, 按量计费, 许可证计费, 存储配置"
---

Aspose.Cells Cloud Docker 提供了一个可直接运行的容器镜像，用于在本地或私有云中托管 Aspose.Cells Cloud API。本指南将介绍如何以三种常见许可模式——**试用模式**、**按量计费模式** 和 **许可证计费模式**——启动容器，并包含一种使用访问令牌（access token）的变体。所有命令均针对 Windows Server 2022 上的 PowerShell 编写；若您使用 Linux，请相应调整卷路径。

**前提条件**

- 已安装并运行 Docker Engine 20.10 或更高版本。  
- PowerShell 5.1 或 PowerShell 7+。  
- 容器内开放端口 5000（映射到主机端口 47900），并确保主机防火墙允许端口 47900 的入站流量。  
- 若使用按量计费或许可证计费模式，请准备好 `LicensePublicKey`、`LicensePrivateKey` 或许可证文件；若使用令牌模式，请准备好 `AccessToken`。  
- 准备一个本地文件夹（例如 `C:\data`），用于挂载为容器的存储目录。

**快速入门（试用模式）**

运行以下命令以试用模式启动容器：

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## 以试用模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

该容器将在前台运行，并监听主机端口 **47900**（映射至容器内部端口 **5000**）。

## 以按量计费模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
# 按量计费模式：将 LicensePublicKey 和 LicensePrivateKey 设置为环境变量。
# 挂载存储目录（主机 → 容器）
#   -v c:/data:c:/data
# 挂载 Windows 字体目录，以便 API 可访问系统字体
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

容器将以分离模式（`-d`）运行。启动后，可通过以下命令验证服务是否可访问：

```powershell
curl http://localhost:47900/v3.0/health
```

**示例 `storageResource.json` 文件内容：**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## 以许可证计费模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
# 许可证计费模式：通过 LicenseFile 环境变量提供许可证文件路径。
# 挂载存储目录（主机 → 容器）
#   -v c:/data:c:/data
# 挂载 Windows 字体目录
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## 使用访问令牌运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
# 访问令牌模式：设置 AccessToken，并可选地配置按量计费所需的密钥。
# 挂载存储目录
#   -v c:/data:c:/data
# 挂载 Windows 字体目录
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

容器启动后，使用前述健康检查命令验证服务是否正常运行。

## 参考文档

- [如何配置 Aspose.Cells Cloud Docker 容器的存储](https://docs.aspose.cloud/cells/docker/storage/)

---

### 故障排除

- **健康检查失败** — 确保端口 47900 未被防火墙阻止，并确认容器正在运行（使用 `docker ps` 查看）。  
- **许可证错误** — 请核实 `LicensePublicKey`、`LicensePrivateKey` 或 `LicenseFile` 的值是否正确，并确保环境变量传入时无多余空格。  
- **存储不可访问** — 确认主机目录（如 `c:/data`）存在，且 Docker 具备对该目录的读写权限。

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "如何运行 Aspose.Cells Cloud Docker 容器",
  "description": "分步指南，介绍如何在 Windows Server 2022 上以试用模式、按量计费模式、许可证计费模式及访问令牌模式启动 Aspose.Cells Cloud Docker 容器。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, 试用模式, 按量计费, 许可证计费, 存储配置"
}
</script>
---