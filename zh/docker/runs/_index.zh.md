---
title: 如何运行 Aspose.Cells Cloud Docker Containe
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: 集装箱俄罗斯
type: docs
url: /zh/run-aspose-cells-cloud-docker-container/
description: 如何运行 Aspose.Cells Cloud Docker 容器。Aspose.Cells Cloud Docker 容器是 Aspose 提供的基于 Docker 的容器化服务，允许您在本地或私有云环境中部署 Aspose.Cells Cloud API 的功能，而无需依赖 Aspose 的公共云服务
weight: 30
kwords: Excel 云 Docker 容器、自云 Docker 容器、REST Docker 容器、电子表格、PDF、CSV、Json、Markdown、Docker 镜像、运行 Docker 容器
---
## 以试用模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## 以计量计费模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## 以许可计费模式运行 Aspose.Cells Cloud Docker 容器

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## 参考文献

- [如何配置Aspose.Cells云Docker容器存储。](https://docs.aspose.cloud/cells/docker/storage/)
