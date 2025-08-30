---
title: 多克
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells 云
weight: 30
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells 云 Docker

Aspose.Cells 云映像可用于 Linux、Microsoft Windows 11 Pro、Microsoft Windows Server 2016、Microsoft Windows Server 2019、Microsoft Windows Server 2022。

## API 参考 - Aspose.Cells 云 Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## 暴露端口

端口 | 描述 | 必填
---|:--:|---:
5000 | 包含字体的文件夹，将用于呈现文档 | true

## 所需卷 ##

容器中的挂载路径 | 描述 | 必填
---|:--:|---:
C:\fonts | 包含字体的文件夹，将用于呈现文档 | false
C:\data | 文件存储文件夹 | false

## 运行参数 ##

名称 | 描述 | 必填
---|:--:|---:
LicensePublicKey | 许可证的公钥 | true
LicensePrivateKey | 许可证的私钥 | true
storagesCredentialsFilePath | 存储配置文件路径。默认文件为 ./storageResource.json | true

## 运行命令 ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}

**参考文档** :

- [Docker 运行]( https://docs.docker.com/engine/reference/commandline/run/)
-

看：

- [下载信息](/cells/zh/docker/downloads/)
- [运行版本信息](/cells/zh//docker/tag-list/)
- [存储信息](/cells/zh/docker/storage/)
