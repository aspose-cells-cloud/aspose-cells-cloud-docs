---
title: "如何设置 Aspose.Cells Cloud Docker 容器的存储位置"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud Docker 容器存储配置"
linktype: "Container Storage"
type: docs
url: /zh/docker/storage/
description: "使用 JSON、PowerShell 或 Bash 配置 Aspose.Cells Cloud Docker 容器的存储位置。"
weight: 30
keywords: "Aspose.Cells, Docker, 容器存储, JSON 配置, PowerShell, Bash"
---

**摘要**：本指南介绍如何在 Windows 和 Linux 上使用 JSON 配置文件和 Docker run 命令配置 Aspose.Cells Cloud Docker 容器的存储位置。

## 默认存储配置 ##

**前提条件**：确保已安装 Docker Engine 20.10 或更高版本，拥有有效的 Aspose.Cells Cloud 许可证密钥（`LicensePublicKey` 和 `LicensePrivateKey`），且已创建并具备适当权限的主机存储文件夹（例如 Windows 上的 `c:/data` 或 Linux 上的 `/data`）。

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 默认路径 ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## 自定义存储配置 ##

当您需要使用其他文件夹来存储 Aspose.Cells Cloud 数据时，请指定自定义存储配置文件。

```bash
docker run -d \
  -v c:/data:c:/data \   # 将主机文件夹挂载为容器存储
  -p 47900:5000 \        # 映射 API 端口
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux 示例*：

```bash
docker run -d \
  -v /data:/data \   # 将主机文件夹挂载为容器存储
  -p 47900:5000 \    # 映射 API 端口
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**参考文档**：

- [如何运行 Aspose.Cells Cloud Docker 容器](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Docker 容器功能](https://docs.aspose.cloud/cells/docker/container-features/)
- [下载 Aspose.Cells Cloud Docker 镜像](https://docs.aspose.cloud/cells/docker/download-image/)
- [管理容器标签](https://docs.aspose.cloud/cells/docker/manage-tags/)